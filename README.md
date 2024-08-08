# Commodity-Contract-Valuation
A Machine Learning Model that predicts the price of natural gas commodity and estimates the storage contract valuation. 

Project Overview

Natural gas is a vital component of the global energy market, and its price has a significant impact on various industries, including power generation, industrial manufacturing, and transportation. Accurate prediction of natural gas prices is crucial for businesses and investors to make informed decisions. This project aims to develop a machine learning model to predict natural gas prices using historical data and evaluate its performance. Additionally, a contract valuation function is created to estimate the value of a storage contract based on the predicted prices.

Objective

Natural gas prices are influenced by various factors, including supply and demand, weather conditions, global events, and economic indicators. Traditional methods of predicting natural gas prices rely on statistical models and expert opinions. However, these methods have limitations in capturing the complex relationships between the influencing factors. Machine learning algorithms, such as linear regression, can be used to analyze historical data and predict future prices.

Methodology

The project consists of two main components:
1.Natural Gas Price Prediction: A linear regression model is developed to predict natural gas prices using historical data.
2.Contract Valuation: A function is created to estimate the value of a storage contract based on the predicted prices.

Steps Involved

1.Data Collection
The project uses a Dataset containing historical natural gas prices and dates.

2.Data Processing
- The distribution of natural gas prices was visualized using a seaborn distribution plot.
- A scatter plot was created to visualize the relationship between dates and prices.
- A new feature was created by converting dates to ordinal values using the toordinal function. This allows the model to learn from the sequential nature of dates.

3.Model Building & Development
- Model Selection: Linear regression was chosen as a baseline model for price prediction due to its simplicity and interpretability.
- Train-Test Split: The data was split into 80% training and 20% testing sets for model evaluation.
- Model Training: The linear regression model was trained on the training data with "Date_Ordinal" as the only feature.
- Prediction: The model was used to predict prices on the testing data.

4.Model Evaluation
- Mean Squared Error (MSE): MSE was calculated to evaluate the model's prediction accuracy. Lower MSE indicates better performance. The MSE is displayed in the code output.
- R-squared (R²): R² was calculated to measure the proportion of variance in the target variable explained by the model. Higher R² indicates better model fit. The R² is displayed in the code output.
- Visualization: Predicted prices were visualized on a scatter plot alongside actual prices and training data to compare performance visually.

5.Contract Valuation Functionality
- User Input: The code prompts the user for injection and withdrawal dates, injection and withdrawal rates, maximum storage volume, fixed storage cost, and variable storage cost.
- Price Prediction: The model predicts purchase and selling prices based on the injection and withdrawal dates.
- Contract Valuation Calculation: A function contract_val calculates the estimated profit of the storage contract by subtracting the purchase cost, fixed storage cost, and variable storage cost (assuming a linear relationship) from the selling revenue. The function considers scenarios where the injection rate exceeds the maximum storage volume.

6.Results
The results of the project are as follows:

Natural Gas Price Prediction: The linear regression model achieves an MSE of 0.26 and an R-squared value of 0.28.
Contract Valuation: The contract valuation function estimates the value of the contract based on the predicted prices.

7.Discussion
The results show MSE of 0.26 which is compared to the price for MMBtu/day.  This project demonstrates a basic approach for natural gas price prediction using machine learning. The contract valuation functionality adds practical application to the price predictions. But Linear regression model is very basic and it might not be suitable when we consider other factors that can influence the natural gas price. For more refined model and accurate desired output, We should include the economic indicators, weather data, and news sentiments.

8.Conclusion
This project demonstrates the potential of machine learning algorithms in predicting natural gas prices and estimating the value of a storage contract. The results show that the linear regression model can accurately predict natural gas prices, and the contract valuation function provides a useful tool for businesses and investors.
