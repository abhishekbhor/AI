# AI - Product
My current focus is creating AI products that integrate seamlessly into workflow ecosystems—LLM agents, intelligent recommendations, automated decisioning, and hybrid human-in-the-loop systems that improve accuracy, reduce friction, and scale safely. I’m particularly interested in opportunities at the intersection of AI systems, platform modernization, and healthcare or mission-critical operations.

### Education
- M.S., Artificial Intelligence - University of Pennsylvania (Upenn)
- M.S., Computer Science - University of Pennsylvania (Upenn)
- M.S., Architecture - Texas A&M University (TAMU)

### Work Experience
- Led end-to-end development of AI-enabled workflow products, from concept exploration through launch, adoption, and scale, supporting 50K+ users across 5K organizations.
- Designed AI-assisted agent-like workflows for documentation review, coding prioritization, and case targeting—reducing manual effort while preserving clinical intent and compliance.
- Defined product strategy and multi-year roadmaps focused on embedding AI into clinician-adjacent workflows, reducing administrative burden and improving throughput, accuracy, and downstream revenue outcomes.

### Projects
#### Field Agent Portal & Provider Affiliation Automation
#### Enterprise Data Warehouse Cloud Migration, Databricks Lakehouse


<h3>
 <a href="https://medium.com/@nkoro/heart-health-education-is-there-something-were-missing-ee41292c7729">
 Big Data Analysis & Prediction</a>
 </h3>

 <a href="https://medium.com/@nkoro/heart-health-education-is-there-something-were-missing-ee41292c7729"> 
 <img src="assets/img/heart-health-image.png"></a>

 <p>The study used machine learning models like Random Forest and oversampling techniques (SMOTE) to analyze 2022 CDC data and identify key predictors of heart attacks. It concluded that while age and angina are primary factors, unexpected variables like dental health (removed teeth) also significantly influence heart attack probability.</p>

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

