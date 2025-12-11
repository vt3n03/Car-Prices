# Car Price Analysis and Prediction
This project explores a large dataset of vehicle listings and builds a machine learning model to predict car prices. The work includes data exploration, cleaning, visualization, feature engineering, and training a Random Forest regression model.

# Project Overview
The goal is to understand which factors influence car prices and to create a model that can predict price based on vehicle features such as year, odometer, fuel type, manufacturer, and more.

The project uses a dataset of over four hundred thousand vehicle listings, which contains both numerical and categorical information along with substantial missing data. The workflow focuses on cleaning the dataset, identifying meaningful patterns, and building a predictive model.



# Main Steps
1. Data Loading and Inspection

The dataset is loaded from the project’s ```input/``` directory and basic structure information is displayed. This includes the number of rows and columns, the names of all features, counts of unique values, and summary statistics.

2. Handling Missing Data

A function is used to filter out columns with more than forty percent missing values. This helps remove variables that would not meaningfully contribute to the model.

3. Outlier Removal

Several cleaning rules are applied to make the dataset realistic and suitable for modeling:

- Price is restricted to a defined range to remove extreme or invalid listing values.

- Statistical outliers are removed using the IQR method.

- Additional filters limit the year and odometer readings to plausible values.

These steps reduce noise and improve model performance.

4. Feature Selection

Columns unrelated to prediction or too inconsistent for use are removed. These include URLs, text descriptions, VIN numbers, and other fields that do not directly contribute to price prediction.

5. Exploratory Data Analysis

Visualizations are used to understand relationships within the dataset:

- A correlation heatmap shows how numerical variables relate to price and to each other.

- Bar charts show the distribution of manufacturers and vehicle types.

These plots reveal which variables carry the most useful information.

6. Encoding Categorical Data

Categorical features such as manufacturer, fuel type, transmission, and drive type are converted into numerical dummy variables. This allows machine learning algorithms to use these features.

7. Scaling and Model Training

All features are standardized to ensure fair weighting in the model.
A Random Forest Regressor is then trained using a train test split.
Performance is measured with mean absolute error and the model’s score on the test set.

8. Feature Importance

The most influential features in predicting price are visualized. This highlights which attributes matter most, such as year, odometer, manufacturer, and fuel type.

# Results

- The Random Forest model produces a measurable prediction error and captures the major patterns in the dataset.

- Visual analysis helps reveal realistic price ranges and meaningful trends in the data.

- Feature importance shows that both numerical and categorical attributes strongly influence pricing.

# Tools and Libraries

- Python

- NumPy

- Pandas

- Matplotlib

- Seaborn

- Scikit-learn

- Jupyter Notebook

