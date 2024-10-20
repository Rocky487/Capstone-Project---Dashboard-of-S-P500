# Capstone
This project aims to create a monthly refreshable Tableau dashboard carrying useful info regarding S&P 500.

The useful info includes the following items:
1. Price trend of S&P 500 and its components (stocks) in the last 30 days
2. Growths of the stocks in the last 30 days
3. Safest and riskiest stocks by volatility
4. Weights of different GICS sectors
5. Predicted percentage return of S&P 500 for the current month

Be noted that a big part of this project is to made a prediction model for point 5. We first collect data and perform feature engineering and correlation analysis at ML_data_prep.ipynb, then load the dataset created to ML.ipynb for model building and evaluations. By loading the models created from ML.ipynb to Connect.ipynb, we can then make the prediction. For points 1-4, the data required is mainly collected using the yfinance API in Python. Capstone.twbx is our end product.

To explain the folders and files in this repository, data is the folder storing economic indicators that we fetched from the FRED webpages as the features used in ML_dat_prep.ipynb. sp500_dataset.csv is the preprocessed data derived from ML_data_prep.ipynb and used for model building in ML.ipynb. The models folder stores the models created from ML.ipynb, which are deployed in Connect.ipynb. Data Source Tables stores the tables derived from Connect.ipynb for the use of dashboard building in Tableau. If you want to run ML.ipynb successfully, please set it up in a Google Colab environment, with sp500_dataset.csv located in your own Colab Notebooks folder.

Visit this page if you want to see the end product directly:
https://public.tableau.com/app/profile/ming.chung.fong/viz/Capstone_17285382573660/Dashboard1

![Screenshot 2024-10-17 161428](https://github.com/user-attachments/assets/2f84ef7b-f2b5-4dc1-9bf9-eed5434ebff2)

My key takeaways from this project are:
1. Understanding the model building processes for linear, polynomial and XGBoost regressions
2. Realizing that a meta model can be derived from the prediction results from various different models
3. Using dashboard actions and Visibility Control in Tableau to make a dashboard lively
4. Different ways to rerun the codes at a defined frequency, such as GitHub actions, and their constraints
5. Different medias to load the dataframes from a Python script to be accessible by Tableau through live connection, or by Power Bi through direct query, such as ngrok and Google Cloud MySQL, and their constraints

The full report can be viewed here:

https://docs.google.com/document/d/1tGjnqrRIfKrV7SZu7Dp5_jepgVGVx_-YlcsrNCphQj8/edit?usp=sharing
