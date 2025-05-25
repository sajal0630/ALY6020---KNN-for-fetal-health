# Fetal Health Classification using K-Nearest Neighbors (KNN)
This project uses machine learning to predict fetal health status based on cardiotocography (CTG) data. The goal is to assist healthcare professionals in identifying potentially risky fetal conditions early using a simple, interpretable model.


## 📊 Dataset Overview

The dataset contains **2,126 fetal monitoring records** collected during pregnancy via cardiotocography. Each record includes several physiological features such as:
- Baseline fetal heart rate
- Accelerations
- Fetal movement
- Uterine contractions
- Light, severe, and prolonged decelerations
- Abnormal short-term variability

The original target variable had 3 classes:
- 1 = Normal
- 2 = Suspect
- 3 = Pathological

For this project, we recoded the target into a **binary classification problem**:
- 1 = Normal
- 0 = Not Normal (combining Suspect and Pathological)

---

## 🧠 Objective

- Build a K-Nearest Neighbors (KNN) model to classify fetal health
- Select clinically relevant features
- Justify each step with statistical and clinical reasoning
- Evaluate performance using confusion matrix, accuracy, precision, recall, and F1-score

---

## 🔧 Tools and Libraries

- Python (Jupyter Notebook)
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

---

## 🧪 Modeling Approach

1. **Data Cleaning**
   - Feature-wise handling of missing values (mean, median, or zero based on distribution)
   - Visual analysis of outliers (boxplots, histograms)
   - Feature standardization

2. **Feature Selection**
   - Based on clinical relevance and visual separation (boxplots)
   - Final features used: `accelerations`, `prolongued_decelerations`, `abnormal_short_term_variability`

3. **Modeling**
   - Trained KNN classifiers for K = 5, 15, 30
   - Selected K = 15 as the final model for its balanced performance

---

## ✅ Final Model Performance (K = 15)

| Metric               | Value    |
|----------------------|----------|
| Accuracy             | 88.97%   |
| Precision (Normal)   | 75%      |
| Recall (Normal)      | 74%      |
| Precision (Not Normal) | 93%   |
| Recall (Not Normal)    | 93%   |

---

## 🏥 Real-World Applicability

- This model could assist clinicians as a **real-time decision-support tool**
- Helps prioritize high-risk cases for early intervention
- Uses clinically explainable features and maintains a low false-negative rate

---

## 📄 Report

See `ALY_6020_Mod_1_Gangrade.docx` for a full 7–8 page report, including:
- Visualizations
- Model evaluation
- Clinical interpretation
- Strengths and limitations of KNN in healthcare
