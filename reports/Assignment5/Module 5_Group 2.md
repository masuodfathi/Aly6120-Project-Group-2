# Part 1 Model Selection (SARIMA + XGBoost)

To support Samsung’s shift from hindsight-focused analytics to predictive foresight, this project applies two complementary forecasting models: Seasonal ARIMA (SARIMA) and Gradient Boosted Decision Trees (XGBoost). SARIMA is selected for its strength in modeling stable, recurring seasonal patterns in historical smartphone sales, such as demand spikes associated with flagship releases, holiday cycles, and regional promotions. These properties align with time-series forecasting principles emphasizing iterative refinement and seasonality (Hyndman & Athanasopoulos, 2021).

XGBoost complements SARIMA by capturing nonlinear relationships not explained by seasonality, including competitor actions, pricing strategies, marketing intensity, and macroeconomic factors. This dual-model approach aligns with the CRISP-DM Modeling phase, which encourages testing multiple techniques to determine the best business fit (Bokrantz et al., 2023).

# Part 2 How the Models Address the Business Problem

The chosen models help Samsung reach its business goals by making forecasts more accurate, cutting down on extra inventory, and helping the company respond quickly to the market. SARIMA gives a reliable and easy-to-understand forecast for long-term production and purchasing decisions. XGBoost helps Samsung react faster in the short term by capturing the factors that cause demand to change from week to week (Chen & Guestrin, 2016).

By using both models, Samsung’s leaders can look at different demand scenarios, measure supply-chain risks, avoid running out of stock, and keep less money tied up in extra parts. Research shows that combining statistical and machine-learning methods leads to better planning and stronger operations (Makridakis et al., 2018). This approach helps Samsung’s global supply chain work more smoothly, so executives can coordinate production, shipping, and marketing as things change.

# Part 3 Model Pros/Cons + Cross-Functional Collaboration

Predictive models such as logistic regression and decision trees offer complementary value within agile analytics. Logistic regression provides transparency and straightforward interpretability (Provost & Fawcett), but it assumes linear relationships and may underperform with complex interactions.

Decision trees capture non-linear patterns and are easy for stakeholders to understand, yet they risk overfitting and can become unstable with small data shifts (Collier; Saporito). Both models require strong data foundations to remain feasible and maintainable.

Building, validating, and refining these models depends on coordinated roles: data engineers to prepare reliable, iterative data pipelines; data scientists to design and tune the models; BI analysts to align outputs with decision needs; and domain experts to ensure business relevance. Agile leadership principles frequent feedback, cross-functional pairing, and adaptive planning support continuous model improvement and stakeholder trust.


# Part 4 Data Quality Risks & Pattern Identification

Data quality risks can affect how well the model performs, so they need to be identified early. The dataset may contain missing fields, inconsistent entries, or fragmented supply chain records, limiting a full view of product activity. Promotional periods can also create outliers that distort trends. Organizational constraints such as delayed updates, restricted access to source systems, and seasonal drift may further reduce model accuracy. Fixing these problems helps CRISP-DM meet its success criteria by making it more reliable and easier to understand.

Once these risks are managed, the model should reveal meaningful patterns such as seasonal demand cycles, promotion-driven lift, and regional performance differences. These insights strengthen the transition from business understanding to modeling by highlighting the underlying drivers that guide better decisions.

