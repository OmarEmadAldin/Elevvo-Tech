# Movielens User-Based Recommender (Enhanced Notebook)

This repository contains an **enhanced Jupyter notebook** (generated from your `data.ipynb`) that adds data exploration, merging, visualization, a user-based collaborative filtering recommender, and evaluation (Precision@K).

## Files produced
- `data_d.ipynb` — the enhanced notebook (run this locally to generate plots and `merged_data.csv`).
- `requirements.txt` — Python dependencies (for Python 3.12).
- `README.md` — this document.
- `merged_data.csv` — **will be created when you run the notebook** (the notebook searches for Movielens files like `u.data`, `u.item`, `ratings.csv`, etc.).

## Highlights
- Flexible data-loading: searches common filenames and locations (`./`, `./data`, `/mnt/data`, `ml-100k/`).
- Exploratory plots (matplotlib): rating distribution, top movies, top users, average ratings.
- User-based CF using cosine similarity, with leave-one-out Precision@K evaluation and a plot of Precision@K vs K.
- Clean `merged_data.csv` that combines ratings, movie titles, and (when available) user info.

## How to use
1. Place the Movielens 100k files (`u.data`, `u.item`, `u.user`) or Kaggle CSVs (`ratings.csv`, `movies.csv`, `users.csv`) in the notebook folder or a `data/` subfolder.
2. Create a virtual environment (recommended) with Python 3.12 and install requirements:

```bash
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

3. Open and run `data_d.ipynb` in JupyterLab or Jupyter Notebook. Run cells top to bottom. The notebook will save `merged_data.csv` and display plots.
4. For faster evaluation edit the K-range or reduce the dataset slice in the evaluation cell.

## Notes & tips
- The notebook uses matplotlib (no seaborn) to keep plotting portable and compatible.
- If you prefer mean-centering (removing user bias) for similarity, uncomment the suggested lines in the recommender cell.
- Evaluation uses leave-one-out per-user; results are averaged across users and reported as Precision@K.
