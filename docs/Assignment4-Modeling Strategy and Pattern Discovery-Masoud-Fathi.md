# Data Sources
The main dataset is the “Samsung Mobile Sales Dataset” from Kaggle (2024). This public dataset is updated quarterly and includes over 1,000 rows from 2019 to 2024. It covers key variables for demand forecasting, such as Units Sold (target), Revenue, Market Share, 5G Capability, Regional 5G Coverage, 5G Subscribers, Average 5G Speed, Preference for 5G, Product Model, Year, Quarter, and Region. 

Right now, all data is external and comes from the public Kaggle release. In a real Samsung-led project, about 100 percent of the data would be internal, including SAP ERP sales transactions, Samsung Members device telemetry, supply-chain planning, component procurement logs, and carrier partnership reports. 

# Acquisition Plan

* The Kaggle dataset is downloaded once using the API (kaggle datasets download -d datatechexplorer/samsung-mobile-sales-dataset).
* Internal data is extracted every quarter from SAP HANA and Samsung’s data lake using secure ODBC connectors or Samsung’s internal APIs. The data is then loaded into Snowflake or Databricks.


# Modeling Strategy and Pattern Discovery

To extract meaningful patterns and generate reliable forecasts from the Samsung Mobile Sales Dataset, the modeling strategy must align with both the structure of the data and the overall business objective. The sales data is inherently time-dependent, influenced by pricing cycles, product releases, macroeconomic conditions, and competitive trends. Because of this temporal nature, time-series forecasting models such as ARIMA or Prophet are highly effective. These models can capture seasonality, long-term trends, and sudden shifts in demand. Prophet, in particular, handles holiday effects and irregular patterns well, which is useful for Samsung’s seasonally driven sales cycles (e.g., Black Friday, new device launches).

Using these models helps us achieve the most accurate long-range sales projections, enabling Samsung to optimize inventory, production planning, and marketing spend. For example, if Prophet detects an upcoming downward trend in a device category, the business can proactively adjust supply or introduce promotions. In short, the strength of time-series forecasting is its ability to use past patterns to reliably predict future performance, which is exactly the goal of this project.

Beyond forecasting, regression modeling plays a key role in identifying why sales behave the way they do. Regression helps quantify relationships between sales and external factors such as competitor pricing, inflation, interest rates, or promotional events. This is crucial because forecasting alone tells us what will happen; regression helps explain why it is happening. Understanding these causal relationships allows leadership teams to adjust strategic levers that influence demand.

Additionally, clustering methods (such as K-means or hierarchical clustering) help discover hidden structures in the data. For example, different geographic markets may behave similarly even if they appear unrelated at first glance. Clustering reveals these patterns, allowing Samsung to group similar markets for targeted marketing or pricing strategies. This is valuable in identifying market segments that have consistent buying behavior or predictable seasonal patterns.

## Why this combined strategy gives the best results

### This multi-model approach covers all important angles:

1. Time-series forecasting: future sales predictions

2. Regression analysis: impact of major drivers

3. Clustering: segmentation and pattern discovery

4. Integration of models: deeper and more actionable insights

> Together, they provide a complete understanding of both behavior over time and behavior across markets.

## Alternative modeling approaches

Several alternative models could be used, depending on data complexity and team experience:

1. **Machine learning forecasting models**

- Random Forest Regressor

- Gradient Boosted Trees (XGBoost, LightGBM)
> These can capture nonlinear patterns but require more data preprocessing and may be less interpretable.

2. **Deep learning models**

- LSTM (Long Short-Term Memory networks)

- Temporal Convolutional Networks
> These models perform extremely well on complex time-series but require larger datasets, computational resources, and more expertise.

3. **Classical statistical alternatives**

- Exponential Smoothing

- Holt-Winters
> Easier to implement but less flexible compared to Prophet or ARIMA.

4. **Market-basket or association models**
> Useful if analyzing which devices or accessories sell together.

*Overall, the selected strategy (time-series forecasting + regression + clustering) offers the strongest balance between accuracy, interpretability, and practicality, aligning perfectly with Samsung’s demand forecasting and strategic planning goals.*
