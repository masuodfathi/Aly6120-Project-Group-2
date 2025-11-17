# Data Understanding for Enhancing Demand Forecasting of Samsung Galaxy Smartphones

## Introduction

Samsung’s Galaxy smartphone division has faced recurring challenges in predicting global demand accurately, resulting in overproduction, missed sales, and inventory losses. To address this issue, the data-understanding phase of the CRISP-DM framework focuses on identifying and assessing the data required to build reliable forecasting models. This section defines the datasets, sources, and quality considerations essential for improving forecasting accuracy and operational agility.

## 1. Data Requirements and Rationale
To improve Samsung's demand forecasting with analytics and the CRISP-DM framework, it is important to use high-quality data sources. These sources should cover consumer behavior, supply chain activity, and market trends. The main requirements are:

Historical Sales Data: Collect weekly or monthly Galaxy sales numbers, regional details, product life cycles, and carrier or retailer data. This helps find trends like seasonality and demand patterns using models such as ARIMA or LSTM.
Supply Chain Data: Track component lead times, production capacity, inventory changes, shipments, and supplier costs or tariffs. This information helps model supply limits and prevent stock shortages or excess, which can save $5-7 billion in losses.
Market and Competitor Data: Use market share data (such as IDC), competitor product cycles like those of Apple or Xiaomi, carrier trends, and economic indicators like GDP or inflation. This helps adjust forecasts for sudden market changes.
Consumer Trends: Analyze search volumes, social media sentiment, pre-orders, reviews, and website clickstreams. Machine learning on this unstructured data can spot early changes in demand.
Marketing Data: Ad spends, promotions, discounts, and partnerships to isolate true demand and measure ROI, targeting 25% accuracy gains.
External Factors: Monitor tariffs, geopolitical events, regulations, and disruptions. This allows for proactive changes to inventory plans.
Governance and Quality: Use standard data formats, real-time ETL or ELT pipelines, and follow GDPR rules. This ensures data integrity and lowers the risk of fragmented information.
By bringing these elements together, Samsung can use AI to improve forecasting, lower inventory costs, and support growth in the high-end market.

## 2. Potential Data Sources

Internal data is obtained from Samsung's ERP systems, including SAP for sales records, and from Galaxy device telemetry via Samsung Knox. External data includes IDC's quarterly smartphone shipment trackers (idc.com), Statista's Galaxy sales data from 2010 to 2025 (statista.com), Counterpoint Research's AP-SoC market share reports (counterpointresearch.com), and Samsung's interim financial reports. Economic indicators, such as tariffs, are sourced from APIs like FRED (Federal Reserve Economic Data). These sources are selected for their recent 2025 data and comprehensive detail, as recommended by Leading in Analytics (Larson, 2019).

## 3. Key Data Sources

To fix Samsung’s forecasting problems, the most important data to collect is the information that shows what actually drives demand. First, historical sales data is essential because it reveals patterns by model, season, price, and region. Inventory and supply-chain data also matter since delays, shortages, and overstock directly affect how many phones reach the market on time.

External factors like inflation, tariffs, and overall market conditions help explain why demand rises or drops in certain countries, especially the U.S. and China. Customer-interest data—such as search trends, website visits, and social-media reactions—gives early signs of what people are excited about before sales happen.

Finally, knowing what competitors like Apple are doing and tracking Samsung’s own promotions help the team understand how launches, pricing, and marketing influence buying decisions. Together, these data elements give a complete picture of what shapes demand and where Samsung needs to adjust.

## 4. Data Governance and Quality Considerations

Strong governance ensures the data are trustworthy and usable. Following the Analytics Leader’s Data Quality Checklist (availability, acquisition cost, integrity, alignment) from the lecture (M3.pptx), Samsung must:

Guarantee that relevant ERP, marketing, and external feeds are accessible to authorized analysts.

Balance licensing costs against analytical value.

Validate integrity through checks for duplicates, missing entries, and inconsistent timestamps.

Align all data to consistent product identifiers and calendar periods.

Data cleaning and integration will employ ETL pipelines to correct errors, merge disparate systems, and create unified tables for modeling. Maintaining data lineage and documentation within a governance framework supports regulatory compliance and repeatability.


## References

https://counterpointresearch.com/en/insights/global-smartphone-apsoc-market-share-quarterly.
https://my.idc.com/getdoc.jsp?containerId=prUS53868725.
https://news.samsung.com/global/samsung-electronics-announces-first-quarter-2025-results.
https://www.statista.com/statistics/299144/samsung-smartphone-shipments-worldwide/.


