
# 📘 Neural Confidence Journal Project (Weeks 1–10)
**Author:** Earnest Kyle  
**Course:** Deep Learning / NLP  
**Project:** Multi-Week Confidence Level Text Classification  

---

# ⭐ 1. Overview
This project analyzes **10 weeks of personal confidence journal entries**, training multiple NLP models to classify entries into:

- **0 = Low Confidence**
- **1 = Neutral Confidence**
- **2 = High Confidence**

The project progresses through increasingly advanced NLP approaches:

1. **Weeks 1–2** — EDA, TF–IDF, PCA, baseline visualizations  
2. **Weeks 3–4** — Logistic Regression TF–IDF classifier  
3. **Weeks 5–6** — Sentence embeddings + Feedforward Neural Network  
4. **Weeks 7–8** — DistilBERT fine‑tuning  
5. **Weeks 9–10** — Retraining DistilBERT on expanded dataset + final evaluation  

---

# ⭐ 2. Folder Structure
```
NEURAL-CONFIDENCE-JOURNAL/
│
├── reports/
│ ├── Final_Neural_Confidence_Journal_Report.pdf
│ ├── Neural_Confidence_Journal_Weeks1-4_Report.pdf
│ ├── Weeks_5-6_Progress_Report.pdf
│ ├── Week_7_8_Report.pdf
│ ├── Week9-10_Confidence_Report.pdf
│ └── (All progress reports delivered during the project)
│
├── week1-2_dataset/
│ ├── confidence_journal_eda.ipynb
│ ├── confidence_journal_week1-2.csv
│ ├── README_week1-2.md
│ └── requirements_week1-2.txt
│
├── week3-4_baseline/
│ ├── baseline_confidence_classifier_week3-4.ipynb
│ ├── classification_report.txt
│ ├── confusion_matrix_week3-4.png
│ ├── baseline_lr_tfidf.joblib
│ ├── best_model.joblib
│ └── README_week3-4.md
│
├── week5-6_embeddings/
│ ├── week5-6_embeddings_and_nn.ipynb
│ ├── ffnn_embeddings.keras
│ ├── metrics.txt
│ ├── preds_sample.csv
│ ├── confusion_matrix_week5-6.png
│ ├── requirements_week5-6.txt
│ └── README_week5-6.md
│
├── week7-8_distilbert/
│ ├── week7-8_distilbert_finetune.ipynb
│ ├── artifacts/
│ ├── model/
│ ├── confusion_matrix_distilbert_week7-8.png
│ ├── metrics.json
│ ├── val_predictions_distilbert.csv
│ └── README_week7-8.md
│
├── week9-10_dataset/
│ ├── confidence_journal_week9-10.csv
│ ├── week9-10_confidence_analysis_and_retraining.ipynb
│ ├── week9-10_confusion_matrix_using_old_model.png
│ ├── week9-10_confusion_matrix_using_new_model.png
│ ├── README_week9-10.md
│ └── requirements_week9-10.txt
│
├── requirements.txt
└── README.md
```

---

# ⭐ 3. Installation Instructions

## 3.1 Create Virtual Environment
```
python -m venv venv
source venv/bin/activate   # macOS / Linux
venv\Scripts\activate    # Windows
```

## 3.2 Install Dependencies
```
pip install -r requirements.txt
```

This installs all libraries needed for *every* week:
- PyTorch  
- TensorFlow  
- HuggingFace Transformers  
- Datasets  
- scikit‑learn  
- Matplotlib / Seaborn  
- Joblib  
- Jupyter Notebook  

---

# ⭐ 4. Running Each Notebook

## ✔ Week 1–2: EDA & First Visualizations
File: `week1-2_eda/confidence_journal_eda.ipynb`  
Includes:
- Data inspection  
- TF–IDF exploration  
- PCA scatter plot  
- Class distributions  
- Early confusion matrix  

---

## ✔ Week 3–4: Logistic Regression Baseline
File: `week3-4_baseline/baseline_confidence_classifier_week3-4.ipynb`  
Produces:
- TF–IDF vectorization  
- Logistic Regression model  
- Saved models (`joblib`)  
- Classification report  
- Confusion matrix  

---

## ✔ Week 5–6: Embeddings + Neural Network
File: `week5-6_embeddings/week5-6_embeddings_and_nn.ipynb`  
Steps:
- Generate sentence embeddings with `sentence-transformers`  
- Train FFNN in TensorFlow/Keras  
- Generate predictions, metrics, confusion matrix  

---

## ✔ Week 7–8: DistilBERT Fine-Tuning
File: `week7-8_distilbert/week7-8_distilbert_finetune.ipynb`  
Includes:
- DistilBERT tokenizer + model  
- Full fine‑tuning with HuggingFace Trainer  
- Metrics + confusion matrix  
- Saved model and tokenizer  

---

## ✔ Week 9–10: Retraining & Final Model
File: `week9-10_dataset/week9-10_confidence_analysis_and_retraining.ipynb`  
Features:
- Evaluation of old Week 7–8 model on Week 9–10 data  
- Retraining DistilBERT on combined data  
- Side-by-side comparison  
- New model confusion matrix (strong improvement)  
- Save final model for deployment  

---

# ⭐ 5. Results Summary

## 🔹 Week 1–2 Baseline Patterns
- PCA showed partially separable classes  
- Early predictions were weak but improved with TF–IDF models  

## 🔹 Week 3–4 Logistic Regression Results
- Accuracy improved significantly (~70–75%)  
- Neutral class predicted most accurately  

## 🔹 Week 5–6 Embeddings + FFNN
- Learned richer text semantics  
- Improved F1 scores over TF–IDF  

## 🔹 Week 7–8 DistilBERT Fine‑Tuning
- Performance increased dramatically  
- Strong contextual understanding  

## 🔹 Week 9–10 Retrained Final Model
New DistilBERT model achieved:
- **Accuracy ~ 96%**
- **Precision/Recall/F1: 94–98%**
- Only **4 misclassified** entries out of 89  
- Large improvement over older Week 7–8 model (55% accuracy)

This makes it the definitive final model.

---

# ⭐ 6. Dataset Description

Each dataset includes:
| Column | Meaning |
|--------|---------|
| `text` | Journal entry |
| `label` | Numeric confidence level |
| `label_name` | Text version of label |

Datasets are kept in their respective week folders.

---

# ⭐ 7. Reproducibility Notes

To re-run the entire project:

1. Clone/download repo  
2. Activate virtual environment  
3. Install dependencies  
4. Run notebooks *in chronological order*  
5. Ensure CSV inputs remain in expected folders  
6. For GPU acceleration (optional):  
```
pip install accelerate
```

---

# ⭐ 8. Loading the Final Model Programmatically
```python
from transformers import AutoModelForSequenceClassification, AutoTokenizer

model_path = "week9-10_dataset/week9-10_retrained_distilbert"
tokenizer = AutoTokenizer.from_pretrained(model_path)
model = AutoModelForSequenceClassification.from_pretrained(model_path)
```

---

# ⭐ 9. License
This project contains personal journal data.  
**Do not redistribute without permission.**

---

# ⭐ 10. Contact
**Earnest Kyle**  
earnest.kyle@ucdenver.edu
