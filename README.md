
# Term Deposit Marketing

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Random Forest](https://img.shields.io/badge/Random_Forest-228B22?style=flat)
![XGBoost](https://img.shields.io/badge/XGBoost-EC6B23?style=flat)
![Optuna](https://img.shields.io/badge/Optuna-4169E1?style=flat&logo=optuna&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

## Project Overview

**Customer Subscription Prediction | Random Forest & XGBoost**

A machine learning project designed to predict customer subscriptions to bank term deposits, identify high-potential customer segments, and improve direct marketing campaign effectiveness.

---

## 1. Project Overview

A European banking institution conducts direct marketing campaigns to promote term deposit subscriptions.

This project uses machine learning to identify customers who are more likely to subscribe and provide actionable business insights.

### Objectives

- Predict customer subscription outcomes (`yes` / `no`).
- Compare Random Forest and XGBoost models.
- Identify important factors influencing subscription.
- Determine high-potential customer segments.
- Provide data-driven business recommendations.

---

## 2. Dataset Overview

The dataset contains **40,000 customer records** and **14 original variables**, including demographic, financial, and campaign-related information.

**Target Variable:** `y`

- `yes` — Customer subscribed.
- `no` — Customer did not subscribe.

### Target Distribution

| Subscription Status | Percentage |
|---|---:|
| No | 92.76% |
| Yes | 7.24% |

The dataset is highly imbalanced, making Precision, Recall, F1 Score, and ROC-AUC important evaluation metrics.

> **Note:** The original dataset is not included in this repository.

---

## 3. Project Methodology

The project follows four main stages:

### Stage 1: Exploratory Data Analysis

- Data quality assessment
- Target distribution analysis
- Customer demographic and financial analysis
- Campaign behavior analysis
- Customer segmentation

### Stage 2: Random Forest Modeling

- Data preprocessing
- Feature engineering
- Class imbalance handling
- Hyperparameter tuning using GridSearchCV
- 5-fold cross-validation
- Model evaluation

### Stage 3: XGBoost Modeling

- Baseline XGBoost model
- Hyperparameter optimization
- GridSearchCV and Optuna
- 5-fold cross-validation
- Feature importance analysis

### Stage 4: Model Comparison & Business Analysis

- Random Forest vs XGBoost comparison
- Final model selection
- Customer segmentation insights
- Business recommendations

---

## 4. Model Performance

| Metric | Random Forest | XGBoost |
|---|---:|---:|
| Accuracy | 91.26% | **91.95%** |
| Precision | 43.24% | **45.91%** |
| Recall | **66.30%** | 62.60% |
| F1 Score | 52.34% | **52.97%** |
| ROC-AUC | 0.9175 | **0.9256** |
| Mean 5-Fold CV F1 | 0.5196 | **0.5305** |

### Final Model: XGBoost Grid 4

**XGBoost Grid 4** was selected because it achieved better overall Accuracy, Precision, F1 Score, ROC-AUC, and cross-validation F1.

Random Forest demonstrated higher Recall, making it useful when identifying more potential subscribers is the primary objective.

**Success Metric:** XGBoost achieved **91.95% holdout accuracy**, exceeding the 81% threshold.

However, the saved 5-fold cross-validation results report average F1 rather than average accuracy. Therefore, the exact CV-accuracy requirement remains unverified.

---

## 5. Key Findings

- **Customer Segmentation:** Customers aged 60+, students, retired customers, and higher-balance groups showed stronger historical subscription behavior.
- **Campaign Timing:** Q1 demonstrated comparatively strong subscription performance.
- **Financial Profile:** Housing loan status and account balance provided useful predictive information.
- **Feature Importance:** Call duration, campaign timing, age, and financial characteristics contributed to predictions.
- **Operational Limitation:** Call duration is unavailable before outreach and should not be used for pre-call customer targeting.

---

## 6. Business Recommendations

1. Prioritize customers using predicted subscription probabilities.
2. Combine model predictions with demographic and financial information.
3. Consider both conversion rates and customer-segment sizes.
4. Optimize campaigns using historical timing patterns.
5. Develop a pre-call prediction model excluding call duration.

---

## 7. Project Structure

```text

│
├── README.md
│
├── notebooks/
│   ├── exploration/
│   │   └── 01_Term_Deposit_Marketing_EDA.ipynb
│   │
│   └── modeling/
│       ├── 02_Random_Forest_Modeling.ipynb
│       ├── 03_XGBoost_Modeling.ipynb
│       └── 04_Model_Comparison_and_Business_Analysis.ipynb
│
└── reports/
    ├── figures/
    │   └── Term_Deposit_Analysis_Figures.pdf
    │
    └── summary/
        └── Term_Deposit_Final_Report.pdf
```

---

## 8. Project Documentation

| Document | Description |
|---|---|
| [Exploratory Data Analysis](notebooks/exploration/01_Term_Deposit_Marketing_EDA.ipynb) | Data exploration and customer segmentation |
| [Random Forest Modeling](notebooks/modeling/02_Random_Forest_Modeling.ipynb) | Random Forest training, tuning, and evaluation |
| [XGBoost Modeling](notebooks/modeling/03_XGBoost_Modeling.ipynb) | XGBoost optimization and feature importance |
| [Model Comparison](notebooks/modeling/04_Model_Comparison_and_Business_Analysis.ipynb) | Final model comparison and business analysis |
| [Final Project Report](reports/summary/Term_Deposit_Final_Report.pdf) | Detailed results, explanations, and recommendations |
| [Analysis Figures](reports/figures/Term_Deposit_Analysis_Figures.pdf) | Comparative graphs and visual insights |

---

## 9. Tools & Technologies

- Python
- Pandas & NumPy
- Scikit-learn
- Random Forest
- XGBoost
- Optuna
- Matplotlib & Seaborn
- Jupyter Notebook

---

## 10. Conclusion

This project demonstrates how machine learning can support more effective customer targeting in banking marketing campaigns.

**XGBoost Grid 4 achieved 91.95% holdout accuracy and 0.9256 ROC-AUC**, providing the strongest overall documented performance among the final evaluated candidates.

The findings highlight the importance of combining predictive modeling, customer segmentation, and interpretable business insights.

---

## Author

**Mitesh Sonani**
