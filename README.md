# Predicting Losses Due to Mis-Selling of Insurance Policies

This project aims to predict the **losses incurred by insurance companies** due to **mis-selling practices** in the Indian insurance sector, using data extracted and processed from **IRDAI reports** and applying machine learning models.

---

## 📂 Project Structure

- **Dataset:**  
  `Book2.xlsx` — Contains the final structured data with 9 key factors including Policies Issued, Premium Details, Grievances, Persistency Ratio, UBFPs Reported, and the generated Loss Due To Mis-Selling.
  
- **Model Code:**  
  `PredictingLosses_RandomForest.ipynb` — Jupyter Notebook with complete training, evaluation, and prediction workflow using machine learning.

---

## 🛠️ Technologies Used

- Python (Jupyter Notebook)
- Libraries:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - pygam (Generalized Additive Models)
- Excel for initial synthetic loss value generation
- IRDAI public datasets (Annual Reports)

---

## 📈 Approach

1. **Data Preparation:**
   - Extracted key insurance indicators like Renewal Premiums, Persistency Ratios, Grievances, and UBFPs from IRDAI reports.
   - Hypothetical target variable (`Loss_Due_To_Misselling`) generated using a weighted Excel formula considering all 9 features.

2. **Model Selection:**
   - Initially tested **XGBoost** for high accuracy but found it less interpretable for mathematical derivations.
   - Shifted to **Random Forest** based on evaluation metrics (**MSE** and **R²**) and better interpretability.
   
3. **Model Training:**
   - Features scaled using StandardScaler.
   - Random Forest model trained with smooth terms to capture non-linear patterns.
   - Feature effect visualizations plotted for interpretability.

4. **Prediction Workflow:**
   - New input data accepted from Excel files.
   - Predictions saved into a new Excel file for easy reporting.

---
