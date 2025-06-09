# Autism Spectrum Disorder (ASD) Prediction 🧩

This project focuses on predicting Autism Spectrum Disorder (ASD) using a combination of binary screening questions and demographic/clinical features. The dataset includes 800 records, each representing an individual's answers to 10 behavioral questions (A1–A10), along with personal attributes such as age, gender, ethnicity, and clinical history (e.g., jaundice, family ASD). The goal is to build a classification model that can effectively detect potential ASD cases based on this input data.

## 🔍 Key Features

- Uses a real-world dataset containing demographic and clinical information for ASD screening.
- Performs data cleaning, handling of categorical features, and feature scaling.
- Evaluates model performance using metrics like accuracy, precision, recall, F1-score, and confusion matrix.
  
## 📊 Dataset Overview

The dataset consists of 800 entries, each representing an individual's response to an ASD screening test. Each record includes:

- **10 Binary Screening Questions (A1_Score to A10_Score):** Yes/No questions scored as 1 or 0, evaluating behavioral patterns associated with ASD.
- **Demographic Features:** Age, gender, ethnicity, country of residence.
- **Clinical History:** Jaundice at birth, family history of ASD, prior use of screening app.
- **Additional Features:** Result score, relationship of respondent, and age description.
- **Target Label:** `Class/ASD` (1 = likely ASD, 0 = not ASD).
  
## 🧪 Project Workflow

The main steps in this project are:

1. **Data Cleaning**
   - Removed irrelevant or redundant columns such as `ID` and `age_desc`.
   - Renamed columns for clarity.

2. **Preprocessing**
   - Handled missing values and inconsistent entries.
   - Encoded categorical features using label encoding and one-hot encoding.
   - Scaled numerical features.

4. **Modeling**
   - Applied Logistic Regression classifiers.
   - Used stratified train-test split to preserve class distribution.

5. **Evaluation**
   - Measured accuracy, precision, recall, and F1-score.
   - Displayed confusion matrix for a clearer understanding of false positives/negatives.
     
## 📈 Model Performance & Evaluation

The final model achieved the following performance on the test set:

| Metric       | Class 0 (Not ASD) | Class 1 (ASD) |
|--------------|------------------|---------------|
| Precision    | 0.95             | 0.52          |
| Recall       | 0.81             | 0.81          |
| F1-score     | 0.87             | 0.63          |
| Support      | 128              | 32            |

- **Overall Accuracy:** 81%
- **Macro Average F1-score:** 0.75
- **Weighted Average F1-score:** 0.83

🔍 Although the model performs well overall, precision for the ASD class is relatively low, meaning it produces some false positives. However, recall is high (81%), which is crucial in medical screening tasks where detecting true positives is more important than avoiding false alarms.
