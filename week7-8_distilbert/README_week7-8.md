
# Week 7–8: DistilBERT Fine-Tuning Project

This module contains the full workflow for training, validating, and evaluating a DistilBERT transformer model on the Confidence Journal dataset (Low / Neutral / High confidence classes). 
This week represents a major upgrade from traditional ML models (Weeks 1–6), transitioning to state-of-the-art NLP using Hugging Face Transformers.

## Project Structure

```
week7-8_distilbert/
│
├── artifacts/
│   ├── tokenizer/
│   ├── trainer_state.json
│   └── checkpoints/
│
├── model/
│   ├── config.json
│   ├── pytorch_model.bin
│   └── tokenizer_config.json
│
├── confusion_matrix_distilbert_week7-8.png
├── metrics.json
├── val_predictions_distilbert.csv
├── week7-8_distilbert_finetune.ipynb
└── README.md
```

## Objective

The goal of Week 7–8 was to:

- Fine-tune DistilBERT on the journal entries dataset  
- Predict confidence levels: **0 = Low, 1 = Neutral, 2 = High**  
- Evaluate performance, produce metrics, and analyze misclassifications  

This is the strongest baseline prior to Week 9–10 retraining.

## Environment Requirements

See requirements_week7-8.txt or install:

```
pip install -r requirements_week7-8.txt
```

## How to Run

1. Install dependencies  
2. Open the notebook  
3. Run the full training pipeline  

### Steps Performed

- Load dataset  
- Tokenize using DistilBERT tokenizer  
- Fine-tune using HuggingFace Trainer  
- Evaluate model  
- Save model + tokenizer  
- Generate confusion matrix + metrics  

## Results

Full evaluation results appear in `metrics.json`.

A confusion matrix is included:  
`confusion_matrix_distilbert_week7-8.png`

## Key Takeaways

- DistilBERT significantly outperforms TF-IDF baselines  
- Captures deeper semantic/language patterns  
- Prepares foundation for Week 9–10 combined retraining  
