# BERT and HMM POS Tagging Comparison

This project compares two POS tagging approaches:

- **BERT token classification** (`bert.ipynb`)
- **HMM baseline** (`HMM_Ver3.ipynb`)

It also includes a dedicated notebook for side-by-side metric comparison:

- **Evaluation notebook** (`evaluation.ipynb`)

---

## Project Files

- `bert.ipynb`: BERT-based POS tagging pipeline (PTB training/evaluation + CORD-19 analysis)
- `HMM_Ver3.ipynb`: HMM-based POS tagging baseline and PTB metrics
- `evaluation.ipynb`: Extracts saved notebook outputs and compares BERT vs HMM

---

## Recommended Execution Order

Run notebooks in this order so downstream comparisons can read saved outputs:

1. `bert.ipynb`
2. `HMM_Ver3.ipynb`
3. `evaluation.ipynb`

---

## What Each Notebook Produces

### `bert.ipynb`

- PTB token-level performance (accuracy, classification report)
- CORD-19 full-token analysis
- Frequency-filtered analysis
- Additional diagnostics (pattern and calibration analysis)
- Confusion matrix for **Gold (PTB) vs Predicted (BERT)**

### `HMM_Ver3.ipynb`

- PTB metrics for HMM baseline (e.g., token accuracy, macro F1)
- Confusion matrix and top confusion inspection

### `evaluation.ipynb`

- Unified comparison table for BERT vs HMM
- Metric bar chart
- Absolute and relative improvement summary

---

## Notes

- Some cells are computationally heavy (especially large-sample CORD-19 inference).
- If runtime is too long, reduce `sample_size` and/or `max_words_per_abs` in analysis sections.
- `evaluation.ipynb` relies on metrics already present in saved notebook outputs.

