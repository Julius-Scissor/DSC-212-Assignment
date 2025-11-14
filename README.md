# Karate Modularity Assignment

This repository contains a reproducible analysis for recursive spectral modularity partitioning of Zachary's Karate Club network. It produces visualizations after each accepted split and tracks node metric evolution across recursion iterations.

Contents
- DSC212_Karate_Modularity.ipynb - runnable Jupyter notebook that performs the full analysis, saves figures and CSVs to outputs/, and writes src/helpers.py so the helper module is included.
- src/helpers.py - helper functions for modularity spectral splitting and recursion (the notebook also writes this file when run).
- requirements.txt - Python package requirements.
- outputs/ - generated when you run the notebook/script (figures and CSVs).

How to use
1. Create a Python virtual environment and install requirements:
   python -m venv .venv
   source .venv/bin/activate    # macOS / Linux
   .venv\Scripts\activate       # Windows
   pip install -r requirements.txt

2. Open and run the notebook (recommended):
   jupyter notebook DSC212_Karate_Modularity.ipynb
   # or
   jupyter lab DSC212_Karate_Modularity.ipynb

   Running the notebook will:
   - perform recursive spectral modularity partitioning on the Karate graph,
   - save snapshot visualizations and per-iteration CSVs to the `outputs/` folder,
   - write `src/helpers.py` (identical helper code) so you can push that file to your repo directly.

What is implemented
- Recursive spectral partitioning using the leading eigenvector of a modularity matrix restricted to node sets.
- Splits accepted only if they produce positive modularity gain and both sides are non-empty.
- Snapshot visualizations after each accepted split (saved under outputs/).
- Per-node metrics (degree centrality, betweenness, closeness, clustering) stored per iteration and exported to CSV.
- Metric evolution line plots and boxplots.

Author
- Armaan-Singh
