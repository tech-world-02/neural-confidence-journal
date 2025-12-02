# Week 3–4 Baseline Confidence Classifier

This notebook (`baseline_confidence_classifier_week3-4.ipynb`) trains and evaluates 
baseline machine learning models for the Neural Confidence Journal project using the 
Week 1–2 dataset.

The focus in Weeks 3–4 is to move beyond pure EDA and build the first text classification 
pipeline with traditional ML techniques.

## 📌 What this notebook does

- Loads the preprocessed confidence journal dataset
- Splits the data into train/validation sets
- Builds a TF–IDF + Logistic Regression baseline pipeline
- Optionally compares with other classical models (e.g., SVM, Naive Bayes if included)
- Trains the model and saves:
  - `baseline_lr_tfidf.joblib` – baseline model
  - `best_model.joblib` – best-performing model (if different)
- Evaluates performance and writes:
  - `classification_report.txt` – sklearn classification report
  - `confusion_matrix_week3-4.png` – confusion matrix visualization

These outputs are saved into the `week3-4_baseline/` folder.

## 🗂 Expected project structure

A typical layout might look like:

```text
week3-4_baseline/
  ├─ baseline_confidence_classifier_week3-4.ipynb
  ├─ baseline_lr_tfidf.joblib
  ├─ best_model.joblib
  ├─ classification_report.txt
  └─ confusion_matrix_week3-4.png
```

Make sure the notebook paths match where your data and output folders live.

## ▶️ How to set up the environment

1. **Create and activate a virtual environment (optional but recommended)**

   ```bash
   python -m venv venv
   # Windows:
   venv\Scripts\activate
   # macOS / Linux:
   source venv/bin/activate
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements_week3-4.txt
   ```

3. **Launch Jupyter and open the notebook**

   ```bash
   jupyter notebook
   ```

   Then open `baseline_confidence_classifier_week3-4.ipynb` and run all cells.

## ✅ Python version

This notebook is expected to run with:

- Python 3.9+ (3.10/3.11 typically work as well)

## 🧪 Reproducibility notes

- If you change model types or add new models, update this README to reflect that.
- If you change file names for saved `.joblib` models or plots, be sure to update the notebook accordingly.
- For grading or sharing on GitHub, commit this README, the notebook, and **do not** commit large data files unless necessary (you can mention where to get them instead).
