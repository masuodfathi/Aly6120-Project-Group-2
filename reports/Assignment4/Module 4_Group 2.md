## Data Preparation Project

#1. Data Sources
The main data source is the “Samsung Mobile Sales Dataset” (Kaggle, 2024), 
which is a quarterly dataset with over 1,000 rows from 2019 to 2024. 
It includes key variables like Units Sold, Revenue, Market Share, 5G Capability, Regional 5G Coverage, 
Subscribers, Speed, Preference, and Region. For validation and benchmarking.


## 2. Internal vs. External
Right now, all data comes from extrnal sources, specifically the public Kaggle release. 
In an actual Samsung project, about 60–70% of the data would be internal, such as SAP ERP sales records, 
Samsung Members telemetry, supply chain planning, and procurement logs. The remaining 30–40% would be external 
tracking competitor activity, macroeconomic factors such as tariffs and GDP, and independent 5G rollout data that 
Samsung does not have internally.

## 3. How Data Would Be Acquired


## 4. Team Members to Collaborate With


## 5. Data Preparation & Quality Problems Fixed
The dataset was cleaned by removing about 640 duplicate rows and eliminating 49 rows with impossible negative market share. No missing values were found, but quality-flag columns were added for extreme revenue and units sold. A proper datetime index (Year + Quarter) was created for time-series modeling. New features were engineered, including an “Is_5G” flag and a composite 5G_Readiness_Score. Outliers were capped using the 1.5 IQR method. The final cleaned dataset contains roughly 360 reliable quarterly records ready for modeling.

## 6. Models to Discover Meaningful Patterns
To uncover patterns and generate reliable forecasts from the Samsung Mobile Sales Dataset, the strategy combines time-series forecasting, regression analysis, and clustering techniques. Time-series models such as ARIMA or Prophet capture seasonality, product-release effects, and long-term trends, enabling accurate demand forecasting. Regression models help explain the impact of pricing, competitor behavior, and economic indicators, providing insight into why sales fluctuate. Clustering methods, such as K-means, identify groups of markets with similar sales behavior, supporting targeted planning. This approach balances accuracy and interpretability. Although advanced alternatives like gradient boosting or LSTMs exist, they introduce unnecessary complexity for this project’s scope.

## References
- Davenport, T. H., & Harris, J. G. (2007). Competing on analytics. Harvard Business School Press.
- Kaggle. (2024). Samsung mobile sales dataset. https://www.kaggle.com/datasets/datatechexplorer/samsung-mobile-sales-dataset
- Larson, B. J. (2019). Leading in analytics. Wiley.
- Hyndman & Athanasopoulos (2021) → authoritative source for time-series models (ARIMA, seasonality, forecasting).


