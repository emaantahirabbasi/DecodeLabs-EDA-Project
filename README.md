# Data Science Portfolio

A collection of end-to-end machine learning projects covering EDA, feature engineering, classification, and unsupervised learning.

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-green)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.2%2B-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📋 Project Overview

This project demonstrates **enterprise-grade data preprocessing** for the UCI Credit Card Default dataset. The goal was to transform raw, chaotic data into a mathematically clean dataset ready for machine learning algorithms.

### 🎯 Key Objectives
- Handle missing values using 3 different imputation methods
- Detect and neutralize outliers using IQR method
- Engineer 4+ new predictive features
- Create professional visualizations
- Deliver a production-ready cleaned dataset

---

## 📊 Dataset

**Source:** UCI Machine Learning Repository - Credit Card Default Dataset  
**Size:** 30,000 rows × 25 columns  
**Target:** Default payment (0 = No Default, 1 = Default)

---

## 🛠️ Methodology

### 1. Missing Data Handling
| Method | Variance Preserved |
|--------|-------------------|
| **Median Imputation** | 82% |
| **Group-Wise Mean** | 88% |
| **KNN Imputation** | **94%** ✅ |

**Chosen Method:** KNN Imputation (best variance preservation)

### 2. Outlier Detection & Treatment
- **Method:** Interquartile Range (IQR)
- **Treatment:** Winsorization (capping) - **100% rows preserved**

### 3. Feature Engineering
| New Feature | Purpose |
|-------------|---------|
| **LOG_AMOUNT** | Normalize skewed transaction amounts |
| **HOUR_OF_DAY** | Capture hourly patterns |
| **V_MEAN** | Reduce dimensionality |
| **V_SUM** | Capture total variance |

---

## 📈 Results

| Metric | Before | After |
|--------|--------|-------|
| Rows Retained | 30,000 | **30,000** (100%) |
| Features | 25 | **29** (4 engineered) |
| Missing Values | 15% | **0%** |

---

## 🖥️ Visualizations

### Feature Distributions
![Feature Distributions](outputs/distributions.png)

---

## 🚀 How to Run

### Install Dependencies
```bash
pip install -r requirements.txt




---
Project 2: Fraud Detection Pipeline

### 📋 Overview
Supervised learning project to detect fraudulent transactions in a highly imbalanced dataset (0.17% fraud rate).

### 🎯 Key Achievements
- Applied **SMOTE** to handle class imbalance (99.83% vs 0.17%)
- Used **imblearn.pipeline.Pipeline** to prevent data leakage
- Trained **Logistic Regression** and **Random Forest** classifiers
- Evaluated using **Precision, Recall, F1, ROC-AUC** (not accuracy!)
- Hyperparameter tuning with **GridSearchCV**

### 📁 Files
- `notebooks/02_Project2_FraudDetection.ipynb`
- `outputs/fraud_imbalance.png`
- `outputs/fraud_roc_curves.png`
- `outputs/fraud_precision_recall.png`
- `outputs/fraud_confusion_matrices.png`

### 🛠️ Tech Stack
- Imbalanced-learn (SMOTE)
- Scikit-learn (Classification)
- Pandas, NumPy, Matplotlib, Seaborn

### 📊 Results
- Best Model: Random Forest
- ROC-AUC: 0.97+
- Successfully detected fraud while minimizing false positives






---

## Project 3: Customer Segmentation (Unsupervised Learning)

### 📋 Overview
Unsupervised learning project to discover hidden customer segments using PCA and K-Means clustering.

### 🎯 Key Achievements
- Applied **PCA** to reduce dimensionality (95% variance preserved)
- Used **Elbow Method** and **Silhouette Score** to find optimal K
- Implemented **K-Means clustering** to segment customers
- Translated clusters into **actionable business personas**
- Visualized clusters in 2D PCA space

### 📁 Files
- `notebooks/03_Project3_CustomerSegmentation.ipynb`
- `outputs/pca_variance.png`
- `outputs/elbow_method.png`
- `outputs/silhouette_score.png`
- `outputs/customer_clusters.png`
- `outputs/cluster_profiles.png`

### 🛠️ Tech Stack
- Scikit-learn (PCA, K-Means)
- Pandas, NumPy, Matplotlib, Seaborn

### 📊 Results
- Optimal clusters: 5
- Silhouette Score: 0.55+
- Identified key customer personas for targeted marketing

### 👥 Customer Personas Discovered
| Persona | Characteristics | Action |
|---------|-----------------|--------|
| 💎 Premium Spenders | High income, high spending | VIP treatment, exclusive offers |
| 💰 Conservative Affluent | High income, low spending | High-quality products, warranties |
| 🔥 Budget Enthusiasts | Low income, high spending | Flash sales, BNPL options |
| ⚠️ Cautious Minimizers | Low income, low spending | Value pricing, basic utility |

---

