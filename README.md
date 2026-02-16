# 2026021701
access_resistance_project: Pore Blocking Ratio Calculation and Current Time-Domain Plot — using G5P6 as an example.
This repository contains a Jupyter Notebook (`T40.ipynb`) and custom Python modules (`pySNA.py`, `dbfload.py`) for analyzing single-channel nanopore or ion channel blocking events.

- **Supported data formats**: ABF (Axon Binary Format), HDF5, and DBF files  
- **Key features**: Baseline correction, event detection, and statistical analysis  

## 🛠️ Prerequisites
- Python 3.12+ ([download](https://www.python.org/downloads/))
- Jupyter Notebook (`pip install notebook`)
- (Optional) VS Code with Python extension for better editing experience  
  > Note: VS Code is a development tool and not required to run the code.

## ▶️ Quick Start
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
##Install dependencies:
pip install -r requirements.txt
##Launch Jupyter and open the notebook:
jupyter notebook
Then run T40.ipynb in your browser.
your-repo/
├── T40.ipynb          # Main analysis notebook
├── pySNA.py           # Core analysis logic
├── dbfload.py         # Custom DBF file reader
├── requirements.txt   # Exact package versions
└── README.md          # This file
📦 Dependencies
All dependencies are pinned in requirements.txt, including:
numpy, scipy → numerical computation
pandas → data handling
matplotlib, seaborn → visualization
h5py, hdf5plugin → HDF5 file support
pyabf → ABF electrophysiology data loading
