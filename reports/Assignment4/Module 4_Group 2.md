## Data Sources
The main dataset is the “Samsung Mobile Sales Dataset” from Kaggle (2024). This public dataset is updated quarterly and includes over 1,000 rows from 2019 to 2024. It covers key variables for demand forecasting, such as Units Sold (target), Revenue, Market Share, 5G Capability, Regional 5G Coverage, 5G Subscribers, Average 5G Speed, Preference for 5G, Product Model, Year, Quarter, and Region.

Right now, all data is external and comes from the public Kaggle release. In a real Samsung-led project, about 100 percent of the data would be internal, including SAP ERP sales transactions, Samsung Members device telemetry, supply-chain planning, component procurement logs, and carrier partnership reports.

## How Data Would Be Acquired
The Kaggle dataset is downloaded once using the API (kaggle datasets download -d datatechexplorer/samsung-mobile-sales-dataset).
Internal data is extracted every quarter from SAP HANA and Samsung’s data lake using secure ODBC connectors or Samsung’s internal APIs. The data is then loaded into Snowflake or Databricks.

## Data Preparation & Quality Problems Fixed
The dataset was cleaned by removing about 640 duplicate rows and eliminating 49 rows with impossible negative market share. No missing values were found, but quality-flag columns were added for extreme revenue and units sold. A proper datetime index (Year + Quarter) was created for time-series modeling. New features were engineered, including an “Is_5G” flag and a composite 5G_Readiness_Score. Outliers were capped using the 1.5 IQR method. The final cleaned dataset contains roughly 360 reliable quarterly records ready for modeling.

## Models to Discover Meaningful Patterns
To uncover patterns and generate reliable forecasts from the Samsung Mobile Sales Dataset, the strategy combines time-series forecasting, regression analysis, and clustering techniques. Time-series models such as ARIMA or Prophet capture seasonality, product-release effects, and long-term trends, enabling accurate demand forecasting. Regression models help explain the impact of pricing, competitor behavior, and economic indicators, providing insight into why sales fluctuate. Clustering methods, such as K-means, identify groups of markets with similar sales behavior, supporting targeted planning. This approach balances accuracy and interpretability. Although advanced alternatives like gradient boosting or LSTMs exist, they introduce unnecessary complexity for this project’s scope.

## References
- Davenport, T. H., & Harris, J. G. (2007). Competing on analytics. Harvard Business School Press.
- Kaggle. (2024). Samsung mobile sales dataset. https://www.kaggle.com/datasets/datatechexplorer/samsung-mobile-sales-dataset
- Larson, B. J. (2019). Leading in analytics. Wiley.
- Hyndman, R. J., & Athanasopoulos, G. (2021). Forecasting: Principles and practice (3rd ed.). OTexts. https://otexts.com/fpp3/


