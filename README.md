# Capstone
This project aims to create a monthly refreshable Tableau dashboard carrying useful info regarding S&P 500.

The useful info includes the following items:
1. Price trend of S&P 500 and its components (stocks) in the last 30 days
2. Growths of the stocks in the last 30 days
3. Safest and riskiest stocks by volatility
4. Weights of different BICS sectors
5. Predicted percentage return of S&P 500 for the current month

Be noted that a big part of this project is to made a prediction model for point 5. We first collect data and perform feature engineering and correlation analysis at ML_data_prep.ipynb, then load the dataset created to ML.ipynb for model building and evaluations. By loading the models created from ML.ipynb to Connect.ipynb, we can then make the prediction. For points 1-4, the data required is mainly collected using the yfinance API in Python. Capstone.twbx is our end product.

To run the codes successfully, please apply them in a Google Colab environment. Also, load the files in Raw data from FRED to a folder named "data" in your "Colab Notebooks" folder if you want to run ML_data_prep.ipynb; load the file from ML dataset to "Colab Notebooks" if you want to run ML.ipynb; load those from Models to "Colab Notebooks" if you want to run Connect.ipynb; and download the files from Data Source Tables for the data source of Capstone.twbx.
