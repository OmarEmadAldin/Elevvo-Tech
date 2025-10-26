# GTZAN Genre Classification — Librosa + Random Forest
# **First you have to run the code on kaggle and use the dataset there or download it locally**
This repository contains an enhanced Jupyter notebook that extracts audio features using **librosa**, trains a **Random Forest** classifier with hyperparameter tuning (GridSearchCV), and evaluates the model.

## Files
- `gtzan_enhanced.ipynb` — Enhanced notebook (run this locally in the folder that contains `genres_original/`).
- `gtzan_features.csv` — Will be created when you run the extraction cell (saved in the notebook folder).
- `gtzan_rf_model.pkl` — Saved model (created after training).
- `requirements.txt` — Python dependencies for Python 3.12.

## Quick start
1. Put the `genres_original/` folder in the same directory as the notebook.
2. Create and activate a virtual environment (Python 3.12 recommended):
```
python -m venv venv
source venv/bin/activate  # Windows: venv\\Scripts\\activate
pip install -r requirements.txt
```

3. Open `gtzan_enhanced.ipynb` and run cells sequentially. The extraction may take a few minutes.
4. After training, check `gtzan_rf_model.pkl` and `gtzan_features.csv`.

## What's inside
- Audio feature extraction (MFCC mean/std, chroma, spectral centroid/bandwidth/rolloff, zero-crossing rate).
- Random Forest classification with GridSearchCV tuning (`n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`).
- Plots: confusion matrix, feature importance, PCA visualization, waveform and MFCC spectrogram for a sample audio file.
- Optional: you can replace extraction with precomputed CSV (`features_30_sec.csv`).

## Notes
- Extraction depends on `librosa` and `soundfile`; ensure they are installed.
- For faster experiments, load precomputed feature CSV instead of extracting features each time.
- You can increase GridSearch ranges or switch to RandomizedSearchCV for wider hyperparameter exploration.
