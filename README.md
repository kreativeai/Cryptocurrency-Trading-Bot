# Building a Crypto Trading Bot using the Deep Learning Techniques

## Overview
This is the final project of my Data Science Bootcamp, a deep learning regression model is created to predict the future price of Bitcoin. The trading bot will then trade the Bitcoin according to the prediction.

## Architecture of the trading bot
!["architecture of the trading bot"](https://github.com/kreativeai/Cryptocurrency-Trading-Bot/blob/main/img/01_architecture.jpg)
Input the historial prices into the deep learning model, the trading bot trades the Bitcoin according to the prediction of the model.

## Deep Learning Model
!["deep learning model"](https://github.com/kreativeai/Cryptocurrency-Trading-Bot/blob/main/img/02_model.png)
(1) Load the hourly closing prices of Bitcoin

(2) Convert it to the sequences using the last 100 hours prices with some technical analysis indicators

(3) Pass the sequences into the LSTM model

(4) Predict the future prices for the next two hours

(5) Use the predicted prices as new indicators (DLI1 & DLI2) in the trading strategy


## Prediction Result of the Deep Learning Model

Apply the model to a test data set that the model never seen before for evaluation

!["prediction result"](https://github.com/kreativeai/Cryptocurrency-Trading-Bot/blob/main/img/03_prediction_test.png)


Train data RMSE:  483.00496357240803
Train data MSE:  233293.7948355832
Train data MAE:  352.86448464310223
-------------------------------------------------------------------------------------
Test data RMSE:  274.8333218903143
Test data MSE:  75533.35482126514
Test data MAE:  201.08360079225358
-------------------------------------------------------------------------------------
Train data R2 score: 0.9971042210015536
Test data R2 score: 0.9903749584415457
-------------------------------------------------------------------------------------
Train data Adj. R2 score: 0.9970639122738469
Test data Adj. R2 score: 0.9887944918473824

## Trading Strategy
!["trading strategy"](https://github.com/kreativeai/Cryptocurrency-Trading-Bot/blob/main/img/05_trading_strategy.png)

## Trading Result (Baseline 1: RSI Trading Strategy)
!["result rsi"](https://github.com/kreativeai/Cryptocurrency-Trading-Bot/blob/main/img/07_RSI_result.png)

## Trading Result (Baseline 2: SMA Crossover Trading Strategy)
!["result sma"](https://github.com/kreativeai/Cryptocurrency-Trading-Bot/blob/main/img/08_SMA_result.png)

## Trading Result (Trading bot based on the prediction of the Deep Learning Model)
!["result trading bot"](https://github.com/kreativeai/Cryptocurrency-Trading-Bot/blob/main/img/09_model_result.png)

## Conclusion
In this project, a profitable Crypto trading bot is developed to trade the Bitcoin according to the prediction of the deep learning model. It is planned to apply the model to other cryptocurrencies as a further study.

## Warning
THE MODEL AS WELL AS THE TRADING STRATEGY ARE USED FOR EDUCATIONAL PURPOSE ONLY, DO NOT USE IT IN THE PRODUCTION ENVIRONMENT, YOU LOSE YOUR MONEY!!!
