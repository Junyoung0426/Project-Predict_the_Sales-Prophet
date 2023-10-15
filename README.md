# Project-Predict_the_Sales

## Introduction

This project is a data analysis and prediction project aimed at predicting the daily sales of stores. The project's goal is to develop a model to predict future sales based on given sales and related data.

## Data

- Dataset: [[Source or Link to Dataset]](https://www.kaggle.com/competitions/rossmann-store-sales/data)

- Data Format: CSV File

- Data Columns:
  - Id: An identifier representing a unique (Store, Date) combination within the test dataset.
   Store: A unique identifier for each store.

  - Sales: The target variable, representing the daily turnover for a store.

  - Customers: The number of customers in the store on a given day.

  - Open: An indicator for whether the store was open (0 = closed, 1 = open).

  - StateHoliday: An indicator of a state holiday. Values include "a" for public holidays, "b" for Easter holidays, "c" for Christmas, and "0" for no holiday.

  - SchoolHoliday: An indicator of whether the (Store, Date) was affected by the closure of public schools.

  - StoreType: Categorizes stores into different models, labeled as "a," "b," "c," or "d."

  - Assortment: Describes the assortment level, labeled as "a" for basic, "b" for extra, and "c" for extended.

  - CompetitionDistance: The distance in meters to the nearest competitor store.

  - CompetitionOpenSince[Month/Year]: Provides the approximate year and month when the nearest competitor store opened.

  - Promo: Indicates whether a store is running a promotion on a given day.

  - Promo2: A consecutive and continuing promotion for some stores (0 = not participating, 1 = participating).

  - Promo2Since[Year/Week]: Describes the year and calendar week when the store started participating in Promo2.

  - PromoInterval: Describes the consecutive intervals when Promo2 is started, specifying the months when the promotion begins.

## Project Structure

The project is structured into the following phases:

1. Data Loading: Load the provided dataset into Python and explore the data.

2. Data Preprocessing: Handle missing data, outliers, and duplicate entries, and transform the data into a time-series format.

3. Exploratory Data Analysis (EDA): Explore the data through distribution analysis, statistics, and visualization.

4. Time Series Modeling: Use the Prophet model to train and validate a sales prediction model.

5. Prediction and Visualization: Use the trained model to predict future daily sales and create visualizations.

## Results
I discussed time series analysis with .seasonal_decompose(), ACF and PCF plots and fitted forecasting model using a new procedure by Facebook Prophet.

- Advantages:
 - Time series forecasting is a powerful tool for capturing time dependencies, seasonal patterns, and holidays.
In our analysis, we employed the Facebook Prophet library, which allows for manual inclusion of holidays and special events.
- Drawbacks:
 - Time series forecasting methods do not inherently capture interactions with external features. In our dataset, variables like Promo and CompetitionOpen, which might improve forecasting accuracy, were not fully integrated.
 - The automation of ARIMA models, such as the one offered by Prophet, is still in development and may not be entirely stable.
 - A limitation of seasonal ARIMA models is that they require a dataset with a minimum of 4 to 5 complete seasons. This can be a challenge for new companies with limited historical data.
 - Tuning seasonal ARIMA models in Python can be cumbersome, as it involves adjusting 7 hyperparameters manually, which can significantly affect forecasting speed.
In summary, time series forecasting is a valuable tool, but its effectiveness depends on the quality and completeness of the data, as well as the specific forecasting method employed. Understanding the advantages and limitations of the chosen approach is crucial for accurate and reliable predictions.



## Usage

To run the project, follow these steps:

1. Download the code and data to your local environment.

2. Install the necessary Python packages.

3. Execute the Jupyter Notebook or Python script to start the project.

4. Review the results and visualizations.


