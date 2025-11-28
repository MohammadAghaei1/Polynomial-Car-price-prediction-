# 🚗 Used Car Price Prediction using Ensemble Learning

## 📌 Project Overview
This project aims to predict the selling price of used cars based on various features such as the car's present price, years of usage, fuel type, and transmission. By analyzing historical sales data, we built a robust regression pipeline to estimate vehicle value accurately. The final model utilizes a **Stacking Regressor** approach, combining the strengths of Linear Regression, Random Forest, and XGBoost.

## 🚀 Key Results
The **Stacking Regressor** (combining XGBoost, Random Forest, and Linear Regression) achieved the best performance on the test set.

| Model | R² Score (Test) | MSE (Test) | MAE (Test) |
| :--- | :---: | :---: | :---: |
| **Stacking Regressor** | **0.9601** | **0.73** | **0.62** |
| XGBoost Regressor | 0.9632 | 0.67 | - |
| Random Forest | 0.9240 | 1.39 | - |
| Linear Regression | 0.8287 | 3.15 | - |

> **Note:** The Stacking model provides a robust generalization by leveraging predictions from multiple base models.

## 🛠 Tech Stack
* **Language:** Python
* **Data Processing:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib (Heatmaps, Pairplots, Boxplots)
* **Machine Learning:** Scikit-learn (Linear Regression, Random Forest, Stacking), XGBoost
* **Feature Engineering:** Frequency Encoding, One-Hot Encoding, StandardScaler

## ⚙️ Methodology
1.  **Data Preprocessing:**
    * Handled duplicate records and performed extensive **Outlier Detection** (removing extreme prices and kilometers).
    * Applied **Frequency Encoding** for high-cardinality categorical features like `Car_Name`.
    * utilized **One-Hot Encoding** for categorical variables (`Fuel_Type`, `Seller_Type`, etc.).
    * Scaled numerical features using `StandardScaler` to improve model convergence.
2.  **Exploratory Data Analysis (EDA):**
    * Conducted Spearman correlation analysis to identify key price drivers (e.g., `Present_Price` vs `Selling_Price`).
    * Visualized data distributions and categorical relationships using Boxplots and Bar charts.
3.  **Modeling & Evaluation:**
    * Trained base models: **Linear Regression**, **Random Forest**, and **XGBoost**.
    * Implemented a **Stacking Regressor** to integrate base model predictions for superior accuracy.
    * Evaluated models using **MSE** (Mean Squared Error) and **R² Score**.
