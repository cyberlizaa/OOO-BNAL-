Money Laundering Detection (AML) System
HSE University, Data Mining Course 2026


## Project Overview

This project focuses on identifying money laundering activities within financial transaction data. Using a dataset provided by IBM/HSE, we developed a comprehensive machine learning pipeline that cleans data, engineers features, and utilizes advanced algorithms to detect suspicious patterns.

The primary goal was to maximize the **Recall** metric to ensure that as many fraudulent transactions as possible are flagged for manual review by bank officers.

## Tech Stack

  - **Languages:** Python
  - **Libraries:** Pandas, NumPy, Scikit-learn, CatBoost, Matplotlib, Seaborn
  - **Tools:** Jupyter Notebook, HalvingGridSearchCV (for hyperparameter tuning)

## Key Features & Engineering

  - **Log Transformation:** Applied to transaction amounts to normalize highly skewed financial data.
  - **Categorical Encoding:** One-Hot Encoding for currencies and payment formats with `drop_first=True` to avoid multicollinearity.
  - **Entity Risk Analysis:** Identified high-risk entity types (e.g., Countries) and specific "criminal hubs" (accounts with 100% fraud rates).
  - **Threshold Optimization:** Adjusted classification thresholds (from 0.5 to 0.4) to prioritize fraud detection (Recall) over precision.

## Business Impact

By shifting the classification threshold to **0.4**, we reduced the number of missed fraud cases (**False Negatives**) by approximately **15-20%** compared to the baseline.
Assuming a regulatory fine of **$5,000** per missed case and a manual review cost of **$50** per alert, this model saves an estimated **$340,000+** on the test dataset.

