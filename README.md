# Customer Churn Prediction with Data Leakage Detection

MSc Data Science Project - University of the West of England

## Project Overview
This project demonstrates the critical importance of detecting and resolving data leakage in machine learning applications. Through analysis of 541,909 e-commerce transactions, we show how perfect 100% accuracy can be misleading and build a production-ready model with genuine predictive power.

## Key Results
- **Data Leakage Detected**: Initial 100% accuracy dropped to realistic 95.2% after removing temporal leakage
- **Hidden B2B Discovery**: Found 706 shopping baskets with up to 81 items (B2B customers)
- **Business Value**: 915% ROI with £400,596 net benefit
- **Production Model**: Gradient Boosting with 95.2% accuracy

## Project Notebooks

### [1. Exploratory Data Analysis](01_EDA_Analysis.ipynb)
- Dataset: 541,909 transactions from UCI Online Retail
- Data cleaning: Removed 24.93% missing CustomerIDs, handled returns
- Key discovery: 706 B2B transactions initially mistaken as duplicates
- Final dataset: 392,617 clean transactions (72.4% retention)

### [2. RFM Customer Segmentation](02_RFM_Segmentation.ipynb)
- Segmentation method: Quantile-based RFM analysis
- **Total customers analyzed: 3,212
- Created 8 balanced customer segments
- Key findings: Champions (0% churn), At Risk (56% churn), Lost (100% churn)
- Enables targeted retention strategies per segment

### [3. Churn Prediction Model](03_Churn_Prediction_Model.ipynb)
- **Data Leakage Analysis**: Detected Recency feature correlation of 0.86 with target
- **Model Comparison**: Logistic Regression, Random Forest, Gradient Boosting
- **Final Model Performance**:
  - Accuracy: 95.2%
  - Precision: 90.5%
  - Recall: 95.1%
  - ROI: 915%

## Business Impact
- Identifies 875 at-risk customers
- Saves 238 customers with targeted campaigns
- Net benefit: £400,596
- For every £1 spent, save £9.15

## How to Run
1. Install requirements: `pip install -r requirements.txt`
2. Run notebooks in order: EDA → RFM → Model
3. Data file: `customer_features.csv` (generated from EDA)

## Author
Pannita Marueang - MSc Data Science, UWE Bristol
