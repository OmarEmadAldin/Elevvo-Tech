# 🌲 Forest Cover Type Prediction — Tuned Model Comparison

## 📘 Overview
This project uses the **UCI Covertype dataset** to predict the **type of forest cover** based on cartographic and environmental features.  
We perform **data cleaning**, **preprocessing**, **hyperparameter tuning**, and **model comparison** using **Decision Tree**, **Random Forest**, and **XGBoost** classifiers.

---

## 🚀 Workflow Summary

### 1️⃣ Data Cleaning & Preprocessing
- Handle missing and categorical values.
- Standardize feature scales.
- Split dataset (80% train / 20% test).

### 2️⃣ Hyperparameter Tuning
- Performed using **RandomizedSearchCV**.
- Best parameters saved as JSON:
  - `best_dt_params.json`
  - `best_rf_params.json`
  - `best_xgb_params.json`

### 3️⃣ Model Training (Tuned Parameters)
- Load parameters from JSON.
- Train models using tuned hyperparameters.
- Evaluate with consistent metrics.

### 4️⃣ Model Evaluation
Computed metrics:
- Accuracy
- Precision (weighted)
- Recall (weighted)
- F1-score (weighted)
- Classification report

### 5️⃣ Model Saving
Final trained models:
- `final_tuned_decision_tree.pkl`
- `final_tuned_random_forest.pkl`
- `final_tuned_xgboost.pkl`

---

## 📊 Evaluation Summary (Example)
| Model | Accuracy | Precision | Recall | F1 Score |
|--------|-----------|------------|---------|-----------|
| Decision Tree | 0.84 | 0.83 | 0.84 | 0.83 |
| Random Forest | 0.91 | 0.91 | 0.91 | 0.91 |
| XGBoost | 0.92 | 0.92 | 0.92 | 0.92 |

*(Actual results vary depending on data preprocessing and tuning ranges.)*

---

## 🧠 How to Run

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook Modelling_with_tuned_params.ipynb
   ```

3. **Run all cells** to train and evaluate models.

---

## 🧩 Notes
- XGBoost labels start from `0`; others may use `1–7`. Handled automatically.
- Trained models and tuning parameters are stored for reproducibility.

---

## 📁 Project Structure
```
├── Modelling_with_tuned_params.ipynb
├── best_dt_params.json
├── best_rf_params.json
├── best_xgb_params.json
├── final_tuned_decision_tree.pkl
├── final_tuned_random_forest.pkl
├── final_tuned_xgboost.pkl
├── requirements.txt
└── README.md
```

---

## 👨‍💻 Author
**Omar Ben Emad**  
Robotics Engineer  
📅 Created: October 2025
