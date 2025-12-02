# Week 5–6: Sentence Embeddings & Feedforward Neural Network

This notebook (`week5-6_embeddings_and_nn.ipynb`) extends the Neural Confidence Journal
project by moving from traditional TF–IDF features to dense **sentence embeddings**
combined with a **feedforward neural network (FFNN)** classifier.

The goal in Weeks 5–6 is to see whether richer text representations can improve
confidence-level prediction (Low / Neutral / High).

## 📌 What this notebook does

- Loads the labeled confidence journal entries
- Uses a pretrained sentence-transformer model to generate dense embeddings
  for each journal entry
- Splits the data into training and validation sets
- Builds and trains a feedforward neural network in TensorFlow / Keras
- Evaluates performance and saves:
  - `ffnn_embeddings.keras` – trained neural network model
  - `best_model.joblib` – optionally, best wrapper / metadata object
  - `confusion_matrix_week5-6.png` – confusion matrix visualization
  - `metrics.txt` – text file with accuracy / precision / recall / F1
  - `preds_sample.csv` – sample predictions for inspection

These outputs are written into the `week5-6_embeddings/` folder.

## 🗂 Expected project structure

A typical layout for this stage:

```text
week5-6_embeddings/
  ├─ week5-6_embeddings_and_nn.ipynb
  ├─ ffnn_embeddings.keras
  ├─ best_model.joblib
  ├─ confusion_matrix_week5-6.png
  ├─ metrics.txt
  ├─ preds_sample.csv
  └─ requirements_week5-6.txt
```

(You can rename `requirements_week5-6_new.txt` to `requirements_week5-6.txt`
when you place it in this folder.)

## ▶️ How to set up the environment

1. **Create and activate a virtual environment (recommended)**

   ```bash
   python -m venv venv
   # Windows:
   venv\Scripts\activate
   # macOS / Linux:
   source venv/bin/activate
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements_week5-6.txt
   ```

3. **Launch Jupyter and run the notebook**

   ```bash
   jupyter notebook
   ```

   Open `week5-6_embeddings_and_nn.ipynb` and run all cells in order.

## ✅ Python and library notes

- Recommended Python version: **3.9+**
- `tensorflow` and `sentence-transformers` can be heavy; a GPU is helpful but not required
  for small datasets.
- The exact sentence-transformer model name is defined inside the notebook; if you change it,
  results and runtime may differ.

## 🧪 Reproducibility tips

- If you adjust network architecture (layers, dropout, activation functions),
  update this README so it matches the current configuration.
- If you change output filenames (e.g., a different confusion matrix name),
  make sure both the notebook and this README stay in sync.
- For grading or GitHub sharing, commit this README and `requirements_week5-6.txt`
  along with the notebook; large model files (`.keras`, `.joblib`) can be
  optionally excluded via `.gitignore` if needed.
