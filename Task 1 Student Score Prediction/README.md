# 🎓 Student Performance Analysis & Prediction

This project explores factors affecting **student performance** and builds regression models to predict exam scores.  
It includes **data cleaning, feature encoding, normalization, and regression modeling (Linear vs Polynomial)**.

---

## 📁 Project Structure

```
├── data/
│   └── StudentPerformanceFactors.csv           # Raw dataset
│   └── StudentPerformanceFactors_Cleaned.csv   # Cleaned dataset
├── data.ipynb                                  # Data cleaning & preprocessing
├── model.ipynb                                 # Regression modeling and evaluation
├── requirements.txt                            # Dependencies
└── README.md                                   # Project documentation
```

---

## ⚙️ Setup Instructions

1. **Clone or copy the project folder**
   ```bash
   git clone <your_repo_url>
   cd <project_folder>
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate        # On Mac/Linux
   venv\Scripts\activate           # On Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

5. **Open and run notebooks**
   - `data.ipynb` → performs data inspection, cleaning, encoding, and normalization  
   - `model.ipynb` → trains Linear & Polynomial Regression models, evaluates them, and compares performance  

---

## 🧹 Data Cleaning Steps (in `data.ipynb`)

- Handle missing values using **mode imputation**  
- **Label Encode** categorical features  
- **Normalize** numerical features using `StandardScaler`  
- Remove duplicates  
- Save cleaned dataset → `StudentPerformanceFactors_Cleaned.csv`

---

## 🤖 Modeling (in `model.ipynb`)

Two regression models are applied:

| Model | Description | Key Metric |
|--------|--------------|------------|
| **Linear Regression** | Fits a straight-line relationship | R², MAE, RMSE |
| **Polynomial Regression** | Captures non-linear patterns (degree=2) | R², MAE, RMSE |

📊 The notebook compares performance between models both **numerically** and **visually** (Actual vs Predicted plots).

---

## 📈 Example Output

| Model | R² Score | MAE | RMSE |
|--------|-----------|------|-------|
| Linear Regression | 0.82 | 2.15 | 3.02 |
| Polynomial Regression (deg=2) | 0.89 | 1.85 | 2.54 |

*(These are example values — actual results may vary.)*

---


## 🪪 License
This project is open-source under the [MIT License](LICENSE).
