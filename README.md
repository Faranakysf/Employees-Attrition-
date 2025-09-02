### Employee Attrition: Initial Report and Exploratory Data Analysis


**Faranak Yousefi**

#### Executive summary
This project analyzes factors driving employee attrition, employing EDA and machine learning classification models. Key findings reveal overtime, low job satisfaction, and commute distance as primary predictors, with a tuned VotingClassifier ensemble outperforming individual models. Insights enable targeted HR interventions to reduce turnover, potentially saving costs in recruitment and productivity.
#### Rationale
Employee attrition imposes high costs on organizations, including recruitment, training, and lost knowledge. Understanding predictors allows proactive retention strategies, improving morale, productivity, and financial outcomes. This analysis is crucial for HR leaders to foster stable workforces in competitive markets.

#### Research Question
What are the primary factors influencing employee attrition in a company, and how do they contribute to predicting turnover?

#### Data Sources
The IBM HR Analytics Employee Attrition & Performance dataset https://ieee-dataport.org/documents/ibm-hr-analytics-employee-attrition-performance, containing 1470 records with 35 features like Age, JobSatisfaction, MonthlyIncome, OverTime, and binary Attrition.

#### Methodology
Exploratory Data Analysis (EDA) using Pandas for data cleaning (outlier capping, constant column removal), Matplotlib/Seaborn for visualizations (boxplots, countplots, heatmaps) to identify distributions and correlations. Feature engineering included AgeGroup binning and TenureRatio. Modeling used Logistic Regression (baseline), Decision Tree, KNN, SVM, with SMOTE for imbalance handling. Ensemble via tuned VotingClassifier (soft voting, GridSearchCV on hyperparameters). Evaluation via F1-score and AUC-ROC due to imbalance; permutation importance for feature insights.

#### Results
EDA showed attrition linked to younger age, lower satisfaction/income, overtime, sales roles, and single status. Baseline Logistic Regression: F1 0.89, AUC 0.92. Tuned ensemble: F1 0.92, AUC 0.92, outperforming best individual (Decision Tree F1 0.91), confirming ensemble benefits. Top features: OverTime_Yes (0.037 importance), Department_Sales (0.017), BusinessTravel_Frequently (0.017), low JobInvolvement (0.016), JobRole_Human Resources (0.016).

#### Next steps
Incorporate advanced ensembles like RandomForest or GradientBoosting for better nonlinearity capture. Use SHAP for detailed feature interactions. Validate the results and develop a model for real-time predictions and interventions.

#### Outline of project

- [Link to notebook](Employee Attrition.ipynb)
- [Link to dataset](data/WA_Fn-UseC_-HR-Employee-Attrition.csv)
- [Link to images](images)


##### Contact and Further Information
Send me a message for furtuther information.
