# AI - Product Portfolio
My current focus is creating AI products that integrate seamlessly into workflow ecosystems—LLM agents, intelligent recommendations, automated decisioning, and hybrid human-in-the-loop systems that improve accuracy, reduce friction, and scale safely. I’m particularly interested in opportunities at the intersection of AI systems, platform modernization, and healthcare or mission-critical operations.

### Education
- M.S., Artificial Intelligence - University of Pennsylvania (Upenn)
- M.S., Computer Science - University of Pennsylvania (Upenn)
- M.S., Architecture - Texas A&M University (TAMU)


## Projects

<div style="border: 2px solid blue; background-color: lightblue; padding: 4px;">
<h3>
 <span style="color: #507d2a;">I. RAG Assistant</span>
 </h3>
 <h4>A LLM-powered Retrieval System</h4>

<p>A modular Retrieval-Augmented Generation (RAG) system designed to simulate real-world AI product architecture — combining search, ranking, observability, caching, and feedback-driven improvement.</p>

<p>This project demonstrates how LLM systems move beyond simple prompts into production-style pipelines with measurable performance and iterative learning.</p>
<b>1. Key Capabilities</b>
- <b>Hybrid Retrieval</b>
-- Combines semantic search (FAISS) + keyword search (BM25)

- <b>Reranking Layer</b>: Improves relevance before generation

- <b>LLM Answer Generation</b>: Context-aware responses using retrieved chunks

- <b>Observability & Metrics</b>: Latency tracking across pipeline stages, 
Retrieval diagnostics (scores, ranking signals)

- <b>Caching Layer</b>: Reduces repeated query latency (milliseconds vs seconds)

- <b>Feedback Loop</b>: User ratings influence future ranking decisions

- <b>Evaluation Framework</b>: Measures answer quality and retrieval performance



<b>2. System is built to answer:</b>
- How do we measure retrieval quality?

- How do we optimize latency vs accuracy?

- How do we improve results over time using feedback?

- What does a production-ready LLM pipeline look like?

<b>3. System Design Highlights</b>
- Clear separation of: ingestion pipeline, retrieval pipeline, generation layer
- Provider abstraction (OpenAI-ready, extensible)

- Modular architecture for scaling and experimentation

- Built with system thinking over scripts


<b>4. Project Links</b>
- Full System (Code + Architecture + Metrics) : <a href="https://github.com/abhishekbhor/rag-assistant">https://github.com/abhishekbhor/rag-assistant</a>
- System Documentation / Deep Dive : <a href="https://github.com/abhishekbhor/rag-assistant/blob/main/README.md">https://github.com/abhishekbhor/rag-assistant/blob/main/README.md</a>


<b>5. Tech Stack</b>
- Python, FastAPI
- FAISS (vector search)
- BM25 (keyword retrieval)
- OpenAI APIs
- Custom observability + caching layers


</div>
<br>

<!-- <hr style="border: none; border-top: 1px dotted grey;">

<br> -->


<div style="border: 2px solid blue;">
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

