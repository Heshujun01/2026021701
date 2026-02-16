# Nanopore Event Analysis: D10 Dataset

This repository contains the analysis pipeline for the **D10 dataset**, focusing on single-channel nanopore blocking events. The workflow processes raw electrophysiology data to compute **pore-blocking ratios** and their **voltage dependence**, generating statistical distributions and visualizations.

## 📌 Key Outputs from D10 Analysis
- Pore-blocking ratio distribution (histogram & KDE)
- Voltage-dependent pore-blocking ratio plot
- Processed event data saved as `.npz` files for downstream use

> ⚠️ **Note**: Raw data files (e.g., `.abf`, `.h5`) are not included due to size or sensitivity. You must provide your own D10 data.

---

## 1. System Requirements

### 📦 Software Dependencies (`requirements.txt`)
```txt
numpy==2.4.2
scipy==1.17.0
matplotlib==3.10.8
seaborn==0.13.2
pandas==3.0.0
h5py==3.15.1
hdf5plugin==6.0.0
pyabf==2.3.8
💻 Tested On
Python 3.12
Windows 11, Ubuntu 22.04
Standard desktop (Intel i5+, 16 GB RAM)
2. Installation
git clone https://github.com/Heshujun01/2026021701.git
cd 2026021701
pip install -r requirements.txt
jupyter notebook
Install time: ~2 minutes on a typical desktop.
3. Running D10 Analysis
🚀 Steps
Place your D10 raw data file(s) (e.g., D10_+40mV.abf, D10_+60mV.abf, etc.) in this directory.
Open D10(file_path).ipynb in Jupyter.
Update the file_path variable in the notebook to point to your data.
Run all cells sequentially.
🎯 Expected Output
A .npz file containing:
Event amplitudes and baselines → used to compute pore-blocking ratio = 1 - (event / baseline)
Applied voltage for each event
Two key plots:
Distribution of pore-blocking ratios (aggregated across voltages)
Pore-blocking ratio vs. applied voltage (showing voltage dependence)
⏱️ Runtime
~1–2 minutes on a standard desktop
4. Using Your Own Data
Replace the example file paths in D10(file_path).ipynb with your D10 data.
Ensure your data includes multiple voltage conditions (e.g., +40 mV, +60 mV, +80 mV) to enable voltage-dependence analysis.
The notebook automatically groups events by voltage and computes statistics.
🔁 The generated .npz file can be used in subsequent analyses (e.g., comparison with G6P4).
