# D# Advanced EDA & Feature Engineering Pipeline

An end-to-end automated data engineering pipeline designed to handle missing data strategies, extreme volatility mitigation (winsorization), dynamic interaction variable compilation, and multicollinearity purification over high-dimensional matrices.

This particular implementation leverages a programmatic domain simulation optimized for **Digital Marketing & E-Commerce Campaign Analytics**.

## Project Highlights
- **Chaotic Simulation Engine:** Generates data vectors across structural marketing KPIs containing multi-tier anomalies, non-random dropped states, and collinear parameters.
- **Robust Imputation Architecture:** Implements a layered approach utilizing stratified global parameters and a multi-dimensional K-Nearest Neighbors (5-NN) engine.
- **Outlier Neutralization:** Isolates volatile statistical tails by scaling data back into structural fences calculated through the Interquartile Range (IQR).
- **Eradication Matrix:** Computes upper-triangle correlation matrices to programmatically prune feature sets exceeding a strict threshold boundary (correlation > 0.80).

---

## File Manifest
- `DecodeLabs_Project1_Marketing_Variant.ipynb`: The complete automated pipeline structured to exact engineering compliance specifications.
- `marketing_campaign_clean_production.csv`: The polished, production-ready dataset exported following consolidation.

---

## Technical Architecture

### 1. Data Dimensions & Inputs
The initial chaotic data layer generates 1,200 unique records containing structural marketing metrics:
- `Ad_Spend_USD` (Gamma Distributed)
- `Total_Impressions` (Linear correlation to spend + Gaussian noise)
- `Link_Clicks` (Normally distributed with severe manual anomaly injection)
- `Marketing_Channel` (Nominal classes: Social Media, Search Ads, Email Promo)
- `Revenue_Generated` (The structural target dimension)

### 2. Strategic Transformations
- **Missing Data Resolution:** Rows with sparse categoricals are eliminated (<5% loss). The remaining fields are imputed sequentially using median mapping and numeric row-wise neighbor spaces via 5-NN.
- **Volatility Scaling:** Extremes are trimmed at the standard interquartile fences: [Q1 - 1.5 * IQR, Q3 + 1.5 * IQR]
- **Feature Interaction Generation:**
  - `Spend_Per_Click` = Ad_Spend_USD / (Link_Clicks + 1.0)
  - `Click_Through_Ratio` = Link_Clicks * Total_Impressions
  - `Spend_Deviation` = Ad_Spend_USD - Mean_Spend

---

## Local Environment Execution
To run this pipeline locally or inside your cloud compute container, ensure you have the required statistical and engineering dependencies installed:

```bash
pip install pandas numpy scikit-learn
ecodelab.project
