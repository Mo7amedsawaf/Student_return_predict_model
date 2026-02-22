# 🎓 Predicting Student Retention Using Machine Learning

> Predicting whether a student will return for their second academic year using academic, demographic, and financial data.

**Supervised by:** Prof. Dr. Ahmed Yousry & Eng. Walaa Khaled

---

## 📌 Project Overview

Universities face a significant challenge in identifying students at risk of dropping out before their second year. This project applies supervised machine learning models — **Logistic Regression** and **Support Vector Machine (SVM)** — to analyze student data and predict second-year retention, enabling early academic and financial support interventions.

---

## 🎯 Problem Statement

**Target Variable:** `RETURNED_2ND_YR`
- `1` → Student returned for the second year
- `0` → Student did not return

---

## 📊 Dataset

The dataset is stored in `data/Student.xlsx` (sheet: `University information`).

Each row represents a single student with features across 5 categories:

| Category | Features |
|---|---|
| 👤 Demographic | Age, Gender, Background, In-state flag, International status, Distance from home, Housing status |
| 🏫 Academic Background | High school GPA, Major, Minor, Entrance exam scores |
| 📚 First Term Performance | Credit hours attempted/earned, Course grades |
| 📖 Second Term Performance | Credit hours attempted/earned, Course grades |
| 💰 Financial | Gross financial need, Cost of attendance, Family contribution, Unmet need |

> ⚠️ **Note:** If the dataset contains real student records, do not upload it publicly. Use the sample data template in `data/README.md` instead.

---

## 🔧 Feature Engineering

Key transformations applied:

- **CGPA** — Letter grades converted to GPA scale (4.0) and averaged across all courses
- **ENTRANCE_SCORE_FINAL** — Combined entrance scores with context-aware imputation by degree group
- **TOTAL_EARNED_HRS / TOTAL_DROP_HRS / SUCCESS_RATE** — Aggregated credit hour features from both terms
- **STDNT_MINOR** — Simplified to YES/NO due to high cardinality
- **STDNT_MAJOR** — Grouped into top 8 majors + "Others"
- Dropped course name columns (high cardinality, low signal)

---

## 🤖 Models Used

| Model | Notes |
|---|---|
| Logistic Regression | `C=1.5`, trained on top 10 correlated features |
| Support Vector Machine (SVM) | Default hyperparameters |

**Class Imbalance Handling:** SMOTE (Synthetic Minority Over-sampling Technique)

**Evaluation Metrics:** Accuracy, F1-Score, Confusion Matrix, Classification Report

---

## 🔍 Key Research Questions

- Does high school GPA affect second-year retention?
- Does financial need influence student dropout?
- Is the gap between attempted and earned credit hours a strong predictor?
- Do international students show different retention patterns?
- Does housing status impact continuation?

---

## 📁 Project Structure

```
student-retention-ml/
│
├── notebooks/
│   └── Student_ML_1.ipynb       # Main analysis notebook
│
├── data/
│   ├── Student.xlsx             # Dataset (add to .gitignore if sensitive)
│   └── README.md                # Dataset description & schema
│
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/student-retention-ml.git
cd student-retention-ml
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Add the dataset
Place `Student.xlsx` inside the `data/` folder.

### 4. Run the notebook
```bash
jupyter notebook notebooks/Student_ML_1.ipynb
```

---

## 📦 Requirements

See `requirements.txt` for the full list. Key libraries:
- `scikit-learn` — ML models and evaluation
- `imbalanced-learn` — SMOTE for class imbalance
- `pandas`, `numpy` — Data processing
- `matplotlib`, `seaborn` — Visualization

---

## 📄 License

This project is for Learning purposes only.
