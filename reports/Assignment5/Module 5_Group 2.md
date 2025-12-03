# Part 1 Model Selection (SARIMA + XGBoost)

To support Samsung’s shift from hindsight-focused analytics to predictive foresight, this project applies two complementary forecasting models: Seasonal ARIMA (SARIMA) and Gradient Boosted Decision Trees (XGBoost). SARIMA is selected for its strength in modeling stable, recurring seasonal patterns in historical smartphone sales, such as demand spikes associated with flagship releases, holiday cycles, and regional promotions. These properties align with time-series forecasting principles emphasizing iterative refinement and seasonality (Hyndman & Athanasopoulos, 2021).

XGBoost complements SARIMA by capturing nonlinear relationships not explained by seasonality, including competitor actions, pricing strategies, marketing intensity, and macroeconomic factors. This dual-model approach aligns with the CRISP-DM Modeling phase, which encourages testing multiple techniques to determine the best business fit (Bokrantz et al., 2023).
