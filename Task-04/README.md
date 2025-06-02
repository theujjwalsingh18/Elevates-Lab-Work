# 🧠 Logistic Regression Binary Classifier - Breast Cancer Detection

This project demonstrates how to build and evaluate a **binary classification model** using **Logistic Regression** to predict whether a tumor is **malignant** or **benign** based on medical features.

---

## 📂 Dataset

We used a dataset containing features like:
- `radius_mean`, `texture_mean`, `perimeter_mean`, ...
- `radius_worst`, `texture_worst`, `perimeter_worst`, ...
- Target column: `diagnosis` (B = benign, M = malignant → encoded as 0 and 1)

---

## ⚙️ Tools & Libraries

- Python 3
- Scikit-learn
- Pandas
- Matplotlib
- Seaborn
- Pickle (for saving models)

---

## 🧪 Steps Followed

1. **Data Loading & Exploration**
2. **Preprocessing**
   - Label encoding (`diagnosis` → binary)
   - Feature standardization using `StandardScaler`
3. **Train-Test Split**
4. **Model Training**
   - Logistic Regression (`sklearn.linear_model.LogisticRegression`)
5. **Model Evaluation**
   - Accuracy
   - Confusion Matrix
   - Classification Report (Precision, Recall, F1-Score)
   - ROC-AUC Curve
6. **Model Saving** (using `pickle`)
   - Logistic model saved to `model/logistic_model.pkl`
   - Scaler saved to `model/scaler.pkl`
7. **Threshold Tuning & Sigmoid Explanation**

---

## 📈 Evaluation Results

- **Accuracy**: `97.37%`
- **Classification Report**:
  ```
              precision    recall  f1-score   support

           0       0.97      0.99      0.98        71
           1       0.98      0.95      0.96        43

    accuracy                           0.97       114
   macro avg       0.97      0.97      0.97       114
weighted avg       0.97      0.97      0.97       114
  ```

- **Confusion Matrix**:
  [[70  1]
   [ 2 41]]
- **ROC-AUC Score**: `0.997`
---

## 💾 Saving and Loading the Model (with Pickle)

```python
import pickle
import os

# Save the model
os.makedirs("model", exist_ok=True)
with open("model/logistic_model.pkl", "wb") as f:
    pickle.dump(model, f)

# Save the scaler
with open("model/scaler.pkl", "wb") as f:
    pickle.dump(scaler, f)

# Load the model and scaler
with open("model/logistic_model.pkl", "rb") as f:
    model = pickle.load(f)

with open("model/scaler.pkl", "rb") as f:
    scaler = pickle.load(f)
```

---

## 📉 Sigmoid Function (Explanation)

The logistic regression model uses the sigmoid function:

\[
\sigma(z) = \frac{1}{1 + e^{-z}}
\]

This function maps the linear combination of input features into a probability between 0 and 1. Classification is based on whether this probability exceeds a chosen **threshold** (default = 0.5, but tunable).

---

## 📌 Conclusion

- Logistic Regression performs **exceptionally well** on this binary classification task.
- The **ROC-AUC score of 0.997** shows the model is near perfect.
- It's interpretable, simple, and effective for medical datasets.

---
