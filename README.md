# LendingClub



Project Overview
Lending Club is seeking the expertise of a data science consultant
to perform comprehensive data cleaning, exploratory data
analysis (EDA), and predictive modeling on their loan application
dataset. The project will also explore the potential for deploying 
a real-time scoring application. The primary objective is to prepare
the dataset for accurate analysis and modeling, understand the
key variables influencing loan approval, and recommend a
predictive model for classifying loan applications.



📝 Loan Default Prediction — Project Report

📌 Methodology & Approach

1. Objective
To predict the likelihood of loan default based on historical LendingClub data, enabling financial institutions to better assess credit risk.

2. Methodology Overview
Data Cleaning & Preprocessing
Dropped columns with >80% missing values
Imputed missing numeric fields with median
Encoded categorical variables with LabelEncoder
Engineered datetime features (year, month, quarter, etc.)
Applied log transformation to highly skewed features
Scaled features using StandardScaler
Addressed class imbalance using SMOTE
Exploratory Data Analysis (EDA)
Analyzed target distribution and skew
Visualized variable interactions with target
Conducted statistical tests (T-test, Chi-square)
Assessed multicollinearity with correlation heatmap
Modeling
Baseline model: LogisticRegression(class_weight='balanced')
Challenger model: XGBClassifier(scale_pos_weight=ratio)
Evaluated with F1-score, Precision, Recall, and ROC-AUC


🤖 Model Selection Rationale

Baseline: Logistic Regression
Simple, interpretable, fast to train
Handles class imbalance natively via class_weight
Useful benchmark for comparison
Challenger: XGBoost
Handles large, high-dimensional datasets efficiently
Captures nonlinear relationships
Regularization helps prevent overfitting
Supports imbalance with scale_pos_weight
Achieved near-perfect classification performance after SMOTE
✅ Advantages and Limitations

Aspect	XGBoost Classifier
✅ High accuracy	✔ Excellent recall and precision after SMOTE
✅ Feature importance	✔ Supports interpretability via importance plots
✅ Scalable	✔ Supports parallelism and large datasets
❌ Interpretability	Not as straightforward as logistic regression
❌ Training time	Heavier compared to linear models



🏗 Architecture of the Final Solution
![schema.png](assets%2Fschema.png)
             

