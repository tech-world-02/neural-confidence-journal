# Week 1–2 Confidence Journal – EDA & Baseline Exploration

This notebook (`confidence_journal_eda.ipynb`) performs exploratory data analysis (EDA) and 
basic visualization for the Neural Confidence Journal project using the Week 1–2 dataset.

## 📌 What this notebook does

- Loads the Week 1–2 confidence journal CSV data
- Cleans and inspects the text and label distributions
- Plots:
  - Label counts (Low / Neutral / High)
  - Word frequency and word clouds
  - Additional EDA charts using Seaborn and Matplotlib

This notebook focuses on understanding the dataset structure and confidence label behavior 
for Weeks 1–2 and prepares the ground for later modeling notebooks.

## 🗂 Files

- `confidence_journal_eda.ipynb` – main EDA notebook
- `requirements_week1-2.txt` – Python dependencies for this notebook
- `confidence_journal_week1-2.csv` – (expected) input CSV file with columns such as:
  - `text` – journal entry
  - `label` – numeric label (0 = Low, 1 = Neutral, 2 = High)

Make sure the CSV file path in the notebook matches where your data is stored.

## ▶️ How to set up the environment

1. **Create and activate a virtual environment (optional but recommended)**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements_week1-2.txt
   ```

3. **Launch Jupyter and open the notebook**

   ```bash
   jupyter notebook
   ```

   Then open `confidence_journal_eda.ipynb` and run all cells.

## ✅ Python version

This notebook is expected to run with:

- Python 3.9+ (3.10/3.11 also typically work)

## 🧪 Reproducibility notes

- If you add or change visualizations, update this README accordingly.
- If you rename the CSV file or move it, be sure to adjust the file path in the notebook.
- For consistent plots and behavior, ensure you have the same library versions installed as in `requirements_week1-2.txt`.

