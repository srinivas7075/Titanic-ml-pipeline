📘 End-to-End Machine Learning Pipeline — Titanic Survival Prediction

A complete end-to-end Machine Learning Pipeline built using the Titanic dataset.
This project demonstrates the full ML workflow including:

✔ Data Cleaning
✔ Exploratory Data Analysis (EDA)
✔ Feature Engineering
✔ Model Training
✔ Model Evaluation
✔ Final Model Selection
📦 Dataset
-------------------------------------------------------
📦 Dataset

Source: KaggleHub → yasserh/titanic-dataset

File Used: Titanic-Dataset.csv

Rows: 891

Columns: 12

Target variable: Survived (0 = died, 1 = survived)

🧹 Data Cleaning
-------------------------------------------------------


Performed the following steps:

✔ Missing Value Handling

Age → median imputation

Embarked → mode imputation

Cabin → deck extraction → missing → 'U'

✔ Outlier Treatment

Applied IQR method to Age and Fare.

✔ Data Type Fixing

Converted Pclass, Sex, Embarked, and Deck to categorical types.

✔ Duplicate Removal

No duplicates found.

📊 Exploratory Data Analysis (EDA)
---------------------------------------------------------


Generated visualizations including:

Age Distribution

Fare Distribution by Class

Survival Counts by Gender

Survival by Embarked Port

Age vs Fare Scatter

Correlation Heatmap

Deck Distribution

🔍 Key Insights
---------------------------------------------------------


Female passengers had much higher survival rates than males.

Higher passenger class (1st class) correlated strongly with survival.

Higher fare values associated with higher survival.

Age had a weak negative relationship with survival.

Family-based features such as FamilySize influenced survival patterns.

🛠 Feature Engineering
---------------------------------------------------------


Created multiple high-impact features:

✔ Encoded Features

Sex_enc (Label Encoding)

One-hot encoding for:

Embarked (Embarked_Q, Embarked_S)

Pclass (Pclass_2, Pclass_3)

Deck (Deck A, B, C, D, E, F, G, T, U)

✔ New Features

FamilySize

IsAlone

Title extraction from Name (mapped rare titles)

Title_enc

✔ Scaling

Age_s and Fare_s using StandardScaler

🤖 Model Training
-------------------------------------------------------

Two models were trained:

1️⃣ Logistic Regression

Best performance

Great baseline model

Low variance, stable metrics

2️⃣ Random Forest

Good model, but slightly lower performance in this dataset

📈 Model Evaluation
------------------------------------------------------------
Logistic Regression

Accuracy: 0.8156

Precision: 0.8000

Recall: 0.6957

F1-score: 0.7442

ROC-AUC: 0.8365

Random Forest

Accuracy: 0.7877

Precision: 0.7385

Recall: 0.6957

F1-score: 0.7164

ROC-AUC: 0.8319

🎯 Final Model Chosen:
-----------------------------------------------------

⭐ Logistic Regression — best performance across multiple metrics.
-------------------------------------------------------

🎓 Learnings & Challenges

Handling high missingness in Cabin by extracting deck information helped preserve useful patterns.

Feature engineering (especially Title extraction and FamilySize) significantly improved model performance.

Logistic Regression performed better than Random Forest due to dataset structure and linear separability.

Maintaining consistent preprocessing between training and inference is crucial for deployment.








