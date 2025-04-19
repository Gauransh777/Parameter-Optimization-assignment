# SVM Optimization Assignment – UCI Letter Recognition Dataset

This project performs Support Vector Machine (SVM) optimization using 100 iterations across 10 randomly split samples (70% train / 30% test). The task is part of an academic assignment focused on comparing best accuracy and parameters per sample and analyzing convergence behavior.

---

## 📚 Dataset

- **Name**: [Letter Recognition Dataset](https://archive.ics.uci.edu/ml/datasets/Letter+Recognition)
- **Samples**: 20,000
- **Classes**: 26 (English capital letters A-Z)
- **Features**: 16 numeric features
- **Source**: UCI Machine Learning Repository

---

## ⚙️ Methodology

1. The dataset was encoded and split into 10 different 70-30 train-test splits (samples S1–S10).
2. For each sample:
   - 100 SVMs were trained using randomized hyperparameters (`kernel`, `C`, `gamma`, `degree`)
   - The **best performing model** was recorded with its accuracy and parameters
   - A **convergence graph** was plotted for the sample with **maximum accuracy**

---

## 📈 Results

### 📋 Final Accuracy Table

> Screenshot taken from notebook output after sorting accuracies:

![Final Results Table](results/image.png)

### 📊 Convergence Plot (Best Sample: S6)

> Accuracy over 100 iterations for best performing sample.

![Convergence Plot](graphs/convergence_best_sample.png)

---

## 🧠 Basic Data Analysis

- The **RBF kernel** consistently outperformed others across all samples.
- Best accuracy achieved: **97.95%** (Sample S6)
- Accuracy fluctuated due to random parameter selection, but top-performing configurations often had:
  - `C`: Between 4 and 6
  - `gamma`: `'auto'`
  - `degree`: N/A for non-poly kernels
"""
