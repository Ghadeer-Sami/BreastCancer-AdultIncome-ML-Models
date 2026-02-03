# Machine Learning Assignment – Model Comparison

This assignment compares multiple machine learning models across two datasets:  
**Breast Cancer Diagnostic (WDBC)** and **Adult Income**.  
The goal is to evaluate how preprocessing and algorithm choice affect classification performance.

## Dataset 1: Breast Cancer (WDBC)

### Preprocessing
- Loaded from `wdbc.data`
- No missing values
- Labels converted: `M = 1`, `B = 0`
- Features scaled using `StandardScaler`
- Split: 80% training / 20% testing

### Models Used
- Logistic Regression
- Gaussian Naive Bayes

### Results

| Model               | Accuracy | Precision | Recall | F1-Score |
|--------------------|----------|-----------|--------|----------|
| Logistic Regression | 98.24%   | ~1.0      | ~1.0   | ~1.0     |
| Naive Bayes         | 92.98%   | High      | Moderate | Good   |

**ROC-AUC:**
- Logistic Regression: 0.999  
- Naive Bayes: 0.989

**Conclusion:** Logistic Regression is the best model for this dataset.

---

## Dataset 2: Adult Income

### Preprocessing
- Removed missing values (`?`)
- One-hot encoded categorical features (~100 columns)
- Features scaled using `StandardScaler`
- Split: 70% training / 30% testing

### Models Used
- Logistic Regression
- Random Forest
- Decision Tree

### Results

| Model             | Accuracy | Precision | Recall | F1-Score |
|------------------|----------|-----------|--------|----------|
| Logistic Regression | 85%     | Balanced  | Moderate | Good   |
| Random Forest       | 96%     | High      | High     | Best   |
| Decision Tree       | 81%     | Moderate  | Low      | Weak   |

**ROC-AUC:**
- Logistic Regression: 0.908  
- Random Forest: 0.907  
- Decision Tree: 0.751

**Conclusion:** Random Forest is the strongest model for this dataset.

---

## Final Comparison

| Dataset         | Best Model          | Reason                                      |
|----------------|---------------------|---------------------------------------------|
| Breast Cancer   | Logistic Regression | High accuracy, clean numeric data           |
| Adult Income    | Random Forest       | Handles mixed data, avoids overfitting      |

---


