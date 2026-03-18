# ECG Heartbeat Classification 🫀

This repository contains a machine learning pipeline developed to classify heartbeat anomalies from Electrocardiogram (ECG) signals. The project explores feature selection, dimensionality reduction, and predictive modeling applied to biomedical data.

## 📊 Dataset
The models were trained and evaluated using the **ECG Heartbeat Categorization Dataset**, which combines data from:
* **MIT-BIH Arrhythmia Database**
* **PTB Diagnostic ECG Database**

## 🧠 Methodology & Machine Learning Pipeline
The core of this project focuses on optimizing model performance while reducing computational complexity. 

### Dimensionality Reduction
Two main approaches were compared for feature extraction:
1. **Principal Component Analysis (PCA):** Reduced the dataset to 28 principal components.
2. **Correlation Matrix:** Filtered the dataset to 103 features.

### Predictive Modeling
Several classifiers were tested, including Support Vector Classifiers (SVC) and Random Forests. The performance was rigorously validated using **K-fold Cross-Validation**.

## 🏆 Key Results
The **Random Forest Classifier** yielded the best performance across both feature extraction methods:

* **Using PCA (28 features):**
  * **Test Accuracy:** 95.68%
  * **K-fold F1 Mean:** 96.99%
* **Using Correlation Matrix (103 features):**
  * **Test Accuracy:** 95.72%
  * **K-fold F1 Mean:** 96.95%

**Conclusion:** The PCA approach proved to be the most efficient strategy. It achieved nearly identical predictive performance to the correlation matrix method but required significantly fewer features (28 vs. 103), making the model much lighter and faster.

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** `scikit-learn`, `pandas`, `numpy` 
* **Environment:** Jupyter Notebook

---
*Developed as part of the Machine Learning in Biomedical Engineering course (FCT NOVA).*
