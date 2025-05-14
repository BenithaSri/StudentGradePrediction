# 🎓 Student Grade Prediction Using Regression, Classification & Clustering

## 📌 Overview
This project investigates predicting student final grades using academic, behavioral, and demographic data.  
The goal is to uncover patterns in performance and evaluate which machine learning models best classify students for early academic intervention.

## 🎯 Objective
To build and compare regression, classification, and clustering models that analyze student performance.  
This includes understanding which features are most predictive, and how different modeling strategies perform under real-world feature overlap and variability.

## 🔍 Dataset
- **Source:** [Kaggle - Student Performance Dataset](https://www.kaggle.com/datasets/mahmoudelhemaly/students-grading-dataset)  
- **Records:** 5000 student data points  
- **Features include:**
  - Academic: Midterm, Final, Assignments, Quizzes, Project scores  
  - Behavioral: Attendance, Study Hours, Stress, Sleep  
  - Demographic: Gender, Department, Income, Internet Access

## 🧰 Techniques Used
- **Preprocessing:** One-hot encoding, normalization, missing value handling  
- **Models:**
  - Linear Regression  
  - Decision Tree Classifier  
  - Support Vector Machine (SVM)  
  - KMeans Clustering  
  - Random Forest Classifier  
- **Tuning:** GridSearchCV, depth limiting, parameter optimization  
- **Evaluation Metrics:** Accuracy, R², confusion matrix, elbow method

## 📊 Key Findings
- Linear Regression struggled due to overlapping features and non-linearity  
- Decision Tree was interpretable but overfit easily  
- SVM handled overlap better after normalization  
- KMeans revealed natural behavior-based groupings  
- Random Forest gave the highest and most balanced accuracy

## 🧠 Final Insight
While each model offered a unique lens into the data, classification models — especially Random Forest — proved most effective.  
Unsupervised clustering added valuable validation to the grade-label groupings, supporting real-world applicability in education analytics.


## 🔗 Project Files

- [Raw Data Description](RAW_DATA.md)  
- [Data Exploration and Cleaning](DATA.md)  
- [Modeling and Analysis](ANALYSIS.md)  
- [Conclusions and Future Work](CONCLUSIONS.md)
