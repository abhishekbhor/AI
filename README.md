<style>
.section-card {
  border: 1px solid #e1e4e8;
  border-radius: 8px;
  padding: 20px;
  margin: 20px 0;
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

### Education
- M.S., Artificial Intelligence - University of Pennsylvania (Upenn)
- M.S., Computer Science - University of Pennsylvania (Upenn)

<br>
<br>

## Projects

<h3><span style="color: #507d2a;">I. RAG Assistant (LLM-powered Retrieval System)</span></h3>

<div class="section-card">
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

<div class="section-card">
<!-- <div style="border: thin solid lightgray; background-color: none; padding: 10px 5px 10px;"> -->
<h3>
 <span style="color: #507d2a;">I. RAG Assistant (LLM-powered Retrieval System)</span>
 </h3>
 
<p>
A modular <strong>Retrieval-Augmented Generation (RAG) system</strong> designed to simulate real-world AI product architecture — combining search, ranking, observability, caching, and feedback-driven improvement.
</p>

<h4 class="section-title">Key Capabilities</h4>
<ul>
  <li style="margin-bottom: 0; margin-top: 0;"><strong>Hybrid Retrieval</strong>: Combines semantic search (FAISS) + keyword search (BM25)
  </li>

  <li style="margin-bottom: 0; margin-top: 0;"><strong>Reranking Layer</strong>: Improves relevance before generation
  </li>

  <li style="margin-bottom: 0; margin-top: 0;"><strong>LLM Answer Generation</strong>: <strong>Context-aware</strong> responses using retrieved <strong>chunks</strong>
  </li>

  <li style="margin-bottom: 0; margin-top: 0;"><strong>Observability & Metrics</strong>: <strong>Latency tracking </strong> across pipeline stages, Retrieval diagnostics (scores, ranking signals)
  </li>

  <li style="margin-bottom: 0; margin-top: 0;"><strong>Caching Layer</strong>: Reduces repeated query latency (milliseconds vs seconds)
  </li>

  <li style="margin-bottom: 0; margin-top: 0;"><strong>Feedback Loop</strong>: User ratings influence future ranking decisions
  </li>

  <li style="margin-bottom: 0; margin-top: 0;"><strong>Evaluation Framework</strong>: Measures answer quality and retrieval performance
  </li>
</ul>

<h4>System Design Highlights</h4>

<ul>
  <li>Clear separation of: <strong>Ingestion pipeline</strong>, <strong>Retrieval pipeline</strong>, <strong>Generation layer</strong>  </li>
  <li>Provider abstraction (OpenAI-ready, extensible)</li>
  <li><strong>Modular architecture</strong> for scaling and experimentation</li>
  <li>Built with <strong>system thinking</strong> over scripts</li>
</ul>


<h4>Tech Stack</h4>

<ul>
  <li>Python, FastAPI</li>
  <li>FAISS (vector search)</li>
  <li>BM25 (keyword retrieval)</li>
  <li>OpenAI APIs</li>
  <li>Custom observability + caching layers</li>
</ul>

<h4>Project Links</h4>

<ul>
 <li><strong>Full System (Code + Architecture + Metrics):</strong><br>
  <a href="https://github.com/abhishekbhor/rag-assistant" target="_blank">
  https://github.com/abhishekbhor/rag-assistant
 </a></li>

<li><strong>System Documentation / Deep Dive:</strong><br>
<a href="https://github.com/abhishekbhor/rag-assistant/blob/main/README.md" target="_blank">
https://github.com/abhishekbhor/rag-assistant/blob/main/README.md
</a>
 </li>
</ul>

</div>

<hr>
<br>

<!-- <hr style="border: none; border-top: 1px dotted grey;">

<br> -->


<div style="border: thin solid lightgray; background-color: none; padding: 5px;">
<h3>
 <span style="color: #507d2a;">II. Big Data Analysis & Prediction</span>
 </h3>
 <h4>Indicators of Heart Disease</h4>

 <a href="https://medium.com/@nkoro/heart-health-education-is-there-something-were-missing-ee41292c7729"> 
 <img src="assets/img/heart-health-image.png"></a>

 <p><a href="https://medium.com/@nkoro/heart-health-education-is-there-something-were-missing-ee41292c7729">The study</a> used machine learning models like Random Forest and oversampling techniques (SMOTE) to analyze 2022 CDC data and identify key predictors of heart attacks. It concluded that while age and angina are primary factors, unexpected variables like dental health (removed teeth) also significantly influence heart attack probability.</p>

<b>1. Programming & Libraries</b>
- <b>Python</b>: The primary programming language used for the study.

- <b>SciKit-Learn (sklearn)</b>: Used for building, training, and evaluating the machine learning models.

- <b>Pandas & NumPy</b>: Utilized for data wrangling, cleaning (dropping nulls/duplicates), and data manipulation.

- <b>Matplotlib & Seaborn</b>: Used for Exploratory Data Analysis (EDA) to create visualizations like correlation heatmaps, bar charts, and dendrograms.

<b>2. Machine Learning Models</b>
- The team tested multiple classification algorithms to determine the best predictor for heart attacks:

- <b>Logistic Regression</b>: Used as the baseline model.

- <b>Decision Tree Classifier</b>: Improved accuracy and recall over the baseline.

- <b>Random Forest Classifier</b>: Identified as the most robust model with an AUC score of 0.99 and 97% accuracy.

<b>3. Data Engineering & Analytics Techniques</b>
- <b>SMOTE (Synthetic Minority Oversampling Technique)</b>: A critical tool used to handle the "imbalanced dataset" problem (where heart attack cases were much rarer than non-cases). It created synthetic data points to balance the classes.

- <b>Feature Engineering</b>: * One-Hot Encoding & Label Encoding: Used to convert categorical strings (like RaceEthnicityCategory or SmokerStatus) into numerical data for the models.

- <b>Dendrograms</b>: Used for hierarchical clustering to identify and remove highly correlated (redundant) features.

- <b>Evaluation Metrics</b>: The study relied on Confusion Matrices, Recall, Precision, F1 Score, and ROC/AUC Curves to validate the models.

<b>4. Data Source</b>
2022 CDC Annual Survey: Specifically the "Key Indicators of Heart Disease" dataset, which provided the raw data for the 40+ variables analyzed in the study.
</div>
<br>

<!-- <hr style="border: none; border-top: 1px dotted grey;">

<br> -->
<h3>
 <span style="color: #507d2a;">III. Multi-Modal Image Synthesis & Semantic Segmentation</span>
</h3>
 
 <img src="assets/img/comp-vision.png">

<p>Created an app where I engineered a computer vision pipeline utilizing Mask R-CNN for image segmentation and Pose Estimation algorithms to seamlessly integrate dynamic objects into complex environments, optimizing for spatial consistency and blending.</p>

<b>1. Image Segmentation</b> with <b>Meta's SAM2</b>
- <b> Predictor Mask</b> : The Predictor Mask allowed user to select their object to create mask. Didn’t use 'Automatic Mask Detector' because it was segmenting every object in the picture.
User had to try and select, which configuration to use for final mask. 

<b>2. Pose Adjustment</b> with <b>ChatPose</b>
- Researched analyzed, and didn't use as integration with Google Colab was found tricky.

<b>3. Blending Algorithms</b>
- <b>OpenCV Linear Interpolation</b> Analyzed Adobe Unihuman, Stable Diffusion & Impainting and CV2 seamlessClone, but didn't use.

<b>4. Object Selection</b>
- <b>Jupyter BBox Widget</b>

