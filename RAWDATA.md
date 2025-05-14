# 📦 Raw Data Description

## 📍 Data Source
- The dataset was obtained from [Kaggle - Student Performance Dataset](https://www.kaggle.com/datasets/mahmoudelhemaly/students-grading-dataset)  .  
- It was manually downloaded as a CSV file (`studentsgrade.csv`) and uploaded into the project environment.

## 📂 Data Overview
- **Format:** Comma-Separated Values (.csv)
- **Size:** Approximately 500 KB
- **Number of Records:** 5000 student entries
- **Initial Features Included:**
  - **Academic Features:** Midterm Score, Final Score, Assignments Average, Quizzes Score, Project Score
  - **Behavioral Features:** Attendance Percentage, Study Hours, Stress Level, Sleep Hours
  - **Demographic Features:** Gender, Department, Income Level, Internet Access, Parent Education Level

## 🛠️ Data Handling at Raw Stage
- The dataset was loaded into the environment using `pandas.read_csv`.
- No automated scraping, web APIs, or external database connections were used.
- Minor inconsistencies such as missing values were observed, but no changes were made at the raw data stage.

## 🧠 Initial Observations
- The raw dataset included a combination of **categorical** (e.g., Gender, Department) and **numerical** (e.g., Attendance, Final Score) features.
- No duplicate records were found during the initial inspection.
- Full cleaning, feature engineering, and transformations were conducted during the later preprocessing phase (described in `DATA.md`).

---

[⬅️ Back to Project Overview](README.md)
