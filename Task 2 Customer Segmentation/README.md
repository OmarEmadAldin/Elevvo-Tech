# 🛍️ Mall Customers Segmentation using K-Means

## 📘 Project Overview
This project performs **customer segmentation** using **unsupervised learning (K-Means)** on the *Mall Customers* dataset.

The goal is to group customers into meaningful clusters based on their **Annual Income** and **Spending Score**, allowing businesses to understand customer behavior and target marketing strategies effectively.

---

## 🧩 Project Files

| File | Description |
|------|--------------|
| `Mall_Customers_Cleaning_and_Scaling.ipynb` | Cleans data, handles missing values, scales numeric features, and visualizes raw distributions. |
| `Mall_Customers_KMeans_Clustering_and_Evaluation.ipynb` | Applies K-Means clustering, determines optimal K using Elbow Method, evaluates clusters, and visualizes results. |
| `Mall_Customers_cleaned.csv` | Cleaned dataset ready for clustering. |
| `Mall_Customers_Clustered.csv` | Final dataset with assigned cluster labels. |
| `requirements.txt` | Python dependencies. |
| `README.md` | Project description and usage instructions. |

---

## 🧠 Workflow

### **1. Data Cleaning**
- Normalize column names.
- Drop duplicates and empty rows.
- Convert and fill missing values.
- Save cleaned dataset (`Mall_Customers_cleaned.csv`).

### **2. Scaling & Exploration**
- Apply `StandardScaler` for fair feature comparison.
- Visualize raw vs. scaled distributions (2D scatter plots).

### **3. K-Means Clustering**
- Use Elbow Method to choose optimal K (≈ 5).
- Fit K-Means and assign cluster labels.
- Evaluate clusters with:  
  - **Silhouette Score** (↑ better)  
  - **Calinski–Harabasz Index** (↑ better)  
  - **Davies–Bouldin Index** (↓ better)

### **4. Visualization**
- Plot clusters in 2D (Income vs. Spending Score).  
- Display cluster centers and interpret segment profiles.

---

## 🚀 How to Run

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Open and run the notebooks in order:
   ```bash
   Mall_Customers_Cleaning_and_Scaling.ipynb
   Mall_Customers_KMeans_Clustering_and_Evaluation.ipynb
   ```

3. Outputs will be generated in the same directory:
   - `Mall_Customers_cleaned.csv`
   - `Mall_Customers_Clustered.csv`

---

## 📊 Interpretation Example

| Cluster | Income | Spending | Description |
|----------|---------|-----------|--------------|
| 1 | Low | Low | Budget-conscious customers |
| 2 | High | Low | Wealthy but less engaged |
| 3 | Low | High | Young enthusiastic spenders |
| 4 | Medium | Medium | Average middle-class |
| 5 | High | High | Premium shoppers |

---

## 🧰 Dependencies
All dependencies are listed in `requirements.txt`:
```
pandas
numpy
matplotlib
scikit-learn
```
