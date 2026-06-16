# 🧬 DNA Sequence Classification using Recurrent Neural Networks

This project classifies 100 bp genomic windows by biological origin (Human, Bacteria, Virus, Plant) using a five-model comparison: a chance baseline, a classical k-mer model, a 1D CNN, an LSTM, and a Bidirectional LSTM. Sequences are sourced from NCBI RefSeq.

---

## 🗂️ Repository Structure

```
.
├── DNA Sequence Classification.ipynb     # Main notebook — run this
├── dna_dataset_refseq_L.csv              # Dataset file (required before running)
└── README.md
```

---

## 🛠️ Requirements

The notebook runs on Python 3.8 or later. Install dependencies with:

```bash
pip install tensorflow numpy pandas matplotlib seaborn scikit-learn
```

The dataset file `dna_dataset_refseq_L.csv` must be available before running.

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)

1. Open [Google Colab](https://colab.research.google.com) and upload `DNA Sequence Classification.ipynb`, or open it directly from your Google Drive.
2. Upload `dna_dataset_refseq_L.csv` to the root of your Google Drive (My Drive), not inside any subfolder.
3. When the data loading cell runs, it will prompt you to authorise Drive access. Follow the on-screen link, sign in, and paste the authorisation code.
4. Run all cells in order: **Runtime → Run all**.

All required packages (TensorFlow, scikit-learn, etc.) are pre-installed in the Colab environment.

### Option 2 — Local Jupyter

1. Clone or download this repository.
2. Install dependencies (see Requirements above).
3. Place `dna_dataset_refseq_L.csv` in the same directory as the notebook.
4. Launch Jupyter and open the notebook:

```bash
jupyter notebook 703DNA_Project_Final.ipynb
```

5. Run all cells in order: **Kernel → Restart & Run All**.

---

## 📂 Dataset

The notebook automatically searches for `dna_dataset_refseq_L.csv` in the following locations, in order:

1. The same directory as the notebook (local)
2. The root of Google Drive at `/content/drive/MyDrive/` (Colab)

If the file is not found in either location, the notebook will raise a `FileNotFoundError` with instructions.

---

## 🔄 Pipeline Summary

| Stage | Detail |
|-------|--------|
| Baseline | Dummy Classifier (chance) |
| Classical | N-gram + Naïve Bayes (k-mer counts) |
| Deep (non-recurrent) | 1D CNN (local motif detection) |
| Recurrent | LSTM |
| Recurrent (bidirectional) | Bidirectional LSTM (reads both DNA strands) |

---

## 🔁 Reproducibility

A global seed of `42` is set for NumPy, TensorFlow, and Python's hash randomisation. Results should be consistent across runs given the same environment.
