# 🔎 Modeling and Analysis

---

## 🛠️ Modeling Strategy

The overall strategy was to start with simple models (Regression), move to Classification models, explore unsupervised patterns (Clustering), and then apply more advanced ensemble models (Random Forest) to boost performance.

The dataset was divided into training and testing sets using an 80/20 split.

---

## 📈 Linear Regression

- **Goal:** Predict total score as a continuous variable based on academic and behavioral features.
- **Experiments:**
  - First feature set: Attendance, Midterm, Assignments Average, Study Hours, Stress Level.
  - Second feature set: Age, Final Score, Quizzes, Projects, Sleep Hours.
- **Results:**
  - R² scores were moderate, indicating poor separation between students.
  - Overlapping feature values caused regression to perform poorly.
- **Insight:**  
  Linear Regression struggled to distinguish grade boundaries, motivating a shift to classification models.

---

## 📈 Decision Tree Classifier

- **Goal:** Classify students into grade categories (A, B, C, etc.).
- **Preprocessing:** One-hot encoding applied, no scaling needed.
- **Initial Results:**
  - Overfitting observed: high training accuracy, lower testing accuracy.
- **Tuning:**  
  - Limited tree depth and minimum samples per split to reduce overfitting.
- **After Tuning:**
  - More balanced performance across classes, but still struggled at decision boundaries.
- **Insight:**  
  Decision Trees were interpretable but sensitive to noise and feature overlap.

---

## 📈 Support Vector Machine (SVM)

- **Goal:** Improve classification by handling feature overlap better.
- **Preprocessing:** Normalization applied to scaled features between 0–1.
- **Initial Results:**
  - Better boundary formation compared to Decision Tree.
- **Tuning:**
  - GridSearchCV was used to test different C values and kernels (linear vs. rbf).
  - Best model: RBF Kernel with C=1.
- **After Tuning:**
  - Increased test accuracy.
  - Improved class separation, especially between neighboring grades.
- **Insight:**  
  SVM handled overlapping features better and generalized well after scaling.

---

## 📈 KMeans Clustering

- **Goal:** Explore natural groupings in student behavior without using grade labels.
- **Preprocessing:** Normalized key behavioral features.
- **Method:**
  - Elbow Method used to determine optimal clusters.
  - Chose 4 clusters based on inertia curve.
- **Results:**
  - Identified behavior-based clusters, partially aligning with grade distributions.
- **Insight:**  
  Clustering provided unsupervised validation of performance patterns.

---

## 📈 Random Forest Classifier

- **Goal:** Build a more robust, generalized classification model.
- **Preprocessing:** One-hot encoding; no need for normalization.
- **Initial Results:**
  - Better accuracy than Decision Tree and SVM even before tuning.
- **Tuning:**
  - Optimized `n_estimators` to 150, `max_depth` to 12, `min_samples_split` to 4.
- **After Tuning:**
  - Highest overall accuracy across all models.
  - Reduced overfitting while maintaining strong classification performance.
- **Insight:**  
  Random Forest balanced bias and variance, capturing complex relationships in the data.

---

## 🧠 Final Model Comparison

| Model                  | Key Strength | Key Weakness |
|-------------------------|--------------|--------------|
| Linear Regression       | Simple baseline | Poor boundary separation |
| Decision Tree Classifier| Interpretable splits | Overfitting risk |
| Support Vector Machine  | Good boundary handling | Sensitive to scaling |
| KMeans Clustering       | Discovered behavior groups | No direct grade prediction |
| Random Forest Classifier| Highest accuracy, balanced generalization | Slower training time |

---

[⬅️ Back to Project Overview](README.md)
