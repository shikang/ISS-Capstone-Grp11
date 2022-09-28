# Generative Deep Learning Models for Stock Price Prediction
Modified from [Stock Prediction using GAN](https://github.com/hungchun-lin/Stock-price-prediction-using-GAN/tree/master/Code)

---
## 1. Sign up Capital.com account


1. Visit [here](https://capital.com/api)
	1. Sign up
	2. Get API Key

## 2. Data Collection
1. Add your account login credentials and API key in *Get_Stock_Data.ipynb*
```
API_KEY = '<ENTER YOUR API KEY>'
API_LOGIN = '<ENTER YOUR LOGIN>'
API_PASS = '<ENTER YOUR PASSWORD>'
```
2. Add/Modify interested stocks you wish to include
```
STOCK_LIST = [
   EPIC_APPLE,
   EPIC_TESLA,
   EPIC_META,
   #...
]
```
3. Add/Modify interested FRED data you wish to include
```
FRED_LIST = [
    FRED_10_YR_TREASURY_CONST_MATURITY_MINUS_2_YR,
    FRED_10_YR_BREAKEVEN_INFLATION_RATE,
    #...
]
```
4. Run *Get_Stock_Data.ipynb*
5. Data will be saved as **Data.csv**

## 3. Preprocess Data
1. Run *Load_data.py*
2. Run *Data_preprocessing.py*

## 4. Model Training
1. Run *Train_WGAN_GP.ipynb*

## 5. Back Trading Test
1. Run *Back_Trading.ipynb*

## 6. Live Trading Test
1. Add your account login credentials and API key in *Test_Single_Day_Trade.ipynb*
```
API_KEY = '<ENTER YOUR API KEY>'
API_LOGIN = '<ENTER YOUR LOGIN>'
API_PASS = '<ENTER YOUR PASSWORD>'
```
2. Ensure the `STOCK_LIST` *array has the same values as the one you modified in Get_Stock_Data.ipynb*
```
STOCK_LIST = [
   EPIC_APPLE,
   EPIC_TESLA,
   EPIC_META,
   #...
]
```
3. Ensure the `FRED_LIST` *array has the same values as the one you modified in Get_Stock_Data.ipynb*
```
FRED_LIST = [
    FRED_10_YR_TREASURY_CONST_MATURITY_MINUS_2_YR,
    FRED_10_YR_BREAKEVEN_INFLATION_RATE,
    #...
]
```
4. Run *Test_Single_Day_Trade.ipynb*