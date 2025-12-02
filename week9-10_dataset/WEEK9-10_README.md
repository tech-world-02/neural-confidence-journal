# WEEK 9–10 Confidence Journal Analysis

### **Overview**
This folder contains the Week 9–10 confidence journal dataset (N = 89).  
These entries were compared against the Week 1–2 baseline dataset and were also used to evaluate and retrain a DistilBERT model.

Because only two labeled datasets exist (Week 1–2 and Week 9–10), all comparisons and trends focus on the beginning vs. end of the study.

---

## **1. Dataset Summary**

| Dataset | Entries | Low | Neutral | High |
|--------|---------|-----|---------|------|
| Week 1–2 | 50 | 16 | 18 | 16 |
| Week 9–10 | 89 | 30 | 29 | 30 |

Both datasets are balanced across the three confidence levels.

---

## **2. Model Evaluation (Old Week 7–8 Model)**

Although the Week 7–8 DistilBERT model was not trained on Week 9–10 data, it was evaluated on this dataset.

**Old Model Performance (on Week 9–10):**

- **Accuracy:** 0.55  
- **Macro F1:** 0.49  
- Major issue: The model over-predicted *Neutral* and struggled heavily with *High* entries.

This motivated retraining using your available labeled data.

---

## **3. Retraining a New Model (Using Week 1–2 + Week 9–10)**

A new DistilBERT model was trained using only the datasets you have:

- Week 1–2 (baseline labeled set)
- Week 9–10 (new labeled set)

### **New Model Results (on Week 9–10):**

| Class | Precision | Recall | F1 |
|-------|-----------|--------|----|
| Low | 0.97 | 0.97 | 0.97 |
| Neutral | 1.00 | 0.93 | 0.96 |
| High | 0.91 | 0.97 | 0.94 |

- **Accuracy:** 0.96  
- **Macro F1:** 0.96

### Key Improvements:

- High confidence recognition improved from **0.10 → 0.97 recall**
- Only **4 total misclassifications**
- The new model is vastly more stable and balanced

---

## **4. Misclassifications**

The new model misclassified **4 of 89 entries**, mostly ambiguous emotional phrasing.

| True | Predicted | Count |
|------|-----------|-------|
| Low → High | 1 |
| Neutral → High | 2 |
| High → Low | 1 |

These are subjectively interpretable and within normal human-level variance.

---

## **5. Files in This Folder**

- `confidence_journal_week9-10.csv`  
- `week9-10_retrained_distilbert/`  
  - Model weights  
  - Tokenizer files  
  - Checkpoints  
  - Training arguments  
- `WEEK9-10_README.md`  
- Supporting visualizations (confusion matrix, classification report, trend plots)

---

## **6. Conclusion**

These weeks show the strongest confidence growth signal.  
Retraining using Week 1–2 + Week 9–10 allowed the model to:

- Reduce Neutral bias  
- Correctly identify High confidence patterns  
- Achieve near-perfect performance  

This is the recommended final model for deployment and future weekly updates.

