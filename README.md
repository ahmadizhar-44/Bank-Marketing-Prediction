# 🏦 Bank Marketing Term Deposit Prediction

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?logo=googlecolab&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?logo=scikit-learn&logoColor=white)

## 📌 Project Overview
This project aims to predict whether a customer will subscribe to a bank term deposit based on data from direct marketing campaigns (phone calls) of a Portuguese banking institution. By leveraging Machine Learning algorithms, this classification model helps the bank optimize its marketing strategies and target potential customers more effectively.

## 📊 Dataset Description
* **Source:** Bank Marketing Dataset[cite: 1].
* **Size:** 41,188 records and 21 fields (features)[cite: 1].
* **Target Variable (`y`):** Has the client subscribed to a term deposit? (Binary: '1' for Yes, '0' for No)[cite: 1]. The initial distribution was highly imbalanced with 36,548 'No' and 4,640 'Yes' values[cite: 1].

## 🛠️ Technologies & Libraries Used
* **Programming Language:** Python
* **Environment:** Google Colab
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Logistic Regression, Random Forest, RFE)
* **Imbalanced Data Handling:** Imbalanced-learn (SMOTE)

## 🔄 Project Workflow

### 1. Exploratory Data Analysis (EDA) & Data Cleaning
* Inspected the dataset for shape and missing values.
* Handled missing data represented as `'unknown'` strings by imputing them with the mode of their respective columns[cite: 1].
* Grouped fragmented categories in the `'education'` column (e.g., `'basic.4y'`, `'basic.6y'`, `'basic.9y'`) into a single `'basic'` category to reduce noise and improve model learning[cite: 1].

### 2. Feature Engineering & Encoding
* Converted cleaned categorical data into numerical formats using Label Encoding (`cat.codes`)[cite: 1]. 
* Applied One-Hot Encoding (`pd.get_dummies`) to prepare features for model training.

### 3. Handling Class Imbalance
* The dataset had a severe class imbalance. This was resolved by applying **SMOTE (Synthetic Minority Over-sampling Technique)**, which synthetically generated data for the minority class to ensure unbiased model training.

### 4. Feature Selection
* Applied **Recursive Feature Elimination (RFE)** to extract the top 20 most important features, reducing dimensionality and enhancing the performance of the classification models.

### 5. Model Training & Evaluation
* Trained **Logistic Regression** and **Random Forest Classifiers**.
* Evaluated models using Accuracy, Precision, Recall, F1-Score, Confusion Matrix, and ROC-AUC Curves.

## 🏆 Key Results
* **Best Model:** Random Forest Classifier.
* **Accuracy Achieved:** **88%** on the test dataset.
* The application of SMOTE drastically improved the model's ability (Recall) to correctly identify customers who actually subscribed to the term deposit.

## 🚀 How to Run the Project
Since this project was developed in Google Colab, running it is extremely simple:
1. Open [Google Colab](https://colab.research.google.com/).
2. Upload the `Bank-Marketing-Prediction.ipynb` file from this repository.
3. Upload the dataset to your Google Drive and update the path in the notebook:
   `data = '/content/My_Drive/MyDrive/path_to_your_data/bank-additional-full.csv'`[cite: 1].
4. Run all cells sequentially (`Runtime > Run all`).

---
**Author:** [Ahmad Izhar]  
*Feel free to star ⭐ this repository if you found it helpful!*
