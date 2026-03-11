# ❤️ ML-VerzeoMajor — Heart Disease Risk Prediction

A Machine Learning classification project that predicts a patient's **10-year risk of Coronary Heart Disease (CHD)** using real-world cardiovascular data from the Framingham Heart Study — completed as the **Major Project** of the Verzeo ML Program.

---

## 🎯 Overview

Coronary Heart Disease is one of the leading causes of death worldwide. Early prediction of CHD risk allows for timely medical intervention and lifestyle changes. This project applies supervised ML classification techniques to a real clinical dataset to build a reliable binary risk predictor.

**Prediction Goal:** Given a patient's demographic, behavioral, and medical attributes, predict whether they will develop coronary heart disease within the next **10 years**.

---

## 🗃️ Dataset

The dataset is publicly available on **Kaggle** and originates from an ongoing cardiovascular study on residents of **Framingham, Massachusetts**.

| Property         | Details                          |
|------------------|----------------------------------|
| Source           | Kaggle / Framingham Heart Study  |
| Records          | 4,240+ patients                  |
| Features         | 15 attributes                    |
| Target Variable  | `TenYearCHD` — 1 (Yes) / 0 (No) |
| Task             | Binary Classification            |

---

## 📋 Features & Attributes

### Demographic
| Feature  | Type    | Description                                   |
|----------|---------|-----------------------------------------------|
| `sex`    | Nominal | 0 = Male, 1 = Female                          |
| `age`    | Continuous | Age of the patient (in years)              |

### Behavioral
| Feature          | Type       | Description                                         |
|------------------|------------|-----------------------------------------------------|
| `currentSmoker`  | Nominal    | Whether the patient is a current smoker             |
| `cigsPerDay`     | Continuous | Average number of cigarettes smoked per day         |

### Medical History
| Feature            | Type    | Description                                          |
|--------------------|---------|------------------------------------------------------|
| `BPMeds`           | Nominal | Whether the patient is on blood pressure medication  |
| `prevalentStroke`  | Nominal | Whether the patient has previously had a stroke      |
| `prevalentHyp`     | Nominal | Whether the patient is hypertensive                  |
| `diabetes`         | Nominal | Whether the patient has diabetes                     |

### Clinical Measurements
| Feature       | Type       | Description                          |
|---------------|------------|--------------------------------------|
| `totChol`     | Continuous | Total cholesterol level              |
| `sysBP`       | Continuous | Systolic blood pressure              |
| `diaBP`       | Continuous | Diastolic blood pressure             |
| `BMI`         | Continuous | Body Mass Index                      |
| `heartRate`   | Continuous | Resting heart rate                   |
| `glucose`     | Continuous | Blood glucose level                  |

### Target
| Feature        | Type   | Description                                              |
|----------------|--------|----------------------------------------------------------|
| `TenYearCHD`   | Binary | **1** = At risk of CHD in 10 years, **0** = Not at risk |

---

## 🤖 Models & Approach

The project trains and compares multiple classification models:

| Model                        | Purpose                                          |
|------------------------------|--------------------------------------------------|
| **Logistic Regression**      | Baseline probabilistic classifier                |
| **Random Forest**            | Ensemble model for robust feature handling       |
| **Decision Tree**            | Interpretable rule-based classification          |
| **K-Means Clustering**       | Unsupervised exploration of patient groupings    |
| **Support Vector Machine**   | High-margin binary classification                |

---

## 🔑 Key Steps

1. **Exploratory Data Analysis (EDA)** — Distribution plots, correlation heatmaps, class balance check
2. **Data Preprocessing** — Handling missing values, encoding categorical features, feature scaling
3. **Class Imbalance Handling** — Addressing the skew between CHD-positive and CHD-negative records
4. **Model Training** — Training all classifiers on the preprocessed dataset
5. **Evaluation** — Comparing models on Accuracy, Precision, Recall, F1-Score, and ROC-AUC
6. **Best Model Selection** — Selecting the highest-performing model for deployment

---

## 📊 Evaluation Metrics

Given the medical context, **Recall (Sensitivity)** is the most critical metric — it is more costly to miss a true CHD case than to flag a false positive.

| Metric       | Why It Matters                                         |
|--------------|--------------------------------------------------------|
| Accuracy     | Overall correctness of predictions                    |
| Precision    | Of predicted positive cases, how many are truly at risk |
| **Recall**   | Of actual CHD cases, how many were correctly identified |
| F1-Score     | Harmonic mean of precision and recall                 |
| ROC-AUC      | Ability to discriminate between positive and negative  |

---

## 🗂️ Repository Structure

```
├── ML-MAJOR-AUGUST-ML081B3.ipynb           # Main major project notebook
├── ML-MAJOR-AUGUST-ML081B3copy.ipynb       # Backup / experimental version
├── Logistic Regression in Python - Step by Step.ipynb  # Logistic regression deep-dive
├── 12_1_12_3.ipynb                         # Classification exercises
├── K-Means.ipynb                           # Clustering notebook
├── framingham.csv                          # Framingham Heart Study dataset (main)
├── winequality.csv                         # Supporting dataset
├── iris_dataset.csv                        # Supporting dataset
├── StudentsPerformance (4).csv             # Supporting dataset
├── Weather.csv                             # Supporting dataset
└── README.md
```

---

## ⚙️ Installation & Setup

### Prerequisites

- Python 3.7+
- Jupyter Notebook

### Clone the Repository

```bash
git clone https://github.com/Bharath-Mbnsv/ML-VerzeoMajor.git
cd ML-VerzeoMajor
```

### Install Dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter imbalanced-learn
```

### Launch the Main Notebook

```bash
jupyter notebook ML-MAJOR-AUGUST-ML081B3.ipynb
```

---

## 🔮 Future Improvements

- Apply **SMOTE** or other oversampling techniques to better address class imbalance
- Add **feature selection** using RFE (Recursive Feature Elimination) or SHAP values
- Experiment with **XGBoost** and **LightGBM** for improved performance
- Deploy the best model as a **Flask / Streamlit** web app for clinical use
- Explore deep learning approaches with patient time-series data

---

## 📚 References

- [Framingham Heart Study Dataset — Kaggle](https://www.kaggle.com/datasets/amanajmera1/framingham-heart-study-dataset)
- Dawber, T.R. et al. — *Epidemiological Approaches to Heart Disease: The Framingham Study* (1951)

---

## 🤝 Contributing

Contributions are welcome! To get started:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request
