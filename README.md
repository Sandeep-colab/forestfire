🔥 Algerian Forest Fires Analysis
This project performs data cleaning, exploratory data analysis (EDA), and visualization on the Algerian Forest Fires Dataset. The goal is to understand the distribution and correlation of fire-related variables and gain insight into the conditions associated with forest fires in two Algerian regions.

📁 Dataset
File: Algerian_forest_fires_dataset_UPDATE.csv

Contains meteorological and fire occurrence data for two regions in Algeria: Béjaïa (Region 0) and Sidi Bel-Abbès (Region 1).

Features include temperature, humidity, wind speed, FFMC, DMC, DC, ISI, BUI, FWI, and class labels indicating whether a fire occurred.

🧹 Data Cleaning Steps
Removed null values and corrected column names with leading/trailing whitespace.

Converted appropriate columns to correct data types (int or float).

Dropped a corrupted or irrelevant row at index 122.

Re-encoded the categorical Classes column into binary (0 = not fire, 1 = fire).

Saved a cleaned version as Algerian_forest_fires_cleaned_dataset.csv.

📊 Exploratory Data Analysis (EDA)
Class Distribution

Pie chart showing the proportion of fire vs. non-fire days.

Histograms

Plotted for each feature to understand their distribution.

Correlation Matrix

Heatmap to analyze correlation between features and fire occurrence.

Boxplot

Used to detect outliers in FWI (Fire Weather Index).

Regional Fire Analysis

Fire occurrence by month for:

Béjaïa (Region 0)

Sidi Bel-Abbès (Region 1)

📈 Visualizations
Pie Chart for fire vs. non-fire percentages.

Histograms for all numerical features.

Heatmap showing feature correlation.

Monthly fire count barplots for both regions.

🧪 Tech Stack
Python 🐍

Libraries:

pandas

numpy

seaborn

matplotlib

📈 Machine Learning Pipeline
🔹 Target Variable:
FWI (Fire Weather Index)

🔹 Feature Engineering:
Feature selection based on correlation threshold (> 0.85).

Standardization using StandardScaler.

🔹 Models Used:
Model	Tool	Regularization	Cross-validation
Linear Regression	LinearRegression	No	❌
Lasso Regression	Lasso, LassoCV	L1	✅
Ridge Regression	Ridge, RidgeCV	L2	✅
ElasticNet	ElasticNet, ElasticNetCV	L1 + L2	✅

Each model's performance was evaluated using:

Mean Absolute Error (MAE)

R² Score


forestfire/
│
├── Algerian_forest_fires_dataset_UPDATE.csv
├── Algerian_forest_fires_cleaned_dataset.csv
├── scaler.pkl
├── ridge.pkl
├── EDA_script.py / notebook.ipynb
├── README.md
└── requirements.txt (optional)
