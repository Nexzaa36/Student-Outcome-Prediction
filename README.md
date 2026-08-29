# Interpretable Student Outcome Prediction Using Multiple Supervised Models

## 📌 Project Overview

This project focuses on predicting student academic outcomes using Machine Learning classification algorithms.

The objective is to predict whether a student is likely to **Pass or Fail** based on academic and behavioral features such as attendance, study hours, previous marks, assignment submission, projects completed, aptitude score, communication skills, internet access, family support, and sleep hours.

Multiple supervised Machine Learning models are trained and compared to determine their performance.

The project also focuses on **model evaluation, interpretability, and ethical considerations** rather than relying only on accuracy.

---

## 🎯 Problem Statement

To develop a supervised Machine Learning classification system that predicts whether a student is likely to **Pass or Fail** based on academic and behavioral features.

The project compares multiple classification algorithms and evaluates them using appropriate performance metrics and confusion matrices.

---

## 🎯 Objectives

* Apply supervised Machine Learning to student data.
* Predict student outcomes as Pass or Fail.
* Implement multiple classification algorithms.
* Compare the performance of different models.
* Evaluate models using multiple metrics.
* Use 5-Fold Cross-Validation.
* Analyze predictions using confusion matrices.
* Identify True Positive, True Negative, False Positive, and False Negative predictions.
* Discuss limitations and ethical considerations of student outcome prediction.

---

## 📊 Dataset

The dataset contains anonymized/synthetic student information.

### Features

| Feature               | Description                       |
| --------------------- | --------------------------------- |
| Attendance            | Student attendance percentage     |
| Study_Hours           | Average study hours               |
| Assignment_Submission | Whether assignments are submitted |
| Previous_Marks        | Previous academic marks           |
| Projects_Completed    | Number of completed projects      |
| Communication_Skills  | Communication skill score         |
| Aptitude_Score        | Aptitude test score               |
| Internet_Access       | Availability of internet access   |
| Family_Support        | Availability of family support    |
| Sleep_Hours           | Average sleep hours               |

### Target Variable

The target variable is **Outcome**:

* `Pass = 1`
* `Fail = 0`

`Student_ID` is excluded from model training because it is only an identifier.

---

## 🤖 Machine Learning Algorithms

Four supervised classification algorithms are implemented.

### 1. Logistic Regression

Logistic Regression is a classification algorithm used to estimate the probability of an observation belonging to a particular class.

**Advantages:**

* Simple and fast
* Easy to interpret
* Suitable for binary classification
* Useful as a baseline model

---

### 2. K-Nearest Neighbors (KNN)

KNN predicts the class of a new observation based on the classes of its nearest neighboring observations.

The project uses:

```text
K = 5
```

**Advantages:**

* Simple to understand
* Easy to implement
* Can model nonlinear relationships

---

### 3. Support Vector Machine (SVM)

SVM attempts to find an effective decision boundary that separates different classes.

The project uses the **RBF kernel**.

```text
Kernel = RBF
```

**Advantages:**

* Effective for classification
* Can handle nonlinear relationships
* Performs well with properly scaled data

---

### 4. Decision Tree

Decision Tree makes predictions by repeatedly splitting data according to feature values.

The project uses:

```text
Maximum Depth = 5
```

This helps control model complexity and reduce overfitting.

**Advantages:**

* Easy to understand
* Does not require feature scaling
* Can model nonlinear relationships
* Provides interpretable feature-based decisions

---

## ⚙️ Machine Learning Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Exploration
   ↓
Data Preprocessing
   ↓
Categorical Encoding
   ↓
Train-Test Split
   ↓
Feature Scaling
   ↓
Model Training
   ↓
Predictions
   ↓
Model Evaluation
   ↓
Model Comparison
   ↓
Confusion Matrix
   ↓
TP / TN / FP / FN Analysis
   ↓
Best Model Selection
```

---

## 📏 Evaluation Metrics

The models are evaluated using multiple metrics.

### Accuracy

Measures the percentage of total predictions that the model classified correctly.

```text
Accuracy = (TP + TN) / (TP + TN + FP + FN)
```

### Precision

Measures how many predicted positive cases are actually positive.

```text
Precision = TP / (TP + FP)
```

### Recall

Measures how many actual positive cases were correctly identified.

```text
Recall = TP / (TP + FN)
```

### F1 Score

The harmonic mean of Precision and Recall.

```text
F1 Score = 2 × (Precision × Recall) / (Precision + Recall)
```

### Cross-Validation

The project uses **5-Fold Cross-Validation** to estimate how well the models generalize to unseen data.

---

## 📉 Confusion Matrix

A confusion matrix is used to understand correct and incorrect predictions.

|                 | Predicted Fail | Predicted Pass |
| --------------- | -------------: | -------------: |
| **Actual Fail** |             TN |             FP |
| **Actual Pass** |             FN |             TP |

### True Positive (TP)

The model predicts **Pass**, and the student actually **passes**.

### True Negative (TN)

The model predicts **Fail**, and the student actually **fails**.

### False Positive (FP)

The model predicts **Pass**, but the student actually **fails**.

This could result in a student who needs academic support not being identified.

### False Negative (FN)

The model predicts **Fail**, but the student actually **passes**.

This could result in unnecessary academic intervention.

Therefore, accuracy alone is not sufficient for evaluating the model.

---

## 🛠️ Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Joblib

### Development Environment

* JupyterLab
* Jupyter Notebook

### Data Format

* CSV

---

## 📁 Project Structure

```text
Student-Outcome-Prediction/
│
├── dataset/
│   └── student_data.csv
│
├── images/
│   └── confusion_matrices.png
│
├── models/
│   ├── scaler.pkl
│   ├── logistic_model.pkl
│   ├── knn_model.pkl
│   ├── svm_model.pkl
│   └── decision_tree_model.pkl
│
├── reports/
│   └── model_comparison.csv
│
├── notebooks/
│   └── Student_Outcome_Prediction.ipynb
│
└── README.md
```

---

## 📊 Model Comparison

The project compares all four models using:

* Accuracy
* Precision
* Recall
* F1 Score
* 5-Fold Cross-Validation

The final model comparison is stored in:

```text
reports/model_comparison.csv
```

The model with the strongest overall performance can then be selected based on the evaluation results.

---

## 📈 Results

The final notebook generates a model comparison table containing the performance of all four algorithms.

| Model               | Accuracy | Precision | Recall | F1 Score | CV Mean |
| ------------------- | -------: | --------: | -----: | -------: | ------: |
| Logistic Regression |        - |         - |      - |        - |       - |
| KNN                 |        - |         - |      - |        - |       - |
| SVM                 |        - |         - |      - |        - |       - |
| Decision Tree       |        - |         - |      - |        - |       - |

> The values are generated automatically when the notebook is executed.

---

## 🧠 Interpretability

The project focuses on understanding model predictions rather than reporting accuracy alone.

Confusion matrices are used to analyze:

* True Positives
* True Negatives
* False Positives
* False Negatives

This helps understand the types of mistakes made by each classification model.

---

## ⚠️ Limitations

* The dataset is synthetic and may not fully represent real-world student behavior.
* Student performance can depend on many factors that are not included in the dataset.
* Factors such as motivation, stress, health, personal circumstances, and learning environment are not represented.
* Model performance may change when applied to a different dataset.
* Predictions should not be considered completely accurate or deterministic.

---

## 🔐 Ethical Considerations

Student prediction systems involve educational information and should be used responsibly.

### Privacy

Student information should be anonymized and securely stored.

### Bias

Machine Learning models can learn biases present in the training data. Model performance should therefore be monitored for unfair outcomes.

### Fairness

Predictions should not be used to discriminate against students based on their circumstances.

### Human Oversight

The model should be used as a **decision-support tool**, not as a replacement for teachers or academic authorities.

### Responsible Use

A prediction of Fail should not automatically result in punishment or negative academic consequences. Instead, it can be used to identify students who may benefit from additional support.

---

## 📄 Model Card

The project includes a Model Card describing:

* Model purpose
* Dataset
* Input features
* Target variable
* Algorithms used
* Evaluation metrics
* Intended use
* Limitations
* Ethical considerations

---

## 📚 Reference Sources

1. Aurélien Géron, *Hands-On Machine Learning with Scikit-Learn, Keras and TensorFlow*, 3rd Edition.
2. Christopher M. Bishop, *Pattern Recognition and Machine Learning*.
3. Trevor Hastie, Robert Tibshirani, and Jerome Friedman, *The Elements of Statistical Learning*.

---

## 🎓 Academic Information

**Project Title:**
Interpretable Student Outcome Prediction Using Multiple Supervised Models

**Domain:**
Data Science / Machine Learning

**Machine Learning Type:**
Supervised Learning

**Problem Type:**
Binary Classification

**Target:**
Student Pass/Fail Outcome

**Algorithms:**
Logistic Regression, KNN, SVM, Decision Tree

**Evaluation:**
Accuracy, Precision, Recall, F1 Score, 5-Fold Cross-Validation, Confusion Matrix

**Development Environment:**
JupyterLab

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Open the Project

```bash
cd Student-Outcome-Prediction
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib scikit-learn joblib jupyterlab
```

### 4. Start JupyterLab

```bash
jupyter lab
```

### 5. Open the Notebook

Navigate to:

```text
notebooks/Student_Outcome_Prediction.ipynb
```

Run the notebook cells sequentially.

---

## 📌 Conclusion

This project demonstrates how supervised Machine Learning can be applied to predict student outcomes using multiple classification algorithms.

By comparing Logistic Regression, KNN, SVM, and Decision Tree using multiple evaluation metrics and confusion matrices, the project provides a broader understanding of model performance.

The project also highlights that Machine Learning predictions should be interpreted carefully and used responsibly, especially when they involve decisions related to students.

---

## 👨‍💻 Author

**Ayush Joshi**

BCA – Data Science / Machine Learning Project
