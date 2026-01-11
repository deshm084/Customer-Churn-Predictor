# 📉 Telco Customer Churn Prediction

A Machine Learning project that predicts which customers are likely to leave a service (churn). It identifies key indicators of churn to help businesses take proactive retention actions.

## 💼 The Business Problem
Customer Acquisition Cost (CAC) is often 5x higher than Customer Retention Cost. 
**Goal:** Identify high-risk customers *before* they leave so the marketing team can intervene.

## 🛠 Tech Stack
* **Python** (Pandas, NumPy)
* **Scikit-Learn** (Random Forest Classifier)
* **Imbalanced-learn** (SMOTE)
* **Seaborn** (Visualization)

## 🧠 Key Challenge: Class Imbalance
Real-world churn data is heavily imbalanced (e.g., 80% stay, 20% leave).
* **The Problem:** Standard models bias towards the majority class (predicting "Stay" for everyone).
* **The Solution:** I implemented **SMOTE (Synthetic Minority Over-sampling Technique)**. This generates synthetic examples of churners in the training data to create a 50/50 balance, forcing the model to learn the characteristics of churners effectively.

## 📊 Results
* **Accuracy:** ~79% (on unseen test data)
* **Recall (Churners):** High recall ensures we catch most potential churners, even if it means a few false alarms (better safe than sorry).

## 🔍 Top Drivers of Churn
The Random Forest model identified the following as the strongest predictors of a customer leaving:
1.  **Contract Type:** (Month-to-month customers churn significantly more).
2.  **Monthly Charges:** (Higher bills correlate with higher churn).
3.  **Tenure:** (New customers are the most fragile).

## 🚀 Usage
Run the notebook to load the IBM Telco dataset, train the model, and view the feature importance report.
