
# Zillow Home Value Prediction

## Project Overview
Zillow, the leading real estate and rental marketplace, empowers consumers with a comprehensive view of homeownership, including homes for sale, homes for rent, and off-market properties. Zillow’s Zestimate model estimates home values based on 7.5 million statistical and machine learning models that analyze hundreds of data points on each property. This project aims to enhance the accuracy of Zestimate by developing models to predict future sale prices, reducing the error margin, and improving the valuation process.

## Objective
The primary objective of this project is to leverage machine learning algorithms to predict the future sale prices of homes. By reducing the log-error in Zestimate predictions, this project will strive to make Zillow’s home value estimates more accurate.

### Required Libraries
To run these notebooks, you need to install the following libraries:
```bash
pip install pandas numpy seaborn matplotlib keras tensorflow xgboost lightgbm scikit-learn datetime scipy patsy
```

For xgboost installation instructions, refer to the official [xgboost documentation](http://xgboost.readthedocs.io/en/latest/build.html).

## Datasets
Before running any notebooks, download the datasets from [Kaggle Zillow Prize 1 Data](https://www.kaggle.com/c/zillow-prize-1/data). The primary files include:
- **properties_2016.csv**: Contains all property details for 2016. Note that some 2017 properties are included but may have incomplete data.
- **properties_2017.csv**: Contains all property details for 2017 (released on 10/2/2017).
- **train_2016.csv**: Training data with transactions from 1/1/2016 to 12/31/2016.
- **train_2017.csv**: Training data with transactions from 1/1/2017 to 9/15/2017.
- **sample_submission.csv**: A sample submission file to use for predictions on the test set.

## Project Notebook Execution Order
Run the notebooks in the following order to ensure proper workflow and data dependency:
1. `Project.ipynb`
2. `LinearRegression and Boosted Trees LightGBM.ipynb`
3. `Simple Neural Net.ipynb`
4. `LSTM Network.ipynb`
5. `Multivariate LSTM Network.ipynb`

## Prediction Target
The target prediction for this project is the **log-error** between Zillow’s Zestimate and the actual sale price. The log-error is calculated as follows:

\[
	ext{logerror} = \log(	ext{Zestimate}) - \log(	ext{SalePrice})
\]

The task involves predicting the log-error for several months in Fall 2017, with predictions used to evaluate Zestimate’s accuracy.


Predictions are needed for the following time points:
- **October 2016 (201610)**
- **November 2016 (201611)**
- **December 2016 (201612)**
- **October 2017 (201710)**
- **November 2017 (201711)**
- **December 2017 (201712)**

Properties sold multiple times within 31 days are evaluated based on the first valid transaction.

