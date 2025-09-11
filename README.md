# Network Traffic Data Preprocessing

This repository contains **corrected preprocessing steps** for the network traffic dataset.  
An earlier version of the preprocessing notebook had mistakes — this `ipynb` is the **final, corrected version**.

---

## 📌 Dataset Description
- Total records: **20,496**
- Features: **79**
- Target column: **`Label`**
  - Encoded as **0 = BENIGN** and **1 = ATTACK**

---

## ✅ Preprocessing Steps
1. **Fixed column names** (removed extra spaces / duplicates like `' Label'`).
2. **Handled missing values**:
   - Identified columns with `NaN` (mainly `Flow Bytes/s`).
   - Filled missing values using **median** for skewed features.
3. **Label Encoding**:
   - Converted `BENIGN` → **0**,  
   - Attack types → **1**.
4. **Exploratory Data Analysis (EDA)**:
   - Distribution plots (`distplot`, histograms, KDE).
   - Class imbalance check (`countplot`).
5. **Saved cleaned dataset** to CSV for ML model building.

---

## 📊 Visualizations
- Class distribution bar chart.
- Histograms of traffic features (e.g., `Flow Duration`, `Flow Bytes/s`).
- Correlation heatmap for feature selection.

---

## 📂 Files
- `data_preprocessing_final.ipynb` → **Final preprocessing notebook**.
- `clean_data.csv` → Preprocessed dataset (ready for ML).

---


---

⚠️ **Note**: Ignore the older preprocessing notebook — it had label mis-encoding and unhandled missing values.
