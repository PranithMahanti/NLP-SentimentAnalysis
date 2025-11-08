# NLP-SentimentAnalysis
## NIFTY50 Directional Prediction (1-Day Horizon)

This project builds a supervised ML pipeline to generate **discrete BUY / SELL / HOLD signals** for NIFTY50 based on 1-day price movement prediction.

## Objective
Predict next-day direction of NIFTY50. 
Get Discrete Trading Signals.


## Features
- Daily sentiment score (FinBERT)
- OHLC price data
- Lagged returns
- Volume-based features


## Models Implemented

| Model | Class |
|-------|-------|
| Logistic Regression | `sklearn.linear_model.LogisticRegression` |
| Random Forest | `sklearn.ensemble.RandomForestClassifier` |
| XGBoost | `xgboost.XGBClassifier` |
| Gradient Boosting | `sklearn.ensemble.GradientBoostingClassifier` |
| Support Vector Classifier | `sklearn.svm.SVC` |
| MLP Neural Network | `sklearn.neural_network.MLPClassifier` |


## Workflow
1) Load RSS articles > clean > FinBERT score  
2) Aggregate daily sentiment - `daily_sent`  
3) Download NIFTY50 using `yfinance`  
4) Merge with sentiment  
5) Create labels (`signal`)  
6) Train/test split  
7) Train ML models  
8) Evaluate and Compare 
9) Save best models  


## Evaluation Metrics
- Accuracy
- Precision / Recall
- F1-score
- Confusion Matrix
- Classification Report


## Installation

```bash
git clone https://github.com/PranithMahanti/NLP-SentimentAnalysis/
cd NLP-SentimentAnalysis/
pip install -r requirements.txt
```

## Author
(Pranith Mahanti) [https://github.com/PranithMahanti/]


