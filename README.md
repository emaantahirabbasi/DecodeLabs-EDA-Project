# DecodeLabs Internship - Advanced EDA & Feature Engineering

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
