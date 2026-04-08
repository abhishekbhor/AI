<div align="center">

# No Cameraman Left Behind

### AI-Assisted Human Insertion into Complex Group Photos

<p>
  A computer vision project that helps a photographer or cameraman insert themselves into a group photo
  or scene after the picture is taken, while preserving realistic front/back object layering.
</p>

</div>

<hr>

<h2>Overview</h2>

<p>
This project explores a practical computer vision problem: how to let the person taking the photo
appear inside the final image, even in complex real-world scenes with multiple people and objects.
The idea is to first isolate the source person from one image, then insert that person into a target
scene while controlling which target objects should remain in front and which should remain behind.
</p>

<p>
The attached project writeup describes this as a solution for cases such as family group photos or
journalistic scenes, where the photographer later wants to place themselves into the final composition.
</p>

<hr>

<h2>Problem Statement</h2>

<p>
Traditional image insertion often works poorly in realistic scenes because it is not enough to simply
paste a person into a background. The inserted person must:
</p>

<ul>
  <li>be segmented cleanly from a source image, even in a cluttered environment</li>
  <li>be positioned correctly inside a target image</li>
  <li>appear behind selected target objects when needed</li>
  <li>blend naturally without halos, ghosting, or background bleeding</li>
</ul>

<p>
This project solves that problem by combining interactive object selection, segmentation, composite-mask
construction, and image blending. :contentReference[oaicite:2]{index=2}
</p>

<hr>

<h2>Core Idea</h2>

<p>
The system lets a user:
</p>

<ol>
  <li>select the cameraman or source person from one image</li>
  <li>select foreground objects in the target image that should remain in front</li>
  <li>build a composite mask representing source and target layering</li>
  <li>blend the source into the target image with realistic depth ordering</li>
</ol>

<p>
The project specifically aims to work not just on plain backgrounds, but on day-to-day scenes with
multiple humans and environmental complexity. :contentReference[oaicite:3]{index=3}
</p>

<hr>

<h2>Tech Stack</h2>

<ul>
  <li>Google Colab</li>
  <li>Jupyter Notebook</li>
  <li>Jupyter BBox Widget for interactive bounding-box selection</li>
  <li>Meta SAM2 for image segmentation</li>
  <li>OpenCV for blending</li>
  <li>Poisson-based blending / linear interpolation</li>
  <li>cv2.seamlessClone for baseline experiments</li>
</ul>

<p>
These tools are listed in the project’s solution summary. :contentReference[oaicite:4]{index=4}
</p>

<hr>

<h2>Pipeline</h2>

<p>
The end-to-end workflow is:
</p>

<ol>
  <li>User uploads a source image</li>
  <li>User creates a bounding box around the source subject</li>
  <li>User may optionally enlarge the source mask</li>
  <li>User uploads a target image</li>
  <li>User creates one or more bounding boxes around target objects</li>
  <li>System creates composite masks</li>
  <li>System computes a final mask using source and target masks</li>
  <li>System generates the merged image</li>
</ol>

<p>
The process diagram in the project document lays out this flow explicitly. :contentReference[oaicite:5]{index=5}
</p>

<hr>

<h2>Approach</h2>

<h3>1. Interactive Object Selection</h3>

<p>
A major design choice in this project was to let the user interactively define objects of interest using
bounding boxes. This turned out to be more effective than relying fully on automatic segmentation,
because the user could precisely select the intended person amid other distractions in the scene.
</p>

<p>
The writeup notes that the <code>Jupyter BBox Widget</code> worked well in Google Colab for this purpose. :contentReference[oaicite:6]{index=6}
</p>

<h3>2. Image Segmentation with Meta SAM2</h3>

<p>
The project evaluated Meta’s SAM2 in two modes:
</p>

<ul>
  <li>Automatic Mask Generation</li>
  <li>Mask Predictor</li>
</ul>

<p>
Automatic mask generation was rejected because it often over-segmented people into clothing parts or
produced too many inconsistent masks. The predictor-based workflow was better because it allowed user-guided
selection through clicks or bounding boxes. :contentReference[oaicite:7]{index=7}
</p>

<p>
Among the available SAM2 model sizes, the project found that the <strong>tiny</strong> model was adequate
for the use case, which helped manage GPU cost. :contentReference[oaicite:8]{index=8}
</p>

<h3>3. Composite Mask Construction</h3>

<p>
A key breakthrough in the project was moving from single-object masks to composite masks. A single
bounding box around multiple objects produced poor and pixelated masks, while separate boxes around
individual objects gave clean masks that could then be combined. :contentReference[oaicite:9]{index=9}
</p>

<p>
This made it possible to create a target-side composite mask and then compute a final layered mask of:
</p>

<pre><code>Final Mask = Source Mask - Target Combined Mask</code></pre>

<p>
That subtraction-based approach allowed the source person to be placed behind selected target objects. :contentReference[oaicite:10]{index=10}
</p>

<h3>4. Image Blending</h3>

<p>
The project experimented with two main blending options:
</p>

<ul>
  <li><code>cv2.seamlessClone</code></li>
  <li>Poisson-equation-based blending</li>
</ul>

<p>
The initial <code>cv2.seamlessClone</code> approach worked for simpler masks, but it struggled with correct
center placement and produced misaligned results. The writeup shows that the inserted source figure could be
lifted incorrectly toward the center of the image. :contentReference[oaicite:11]{index=11}
</p>

<p>
Poisson blending solved the positioning issue more effectively and became the final preferred method,
though it introduced additional mask-boundary and gradient-related challenges. :contentReference[oaicite:12]{index=12}
</p>

<hr>

<h2>Key Experiments</h2>

<ul>
  <li>Automatic vs predictor-based SAM2 segmentation</li>
  <li>Single-object vs multi-object selection</li>
  <li>Bounding-box selection vs click-based selection</li>
  <li>Tiny vs larger SAM2 model variants</li>
  <li>Composite-mask creation through mask subtraction</li>
  <li>cv2.seamlessClone vs Poisson blending</li>
  <li>Mask dilation, feathering, grayscale preprocessing, contour detection, and edge padding</li>
</ul>

<p>
These experiments are described in the writeup’s “Experiments & results” section. :contentReference[oaicite:13]{index=13}
</p>

<hr>

<h2>Challenges Encountered</h2>

<p>
This project surfaces several realistic computer vision challenges:
</p>

<ul>
  <li>automatic segmentation was unpredictable across images</li>
  <li>single-box multi-object selection produced poor masks</li>
  <li>source figures could be misplaced during blending</li>
  <li>tight masks caused ghosting artifacts</li>
  <li>enlarged masks could create halos</li>
  <li>target background could bleed into the source object</li>
  <li>darkening artifacts appeared when mask/background values were adjusted poorly</li>
</ul>

<p>
The writeup shows examples of ghosting, halo effects, darkened targets, and background bleeding,
especially in the experiment pages. :contentReference[oaicite:14]{index=14} :contentReference[oaicite:15]{index=15}
</p>

<hr>

<h2>Important Technical Lessons</h2>

<ul>
  <li>
    <strong>Bounding-box-guided segmentation is more practical than fully automatic masks</strong>
    for this kind of user-facing interaction.
  </li>
  <li>
    <strong>Single-object masks are much easier to blend than composite layered masks</strong>.
  </li>
  <li>
    <strong>Tight masks can create ghosting</strong>, because border gradients get lost.
  </li>
  <li>
    <strong>Dilating the mask and including a small background margin</strong> improves blending,
    though the chosen fill color matters.
  </li>
  <li>
    <strong>Poisson blending handled placement better than seamlessClone</strong> for this project.
  </li>
</ul>

<p>
The writeup explicitly notes that enlarging the mask with morphological operations and using a color like gray
around boundaries was a better starting point for blending. :contentReference[oaicite:16]{index=16}
</p>

<hr>

<h2>Results</h2>

<p>
The final results section shows successful examples across multiple scenarios:
</p>

<ul>
  <li>plain or simple backgrounds</li>
  <li>slightly more complex scenes</li>
  <li>typical indoor day-to-day environments</li>
  <li>cases where the source person is inserted behind selected objects</li>
</ul>

<p>
The final result gallery in the project document demonstrates that the system achieved visually credible
insertions across several scenes. :contentReference[oaicite:17]{index=17}
</p>

<hr>

<h2>What Worked Best</h2>

<ul>
  <li>user-drawn bounding boxes for object selection</li>
  <li>SAM2 predictor mode instead of automatic masks</li>
  <li>tiny SAM2 model for sufficient quality at lower cost</li>
  <li>multiple clean masks combined into a composite mask</li>
  <li>Poisson blending for improved placement control</li>
</ul>

<hr>

<h2>Limitations</h2>

<ul>
  <li>GPU cost was a major constraint for SAM2 usage in Colab</li>
  <li>complex backgrounds still reduced reliability</li>
  <li>some results required manual tweaking of mask size and edges</li>
  <li>the pipeline was not fully automated for pose, lighting, and orientation consistency</li>
  <li>success was stronger on flatter backgrounds than highly complex scenes</li>
</ul>

<p>
The project reflection also notes that success on complex backgrounds was only partial and sometimes required
expert mask tuning. :contentReference[oaicite:18]{index=18}
</p>

<hr>

<h2>Future Improvements</h2>

<ul>
  <li>pose alignment with ChatPose</li>
  <li>better photorealistic blending with Adobe Unihuman or diffusion-based approaches</li>
  <li>more automated mask refinement</li>
  <li>improved lighting and orientation consistency</li>
  <li>less user intervention for edge and gradient correction</li>
</ul>

<p>
These next-step ideas are documented in the report’s future work section. :contentReference[oaicite:19]{index=19}
</p>

<hr>

<h2>What I Learned</h2>

<ul>
  <li>Colab is workable, but limiting for refined productization</li>
  <li>SAM2 was powerful, but not ideal for the project’s cost constraints</li>
  <li>interactive selection tools in notebooks can meaningfully improve usability</li>
  <li>mask composition and layered blending are much harder than single-object insertion</li>
  <li>OpenCV blending techniques require careful gradient and boundary handling</li>
</ul>

<p>
The project’s concluding reflection emphasizes these implementation lessons and tradeoffs. :contentReference[oaicite:20]{index=20}
</p>

<hr>

<h2>Project Summary</h2>

<p>
<em>No Cameraman Left Behind</em> is a thoughtful computer vision project that combines interactive segmentation,
layer-aware mask composition, and image blending to solve a real user problem: making sure the person taking the
photo can still appear in the final scene.
</p>

<p>
More than a simple cut-and-paste system, the project tackles realistic occlusion, layering, and blending issues,
making it a strong example of applied vision work with user interaction and iterative experimentation.
</p>
