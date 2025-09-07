# Early-Diabetes-Prediction

# 🩺 Early Diabetes Prediction using Machine Learning

This project predicts the likelihood of diabetes using health indicators such as **blood glucose level, BMI, Hypertension , HbA1c, smoking history and heart disease**.The Project is entirely implemented in R. It applies **Logistic Regression** and **Random Forest (with SMOTE)** to handle class imbalance, achieving strong predictive accuracy and recall.

---

## 📊 Motivation
Diabetes is a global health challenge, and early detection plays a key role in prevention and better care.  
This project demonstrates how **data-driven methods** can support early intervention in healthcare.

---

## 🗂️ Dataset
- Source: [Kaggle Diabetes Dataset](https://www.kaggle.com/)  
- Records: ~16,000 patients  
- Features: Age, BMI, Blood glucose, HbA1c, Smoking history, Hypertension, Heart disease, Gender, etc.  
- Target: Diabetes status (Positive / Negative)

---

## 🔍 Approach
1. **Data Exploration**: EDA with histograms, correlation plots, and boxplots to identify outliers and skewed data.  
2. **Preprocessing**:  
   - Log transformation on glucose and HbA1c  
   - Dummy encoding for categorical variables  
   - Train-test split (70/30)  
3. **Models Implemented**:  
   - Logistic Regression (baseline, interpretable model)  
   - Random Forest (robust, handles non-linearity)  
   - Random Forest + **SMOTE** (for class imbalance)  
4. **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, ROC-AUC.

---

## 📈 Results
### Logistic Regression vs Random Forest

| Metric      | Logistic (Train) | Random Forest (Train) | Logistic (Test) | Random Forest (Test) |
|-------------|------------------|------------------------|-----------------|-----------------------|
| **Accuracy** | 89.4%           | 85.8%                 | 89.81%          | 88.02%               |
| **Precision** | 43.4%           | 86.0%                 | 47.5%           | 35.7%                |
| **Recall**   | 88.0%           | 49.4%                 | 86.5%           | 35.3%                |
| **F1 Score** | ~58.2%          | ~62.6%                | 61.3%           | 35.5%                |
| **AUC**      | 0.9167          | –                     | 0.9579          | 0.8114               |

---

### Random Forest Model Comparison (with SMOTE)

| Model                   | Accuracy | Precision | Recall (Sensitivity) | F1-Score | AUC   |
|--------------------------|----------|-----------|-----------------------|----------|-------|
| Original Random Forest   | 0.8824   | 0.3669    | 0.3573                | 0.362    | 0.8106|
| Random Forest + SMOTE    | 0.958    | 0.958     | 0.958                 | 0.958    | 0.958 |

## 📊 Model Performance

### Logistic Regression vs Random Forest with SMOTE
| Model                  | Accuracy | Precision | Recall (Sensitivity) | F1-Score | AUC   |
|-------------------------|----------|-----------|-----------------------|----------|-------|
| Logistic Regression     | 0.8981   | 0.4749    | 0.8649                | 0.6131   | 0.9579|
| Random Forest + SMOTE   | 0.958    | 0.958     | 0.958                 | 0.958    | 0.958 |

---

### Visual Performance Comparison
![Logistic vs SMOTE RF](docs/logistic-vs-smote-bar.png)

---

## 🔑 Key Insights
- Logistic Regression provided a strong baseline:  
  - **High recall (86.5%)** → reliable for detecting diabetic cases  
  - **AUC = 0.9579** → excellent discriminative ability  

- Random Forest with **SMOTE balancing** outperformed across the board:  
  - Accuracy: **95.8%**  
  - Precision, Recall, F1: all **95.8%**  
  - AUC: **0.958**  

✅ **Conclusion**: Logistic Regression is interpretable and robust, but **Random Forest with SMOTE** achieves superior predictive performance on imbalanced healthcare data.


---

## 🛠️ Tech Stack
- **Languages**:  R  
- **Techniques**: Logistic Regression, Random Forest, SMOTE for imbalance handling  
- **Tools**: Jupyter Notebook, R Studio

---


