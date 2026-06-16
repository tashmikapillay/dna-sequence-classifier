# DNA Sequence Classification using Recurrent Neural Networks

This project classifies 100 bp genomic windows by biological origin (Human, Bacteria, Virus, Plant) using a five-model comparison: a chance baseline, a classical k-mer model, a 1D CNN, an LSTM, and a Bidirectional LSTM. Sequences are sourced from NCBI RefSeq.

---

## Requirements

- Python 3.8+
- TensorFlow 2.x
- NumPy, Pandas, Matplotlib, Seaborn, scikit-learn

The dataset file `dna_dataset_refseq_L.csv` must be available before running.

---

## Running on Google Colab

1. Open [Google Colab](https://colab.research.google.com) and upload `703DNA_Project_Final.ipynb`, or open it directly from your Google Drive.

2. Upload `dna_dataset_refseq_L.csv` to the root of your Google Drive (My Drive), not inside any subfolder.

3. When the data loading cell runs, it will prompt you to authorise Drive access. Follow the on-screen link, sign in, and paste the authorisation code.

4. Run all cells in order: **Runtime > Run all**.

All required packages (TensorFlow, scikit-learn, etc.) are pre-installed in the Colab environment.

---

## Running Locally

1. Clone or download this repository.

2. Install dependencies:

   ```bash
   pip install tensorflow numpy pandas matplotlib seaborn scikit-learn
   ```

3. Place `dna_dataset_refseq_L.csv` in the same directory as the notebook.

4. Launch Jupyter:

   ```bash
   jupyter notebook 703DNA_Project_Final.ipynb
   ```

5. Run all cells in order: **Kernel > Restart & Run All**.

---

## Dataset

The notebook automatically searches for `dna_dataset_refseq_L.csv` in the following locations, in order:

1. The same directory as the notebook (local)
2. The root of Google Drive at `/content/drive/MyDrive/` (Colab)

If the file is not found in either location, the notebook will raise a `FileNotFoundError` with instructions.

---

## Reproducibility

A global seed of `42` is set for NumPy, TensorFlow, and Python's hash randomisation. Results should be consistent across runs given the same environment.
