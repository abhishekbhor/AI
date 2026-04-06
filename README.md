<style>
.section-card {
  border: 1px solid #e1e4e8;
  border-radius: 8px;
  padding: 20px;
  margin: 10px 0;
  background-color: #ffffff;
}

.section-title {
  margin-top: 0;
}

.highlight {
  background-color: #f6f8fa;
  padding: 2px 6px;
  border-radius: 4px;
  font-family: monospace;
}

.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
}

.link-box {
  padding: 12px;
  border: 1px solid #d0d7de;
  border-radius: 6px;
  background-color: #f9fafb;
}

@media (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
</style>



# AI - Product Portfolio
My current focus is creating AI products that integrate seamlessly into workflow ecosystems—LLM agents, intelligent recommendations, automated decisioning, and hybrid human-in-the-loop systems that improve accuracy, reduce friction, and scale safely. I’m particularly interested in opportunities at the intersection of AI systems, platform modernization, and regulated, mission-critical operations.

## Education
- M.S., Artificial Intelligence - University of Pennsylvania (Upenn)
- M.S., Computer Science - University of Pennsylvania (Upenn)

<br>


# Projects




<div class="section-card">
   <h3 class="section-title" style="color:#507d2a;">Project I. RAG Assistant</h3>
  <h4>A LLM-powered Retrieval System</h4>
  <a href="https://github.com/abhishekbhor/AI/blob/main/assets/img/rag-architecture.png" target="_blank">
  <img src="assets/img/rag-architecture.png"></a>
  <p>
    A modular <strong>Retrieval-Augmented Generation (RAG) system</strong> designed to simulate real-world AI product architecture — combining search, ranking, observability, caching, and feedback-driven improvement.
  </p>

  <p>
    This project demonstrates how LLM systems evolve into <strong>production-style pipelines</strong> with measurable performance and iterative learning.
  </p>
</div>


<div class="section-card">
  <h3 class="section-title">Key Capabilities</h3>

  <div class="grid">
    <div>Hybrid Retrieval<br><small>FAISS + BM25</small></div>
    <div>Reranking Layer<br><small>Improved relevance</small></div>
    <div>LLM Generation<br><small>Context-aware answers</small></div>
    <div>Observability<br><small>Latency + diagnostics</small></div>
    <div>Caching<br><small>Fast repeat queries</small></div>
    <div>Feedback Loop<br><small>Ranking improvement</small></div>
  </div>
</div>


<div class="section-card">
  <h3 class="section-title">Why this matters</h3>

  <ul>
    <li>Measure <strong>retrieval quality</strong> instead of guessing</li>
    <li>Balance <strong>latency vs accuracy</strong></li>
    <li>Improve results via <strong>user feedback</strong></li>
    <li>Design <strong>production-ready LLM systems</strong></li>
  </ul>
</div>


<div class="section-card">
  <h3 class="section-title">System Design</h3>

  <ul>
    <li>Separate pipelines: ingestion → retrieval → generation</li>
    <li>Provider abstraction (extensible)</li>
    <li>Modular, scalable architecture</li>
    <li>Built with <strong>system thinking</strong></li>
  </ul>
</div>


<div class="section-card">
  <h3 class="section-title">Project Links</h3>

  <div class="grid">
    <div class="link-box">
      <strong>Full System</strong><br>
      <a href="https://github.com/abhishekbhor/rag-assistant" target="_blank">
        View Repository
      </a>
    </div>

    <div class="link-box">
      <strong>Deep Dive</strong><br>
      <a href="https://github.com/abhishekbhor/rag-assistant/blob/main/README.md" target="_blank">
        System Documentation
      </a>
    </div>
  </div>
</div>


<div class="section-card">
  <h3 class="section-title">Tech Stack</h3>

  <p>
    <span class="highlight">Python</span>
    <span class="highlight">FastAPI</span>
    <span class="highlight">FAISS</span>
    <span class="highlight">BM25</span>
    <span class="highlight">OpenAI</span>
  </p>
</div>

<br>
<hr style="border: none; border-top: 2px dotted; color:#507d2a; width: 75%; margin: auto; background: none;">
<br>



<div class="section-card">
  <h3 class="section-title" style="color:#507d2a;">Project II. Big Data Analysis & Prediction</h3>
  <h4>Indicators of Heart Disease</h4>

  <a href="https://medium.com/@nkoro/heart-health-education-is-there-something-were-missing-ee41292c7729" target="_blank">
    <img src="assets/img/heart-health-image.png" alt="Indicators of Heart Disease" class="project-image">
  </a>

  <p>
    <a href="https://medium.com/@nkoro/heart-health-education-is-there-something-were-missing-ee41292c7729" target="_blank"><strong>The study</strong></a>
    used machine learning models such as Random Forest and oversampling techniques like SMOTE to analyze 2022 CDC data and identify the strongest predictors of heart attacks. It found that while age and angina were primary factors, unexpected variables such as dental health also had meaningful predictive value.
  </p>
</div>

<div class="section-card">
  <h3 class="section-title">Key Capabilities</h3>

  <div class="grid">
    <div>Data Cleaning & Wrangling<br><small>Pandas + NumPy</small></div>
    <div>EDA & Visualization<br><small>Matplotlib + Seaborn</small></div>
    <div>Classification Models<br><small>Logistic Regression, Decision Tree, Random Forest</small></div>
    <div>Class Imbalance Handling<br><small>SMOTE</small></div>
    <div>Feature Engineering<br><small>Encoding + feature pruning</small></div>
    <div>Model Evaluation<br><small>Precision, Recall, F1, ROC/AUC</small></div>
  </div>
</div>

<div class="section-card">
  <h3 class="section-title">Tools & Libraries</h3>

  <ul>
    <li><strong>Python</strong> — primary programming language used for analysis and modeling</li>
    <li><strong>Scikit-learn</strong> — model training, evaluation, and ML pipelines</li>
    <li><strong>Pandas & NumPy</strong> — cleaning, transformation, and structured analysis</li>
    <li><strong>Matplotlib & Seaborn</strong> — EDA, correlation plots, and statistical visualization</li>
  </ul>
</div>

<div class="section-card">
  <h3 class="section-title">Models Evaluated</h3>

  <ul>
    <li><strong>Logistic Regression</strong> — baseline model</li>
    <li><strong>Decision Tree Classifier</strong> — improved recall and interpretability</li>
    <li><strong>Random Forest Classifier</strong> — strongest performer with ~97% accuracy and high AUC</li>
  </ul>
</div>

<div class="section-card">
  <h3 class="section-title">Data Engineering & Analytics Techniques</h3>

  <ul>
    <li><strong>SMOTE</strong> — addressed the imbalanced dataset problem by generating synthetic minority samples</li>
    <li><strong>One-Hot Encoding & Label Encoding</strong> — converted categorical variables into model-ready numerical features</li>
    <li><strong>Dendrograms / Hierarchical Clustering</strong> — used to identify and remove redundant correlated features</li>
    <li><strong>Evaluation Metrics</strong> — confusion matrix, recall, precision, F1 score, and ROC/AUC</li>
  </ul>
</div>

<div class="section-card">
  <h3 class="section-title">Data Source</h3>

  <p>
    <strong>2022 CDC Annual Survey</strong><br>
    Specifically the <em>Key Indicators of Heart Disease</em> dataset, which provided the raw data across 40+ variables used in the analysis.
  </p>
</div>



<!--                                                                -->



<br>
<hr style="border: none; border-top: 2px dotted; color:#507d2a; width: 75%; margin: auto; background: none;">
<br>


<div class="section-card">
  <h3 class="section-title" style="color:#507d2a;">Project III. Multi-Modal Image Synthesis</h3>
  <h4>No Cameraman Left Behind</h4>

  <img src="assets/img/comp-vision.png">

  <p>
    An interactive image synthesis system designed to let a user select a “cameraman” from one image and insert that person into a second scene, while preserving realistic foreground/background relationships. The goal was to make the workflow intuitive enough that the user would not need to manually tune mask geometry or blending parameters. 
  </p>

  <p>
    The project explored segmentation, mask composition, and blending strategies to support realistic insertion in everyday scenarios such as family photos, cooking activities, classrooms, studios, and office settings.
  </p>
</div>

<div class="section-card">
  <h3 class="section-title">Problem & Product Goal</h3>

  <ul>
    <li>Allow a user to select the cameraman from a complex real-world scene</li>
    <li>Insert that person into another complex scene with minimal manual effort</li>
    <li>Preserve object layering so the inserted subject can appear behind foreground objects in the target image</li>
    <li>Reduce user burden by avoiding low-level mask and configuration tuning</li>
  </ul>

</div>

<div class="section-card">
  <h3 class="section-title">Solution Workflow</h3>

  <div class="grid">
    <div>User imports source image<br><small>Person to extract</small></div>
    <div>User imports target image<br><small>Scene to insert into</small></div>
    <div>User draws bounding boxes<br><small>Interactive object selection</small></div>
    <div>System generates composite masks<br><small>Per-object mask combination</small></div>
    <div>System computes final mask<br><small>Source mask − target mask</small></div>
    <div>System blends final image<br><small>Preserves occlusion relationships</small></div>
  </div>
</div>

<div class="section-card">
  <h3 class="section-title">Key Capabilities</h3>

  <div class="grid">
    <div>Interactive Segmentation<br><small>Meta SAM2 mask prediction</small></div>
    <div>Multi-object Selection<br><small>Bounding-box based selection</small></div>
    <div>Composite Masking<br><small>Combines multiple selected masks</small></div>
    <div>Occlusion-aware Insertion<br><small>Places source behind target objects</small></div>
    <div>Image Blending<br><small>OpenCV interpolation-based blending</small></div>
    <div>User-friendly Workflow<br><small>Reduced manual parameter tuning</small></div>
  </div>
</div>

<div class="section-card">
  <h3 class="section-title">Technologies & Design Choices</h3>

  <ul>
    <li><strong>Meta SAM2</strong> for image segmentation</li>
    <li><strong>Mask Predictor</strong> was chosen over Automatic Mask Detector because the automatic detector segmented too many objects and forced excessive user choice</li>
    <li><strong>Bounding-box selection</strong> was preferred because it allowed a user to select multiple objects more intuitively</li>
    <li><strong>Jupyter BBox Widget</strong> enabled interactive multi-object selection</li>
    <li><strong>OpenCV linear interpolation</strong> was selected for blending</li>
  </ul>
</div>

<!--
    <div class="section-card">
      <h3 class="section-title">Why These Choices Mattered</h3>
    
      <ul>
        <li><strong>Automatic Mask Detection</strong> was rejected because it segmented every visible object separately, which increased user effort</li>
        <li><strong>SAM2 Mask Predictor with one click</strong> still required users to choose among multiple mask score options</li>
        <li><strong>SAM2 + bounding boxes</strong> solved that by letting users deliberately choose the desired object(s)</li>
        <li><strong>Multiple bounding boxes</strong> enabled the system to create separate masks and combine them into a composite mask</li>
      </ul>
    </div>
-->

<div class="section-card">
  <h3 class="section-title">Core Technical Insight</h3>

  <p>
    A central idea in the project was:
  </p>

  <p>
    <strong>Final Mask = Source Mask − Target Mask</strong>
  </p>

  <p>
    This allowed the inserted source subject to appear behind selected target objects, which was necessary for more realistic compositing. 
  </p>
</div>

<div class="section-card">
  <h3 class="section-title">Challenges Encountered</h3>

  <ul>
    <li><strong>Blending with <code>cv2.seamlessClone</code></strong> produced unpredictable positioning because the center was inferred from mask geometry rather than intended image placement</li>
    <li><strong>Incorrect blending artifacts</strong> included ghosting, excess source background, and darkening of the target or source subject</li>
    <li><strong>Composite mask tuning</strong> required refinement where source and target masks intersected</li>
    <li><strong>Mask resizing</strong> caused further issues, so the solution kept original image sizes and only reduced display size for easier box drawing</li>
    <li><strong>GPU cost</strong> limited exploration of larger SAM2 variants</li>
    <li><strong>Image quality constraints</strong> came from relying on free stock images with stamps and imperfect resolution</li>
  </ul>
</div>


<!--
    <div class="section-card">
      <h3 class="section-title">Scenarios & Results</h3>
    
      <ul>
        <li>Solid background insertion</li>
        <li>Solid background with two source objects</li>
        <li>Classroom setting with partial occlusion</li>
        <li>Studio setting with foreground objects</li>
        <li>Office group setting</li>
      </ul>
    </div>
    
    <div class="section-card">
      <h3 class="section-title">Why this project matters</h3>
    
      <ul>
        <li>Shows how user experience constraints shape technical choices in computer vision systems</li>
        <li>Demonstrates system thinking across segmentation, interaction design, mask logic, and blending</li>
        <li>Highlights tradeoffs between automation and controllability</li>
        <li>Treats image synthesis as a pipeline problem, not just a model problem</li>
      </ul>
    </div>
-->
<div class="section-card">
  <h3 class="section-title">Tech Stack</h3>

  <p>
    <span class="highlight">Python</span>
    <span class="highlight">Meta SAM2</span>
    <span class="highlight">Jupyter BBox Widget</span>
    <span class="highlight">OpenCV</span>
    <span class="highlight">Google Colab</span>
  </p>
</div>


<br>


