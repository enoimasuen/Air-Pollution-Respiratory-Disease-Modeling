# Air-Pollution-Respiratory-Disease-Modeling

This project investigates whether common air pollutants — including PM2.5, ozone, and volatile organic compounds — are predictive of chronic respiratory conditions (asthma and COPD) in the United States. By combining machine learning models with real-world data, we evaluate which environmental factors contribute most to elevated disease rates.

##  Problem Statement

Can county-level pollutant concentrations accurately predict areas with high prevalence of asthma and COPD?

##  Datasets Used
- **CDC**: County-level age-adjusted asthma and COPD prevalence (2021)
- **EPA**: Air Quality Index (AQI) and raw pollutant concentrations (e.g., PM2.5, ozone, benzene, acetaldehyde)
- **NBER**: Crosswalk file to match CBSA and FIPS codes for accurate geographic merging

##  Tools & Techniques
- Python, Pandas, NumPy, Seaborn, Matplotlib
- Scikit-learn: Random Forest, Logistic Regression, Linear Regression
- Data preprocessing: Normalization, missing value imputation, geographic merging
- Model evaluation: Accuracy, ROC AUC, confusion matrix, feature importance

##  Key Results

- **Random Forest Classifier**
  - Asthma: 76% accuracy | Top predictors: acetaldehyde, formaldehyde, benzene
  - COPD: 78% accuracy | Top predictors: acetaldehyde, formaldehyde, carbon tetrachloride

- **Logistic Regression**
  - Asthma: ROC AUC = 0.74
  - COPD: ROC AUC = 0.76

- **Linear Regression** performed poorly (R² < 0), reinforcing the need for non-linear models

##  Insights
- Volatile organic compounds (VOCs) like formaldehyde and acetaldehyde are highly predictive of high asthma and COPD prevalence.
- Diesel particulate matter and carbon tetrachloride showed complex associations, potentially influenced by regional or demographic factors.
- Random Forest models outperformed linear models and offered better generalization across diverse U.S. counties.

##  Repository Structure
/data/
├── asthma.csv # County-level asthma prevalence (CDC)

├── copd.csv # County-level COPD prevalence (CDC)

├── pollutant_data.csv # (from data_121847.csv) Air pollutant concentrations (e.g., VOCs, PM2.5)

├── aqi_by_cbsa.csv # (from daily_aqi_by_cbsa_2024.csv) Daily AQI readings by CBSA

└── cbsa_to_fips_mapping.csv # (from cbsa2fipsxw.csv) Geographic crosswalk for merging datasets


## Future Work
- Incorporate temporal pollution patterns (e.g., wildfire seasons, daily spikes)
- Add demographic covariates (income, race, smoking rates)
- Explore interpretable ML (e.g., SHAP values, L1-regularization)
- Test deep learning models for complex pollutant-disease interactions

## Authors
**Enoghayin Imasuen, Jan Tobias Boehnke, Megha Sharma**  
Harvard Extension School — Psychology & Data Science  


