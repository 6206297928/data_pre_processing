# Network Traffic Data Cleaning & Preprocessing

This project demonstrates the cleaning and preprocessing of a network traffic dataset (e.g., CICIDS-like dataset). The dataset originally contains 79 features and one target label (`Label`) with missing values and mixed data types.

## Tasks Completed
- Loaded dataset with **pandas** and handled mixed data types.
- Converted categorical `Label` values into binary format (`BENIGN → 0`, `MALIGNANT/ATTACK → 1`).
- Checked and filled missing values using **Central Tendency (mean/median/mode)** depending on skewness:
  - If feature skewness < 0.5 → filled with **mean**.
  - If feature skewness ≥ 0.5 → filled with **median**.
  - For categorical → filled with **mode**.
- Reset dataset index after cleaning.
- Visualized feature distributions using **Seaborn & Matplotlib** (e.g., `distplot`, subplots).
- Saved cleaned dataset as a new CSV file for modeling.

