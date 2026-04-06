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
   <h3 class="section-title" style="color:#507d2a;">I. RAG Assistant</h3>
  <h4>A LLM-powered Retrieval System</h4>
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
<hr>
<br>



<div class="section-card">
  <h3 class="section-title" style="color:#507d2a;">II. Big Data Analysis & Prediction</h3>
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







<br>
<hr>

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

