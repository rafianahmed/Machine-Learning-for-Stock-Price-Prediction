# Machine-Learning-for-Stock-Price-Prediction

Skillsets Used and Outcome
1. Skillsets and Techniques Used
1.1 Data Preprocessing and Feature Engineering

Data loading: CSV data containing columns like Date, Symbol, Adj Close, Close, High, Low, Open, and Volume was loaded into a pandas DataFrame.
Feature Engineering: Additional features like 7-day and 30-day moving averages (MA_7, MA_30), percentage change (Pct_Change), and 30-day volatility (Volatility_30) were created to capture trends and volatility in stock prices. These features were key in making the prediction models more robust.
1.2 Regression Modeling

Linear Regression:
Used for predicting stock prices based on engineered features.
Evaluation metric: Mean Squared Error (MSE), with the model yielding a relatively high error value of 68,074.13, indicating significant variability in stock price prediction.
1.3 Bayesian Methods and Probability Theory

Bayesian Inference:
Bayesian updating was applied for probabilistic stock price prediction using the prior and likelihood distributions.
The posterior distribution was calculated based on historical stock prices, yielding a predicted stock price of 99.59 using the Bayesian posterior mean.
1.4 Gaussian Mixture Model (GMM) with Expectation-Maximization (EM)

GMM for Clustering:
Gaussian Mixture Models were used to cluster stocks based on features like adjusted close prices and volatility.
The GMM model identified 3 distinct clusters of stocks:
Cluster 1: Mean adjusted close price ~ 82.72, mean volatility ~ 103.03.
Cluster 2: Mean adjusted close price ~ 934.68, mean volatility ~ 223.22.
Cluster 3: Mean adjusted close price ~ 184.45, mean volatility ~ 398.43.
Covariance matrices for each Gaussian component were computed, indicating how prices and volatility vary together within each cluster.
1.5 Deep Learning (LSTM)

LSTM Neural Network:
A Long Short-Term Memory (LSTM) network was employed to predict stock prices based on historical price sequences.
Network Architecture:
Input layer: Sequence length of 60 time steps, with 50 LSTM units.
Dropout layers: Used to prevent overfitting.
Dense output layer: Predicting a single stock price at each time step.
The Root Mean Squared Error (RMSE) from the LSTM model was 85.71, showing that the neural network provided reasonable predictions for future stock prices.
2. Outcome and Analysis
2.1 Stock Price Prediction

Regression: The linear regression model had a relatively high error rate (MSE: 68,074.13), which suggests that a simple linear model might not capture the complexity of stock market data.
Bayesian Inference: Provided a probabilistic stock price prediction of 99.59, which can be a useful range for making decisions based on confidence intervals.
LSTM Model: Predicted stock prices like 95.51, 124.44, and 66.57 with a reasonably low RMSE of 85.71. LSTM models are particularly good at capturing time-dependent patterns, hence their lower error rate compared to linear regression.
2.2 Clustering Analysis (GMM)

Stock Clusters:
Cluster 1: Represents stocks with moderate prices and volatility.
Cluster 2: Represents high-value stocks with relatively lower volatility.
Cluster 3: Represents medium-priced stocks with high volatility.
This clustering helps investors identify stocks that share similar statistical properties, aiding in portfolio diversification or risk management.
Conclusion and Recommendations
The combination of regression, Bayesian methods, and deep learning provided a multi-faceted approach to stock prediction, each yielding insights into different aspects of the data.
The LSTM model performed best in predicting future prices due to its ability to model temporal dependencies, while Bayesian methods provided a probabilistic framework for understanding uncertainties.
GMM clustering offered valuable insights into stock groupings, which could be used for targeted investment strategies based on price volatility and market behavior.
