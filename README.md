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

- Apply supervised Machine Learning to student data.
- Predict student outcomes as Pass or Fail.
- Implement multiple classification algorithms.
- Compare the performance of different models.
- Evaluate models using multiple metrics.
- Use 5-Fold Cross-Validation.
- Analyze predictions using confusion matrices.
- Identify True Positive, True Negative, False Positive, and False Negative predictions.
- Discuss limitations and ethical considerations of student outcome prediction.

---

## 📊 Dataset

The dataset contains anonymized/synthetic student information.

### Features

| Feature | Description |
|---|---|
| Attendance | Student attendance percentage |
| Study_Hours | Average study hours |
| Assignment_Submission | Whether assignments are submitted |
| Previous_Marks | Previous academic marks |
| Projects_Completed | Number of completed projects |
| Communication_Skills | Communication skill score |
| Aptitude_Score | Aptitude test score |
| Internet_Access | Availability of internet access |
| Family_Support | Availability of family support |
| Sleep_Hours | Average sleep hours |

### Target Variable

The target variable is **Outcome**:

- `Pass = 1`
- `Fail = 0`

`Student_ID` is excluded from model training because it is only an identifier.

---

## 🤖 Machine Learning Algorithms

Four supervised classification algorithms are implemented.

### 1. Logistic Regression

Logistic Regression is a classification algorithm used to estimate the probability of an observation belonging to a particular class.

**Advantages:**
- Simple and fast
- Easy to interpret
- Suitable for binary classification
- Useful as a baseline model

---

### 2. K-Nearest Neighbors (KNN)

KNN predicts the class of a new observation based on the classes of its nearest neighboring observations.

The project uses:

```text
K = 5
