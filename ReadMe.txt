📊 Time Series Sales Forecasting for Favorita

This project focuses on forecasting unit sales for the Ecuadorian retailer Favorita, specifically for their locations in the Guayas region. The analysis and modeling are divided into two distinct Google Colab notebooks for clarity and 
efficient execution.

🎯 Project Goal

The primary objective is to build a robust time series model to accurately predict future unit sales, leveraging various related datasets to enhance predictive power.

📂 Repository Structure

The core of the project is contained within two main notebooks and the associated data files.

    Time_Series_Project_EDA.ipynb: This notebook contains the initial Exploratory Data Analysis (EDA), feature engineering, and the creation of the aggregated, pre-processed data used for modeling.

    Time_Series_Project_Forcasting.ipynb: This notebook focuses on the implementation, training, and evaluation of various Machine Learning (ML) forecasting models.

    oil.csv: Contains information on the price of oil, which may be a relevant external factor.

    sales_data.csv: Contains promotional and holiday information.

    sample.csv: A sample submission file structure for reference.

    stores.csv: Provides metadata about the various store locations.

    transactions.csv: Contains the number of transactions per store and day.

    (Note: The primary training data (train.csv) is too large for the repository and must be acquired separately. E.g. https://www.kaggle.com/datasets/siliconx/favoritagrocerysalesforecastingextracted?select=train.csv)

⚙️ Workflow and Preprocessing

The data preparation is strategically split between the two notebooks:

1. Time_Series_Project_EDA.ipynb (General Preprocessing)

This notebook handles the initial cleaning and merging of all external datasets (oil.csv, sales_data.csv, stores.csv, transactions.csv) with the main sales data.

    Feature Engineering: Creation of general time-based features (e.g., year, month, day of week).

    Data Aggregation: Combining the large raw data into a more manageable, time-series-friendly format.

    Output: The key output is a processed data file that includes all merged and engineered features, which is then loaded by the forecasting notebook.

2. Time_Series_Project_Forcasting.ipynb (Model-Specific Preprocessing)

This notebook loads the pre-processed data from the EDA step and applies transformations specific to the chosen ML model.

    Encoding: Handling categorical features (e.g., one-hot encoding).

    Scaling/Normalization: Applying scaling to numerical features.

    Time Series Preparation: Creating lagged features or other sequence-dependent data structures as required by the chosen model architecture (e.g., ARIMA, Prophet, or Deep Learning models).

🚀 Running the Project

    Obtain Data: Secure the main training dataset (train.csv) from the original source (e.g., the Kaggle competition associated with this dataset).

    Run EDA: Execute the Time_Series_Project_EDA.ipynb notebook first. This will perform the necessary data cleaning and feature generation and save the resultant file.

    Run Forecasting: Execute the Time_Series_Project_Forcasting.ipynb notebook. This notebook will load the file generated in Step 2 and proceed with model training and evaluation.