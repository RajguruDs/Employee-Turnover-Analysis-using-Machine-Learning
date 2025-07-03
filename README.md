
# 🧠 Employee Turnover Analysis using Machine Learning

A data science project aimed at analyzing HR data to identify key factors behind employee resignation and predict future turnover using classification models.

---

## 📊 Problem Statement

High employee turnover is costly and disruptive. Companies struggle to understand **why employees leave** and **how to retain them**. This project addresses:

- 🔍 What features influence employee attrition the most?
- 🔍 Can we accurately **predict which employees are likely to leave**?
- 🔍 How can data-driven strategies help **reduce turnover**?

---

## 🎯 Objective

- Perform **exploratory data analysis** (EDA) on HR data.
- Use ML classification models to **predict employee resignations**.
- Evaluate models using **accuracy, precision, recall, ROC-AUC**.
- Identify **key drivers** of employee attrition for HR strategy.

---

## 🧾 Dataset Info

- `HR_comma_sep.csv` with 14,999 rows and 10 features.
- Target variable: `left` (1 = left the company, 0 = stayed)
- Features include:
  - Satisfaction level
  - Number of projects
  - Monthly working hours
  - Time at company
  - Promotions, salary, department

---

## 📊 Exploratory Data Analysis

### ✅ 1. Correlation Heatmap

Shows feature relationships with `left`:

![Heatmap](images/heatmap.png)

**Inference:**
- 🔻 `satisfaction_level`: **-0.39** correlation → lower satisfaction = more likely to leave
- 🔺 `time_spend_company`, `number_project`: higher values increase risk
- Weak influence: `promotion_last_5years`, `Work_accident`

---

### ✅ 2. Class Imbalance Check

Bar graph showing imbalance in target classes:

![Class Imbalance](images/class_imbalance.png)

**Inference:**  
Dataset is slightly imbalanced — applied **SMOTE** for oversampling to avoid bias.

---

## ⚙️ Model Building

### Algorithms Used:
- Logistic Regression
- Decision Tree
- Random Forest ✅ *(Best)*
- SVM
- KNN
- Gradient Boosting
- XGBoost

---

### 📈 Accuracy Comparison

![Model Accuracy Bar](images/model_accuracy.png)

- ✅ **Random Forest**: 99%
- Gradient Boosting: 96%
- Logistic Regression: 79%
- SVM: 94%
- KNN: 93%

---

## 📉 ROC Curve Analysis

The ROC (Receiver Operating Characteristic) curve is a graphical plot that illustrates the diagnostic ability of a binary classifier system. The Area Under Curve (AUC) value ranges from 0 to 1. The closer to 1, the better the model.

### 🔷 Random Forest
![ROC RF](images/roc_random_forest.png)  
**AUC: 0.99** — Outstanding performance

### 🔷 Logistic Regression
![ROC LR](images/roc_logistic_regression.png)  
**AUC: ~0.88**

### 🔷 Gradient Boosting
![ROC GB](images/roc_gradient_boosting.png)  
**AUC: ~0.93**

> 🔑 **Note:** Random Forest had the **highest AUC score** and was therefore selected as the final model.

---

## 🧠 Conclusion

- **Top contributing factors**: low satisfaction, long working hours, no promotion, many projects.
- **Random Forest** emerged as the most reliable model.
- **SMOTE** improved model performance on imbalanced data.
- HR departments can use these insights to improve employee retention through:
  - Better workload management
  - Promotion policies
  - Boosting satisfaction initiatives

---

## 🤝 Let’s Connect

💼 [LinkedIn](https://www.linkedin.com/in/yourprofile)  
🐙 [GitHub](https://github.com/yourusername)  
📧 your.email@example.com

---

## 🔧 Run This Project

```bash
git clone https://github.com/yourusername/employee-turnover-analysis.git
cd employee-turnover-analysis
pip install -r requirements.txt
jupyter notebook
```

---

## 📁 Directory Structure

```
employee-turnover-analysis/
├── Coursendproject.ipynb
├── HR_comma_sep.csv
├── README.md
├── requirements.txt
└── images/
    ├── heatmap.png
    ├── class_imbalance.png
    ├── model_accuracy.png
    ├── roc_random_forest.png
    ├── roc_logistic_regression.png
    └── roc_gradient_boosting.png
```
