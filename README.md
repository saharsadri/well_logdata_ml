# well_logdata_ml
# Well-log ML dataset preparation: manual depth alignment (core plugs → logs)

This repository contains code and example data used in the study:

**Machine Learning Approaches for Core Porosity Prediction Using Well Log Data**  
(Manuscript in preparation / submitted)

The main component is a Jupyter notebook that performs **manual depth alignment (warping)** between
core plug porosity measurements and well log depths, and exports an aligned dataset for machine learning.

---

## Contents
- `Depth_alignment.ipynb`  
  Notebook for manual depth alignment and warping using user-defined tie points.
- `data/IJS-57.csv`  
  Example well log data (open-source).
- `data/IJS-57_coreplug_averaged.csv`  
  Core plug porosity data for the same well (open-source).

---

## What the notebook does
1. Splits the data into **depth chunks** where the depth gap is > 3 m.
2. Lets the user define **tie points** (Core@ depth → Log depth).
3. Applies **warping** when multiple ties are provided in a chunk (depth correction varies smoothly between ties).
4. Allows exporting the **selected aligned chunks** to create an ML-ready dataset.

---

## How to run
### 1) Install Python packages
```bash
pip install -r requirements.txt
