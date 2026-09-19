# Iris Flower Classification

## 📌 Project Overview

This project was completed as **Task 4** of my **Machine Learning Internship at Arch Technologies**.

The objective is to develop a machine learning classification system capable of predicting the species of an Iris flower from its physical measurements.

The project follows a complete machine learning workflow:

* Dataset loading
* Data exploration
* Data quality checking
* Exploratory Data Analysis (EDA)
* Feature selection
* Train-test splitting
* Feature scaling
* Model training
* Model comparison
* Classification evaluation
* Confusion matrix analysis
* Cross-validation
* Prediction probability analysis
* Model saving

---

## 📊 Dataset

**Dataset:** Iris Flower Dataset

**Source:** Kaggle – Iris Dataset

Dataset characteristics:

* **Rows:** 150
* **Columns:** 6
* **Missing values:** 0
* **Duplicate rows:** 0
* **Classes:** 3

### Target Classes

* `Iris-setosa`
* `Iris-versicolor`
* `Iris-virginica`

Each class contains **50 samples**.

---

## 🌸 Features

The following four measurements were used as input features:

* `SepalLengthCm`
* `SepalWidthCm`
* `PetalLengthCm`
* `PetalWidthCm`

The `Id` column was removed because it does not provide useful information for species classification.

---

## 🧹 Data Preprocessing

The dataset was divided into training and testing sets using an **80/20 stratified split**.

* Training samples: 120
* Testing samples: 30
* Samples per class in test set: 10

`StandardScaler` was applied to standardize the numerical features.

---

## 🤖 Machine Learning Models

Four classification algorithms were trained and compared:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Support Vector Machine (SVM)
4. Random Forest

### Model Performance

| Model               | Accuracy | Precision | Recall | F1-Score |
| ------------------- | -------: | --------: | -----: | -------: |
| SVM                 |   0.9667 |    0.9697 | 0.9667 |   0.9666 |
| Logistic Regression |   0.9333 |    0.9333 | 0.9333 |   0.9333 |
| KNN                 |   0.9333 |    0.9444 | 0.9333 |   0.9327 |
| Random Forest       |   0.9000 |    0.9024 | 0.9000 |   0.8997 |

The SVM model achieved the highest test-set performance among the models evaluated.

---

## 🏆 Final Model

The final model was the **Support Vector Machine (SVM)** classifier using an RBF kernel.

### Test Set Results

* **Accuracy:** 96.67%
* **Precision:** 96.97%
* **Recall:** 96.67%
* **F1-Score:** 96.66%

Out of 30 test samples, the model correctly classified **29 samples**.

---

## 📋 Classification Report

The final SVM produced the following class-level results:

| Class           | Precision | Recall | F1-Score |
| --------------- | --------: | -----: | -------: |
| Iris-setosa     |    1.0000 | 1.0000 |   1.0000 |
| Iris-versicolor |    1.0000 | 0.9000 |   0.9474 |
| Iris-virginica  |    0.9091 | 1.0000 |   0.9524 |

Overall:

* Accuracy: **0.9667**
* Macro F1-score: **0.9666**
* Weighted F1-score: **0.9666**

---

## 🔲 Confusion Matrix

The confusion matrix was:

```text
[[10, 0, 0],
 [ 0, 9, 1],
 [ 0, 0,10]]
```

This indicates that:

* All 10 Iris-setosa samples were classified correctly.
* 9 out of 10 Iris-versicolor samples were classified correctly.
* All 10 Iris-virginica samples were classified correctly.
* One Iris-versicolor sample was classified as Iris-virginica.

---

## 🔄 Cross-Validation

Five-fold cross-validation was performed.

Fold scores:

```text
Fold 1: 0.9167
Fold 2: 1.0000
Fold 3: 0.9583
Fold 4: 0.9583
Fold 5: 1.0000
```

### Cross-Validation Summary

* Mean Accuracy: **0.9667**
* Standard Deviation: **0.0312**

---

## 📊 Exploratory Data Analysis

The notebook includes visualizations for:

* Class distribution
* Feature distributions
* Petal length vs. petal width
* Feature correlation matrix

The analysis also showed a strong relationship between petal measurements, with petal length and petal width showing a correlation of approximately **0.96** in the dataset.

---

## 🔮 Prediction Probabilities

The final SVM model was configured to generate class prediction probabilities using:

```python
predict_proba()
```

This allows the model's predicted class probabilities to be inspected for individual test samples.

---

## 💾 Saved Model

The trained model was saved as:

```text
iris_species_classification_model.pkl
```

The model can be loaded later using `joblib`.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Joblib
* Google Colab
* Kaggle Dataset

---

## 📁 Project Files

```text
Task-4-Iris-Flower-Classification/
│
├── Iris_Flower_Classification.ipynb
├── iris_species_classification_model.pkl
└── README.md
```

---

## 🎯 Learning Outcomes

Through this project, I practiced:

* Classification problem formulation
* Exploratory data analysis
* Feature selection
* Data preprocessing
* Feature scaling
* Multiple classification algorithms
* Model comparison
* Classification metrics
* Confusion matrix interpretation
* Cross-validation
* Prediction probability analysis
* Model serialization

---

## 👩‍💻 Internship

**Machine Learning Internship — Arch Technologies**

**Task:** Iris Flower Classification

**Month:** Month 2

**Author:** Syeda Abeera Haya
