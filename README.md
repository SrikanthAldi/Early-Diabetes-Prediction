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

### Conclusion

This project demonstrated the application of machine learning techniques for early prediction of diabetes using a publicly available health dataset. Through exploratory analysis, logistic regression and random forest models were developed and evaluated to identify individuals at risk. While logistic regression offered strong interpretability and solid baseline performance, the Random Forest model, when trained on SMOTE-balanced data, achieved the highest predictive performance across all evaluation metrics, including precision, recall, F1-score, and AUC.
Addressing class imbalance through SMOTE was a critical step that significantly improved the model's sensitivity in detecting diabetic cases, which is vital in real-world healthcare settings. The project also highlighted the importance of proper preprocessing, feature transformation, and careful model evaluation.
Overall, the study shows that with thoughtful preprocessing and class-balancing techniques, machine learning models can serve as powerful tools in supporting early diabetes detection and public health decision-making. Future work could explore more advanced models (e.g., gradient boosting or neural networks) and real-time clinical validation to further improve prediction accuracy and deployment potential.
<img width="468" height="289" alt="image" src="https://github.com/user-attachments/assets/099fcb27-5a76-4de5-bb4a-84a21b6ea017" />

---

## 🛠️ Tech Stack
- **Languages**:  R  
- **Techniques**: Logistic Regression, Random Forest, SMOTE for imbalance handling  
- **Tools**: Jupyter Notebook, R Studio

---


