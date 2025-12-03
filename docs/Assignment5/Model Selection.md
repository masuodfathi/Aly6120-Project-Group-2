# Why SARIMA
SARIMA is one of the most reliable and widely used time-series forecasting models because it captures three essential components of Samsung’s sales behavior:

### 1. Strong seasonality in smartphone demand

Samsung experiences predictable spikes around:

- New product launches (S-series, Z-series)

- Black Friday

- Holiday seasons

- Back-to-school periods

**SARIMA is designed specifically to detect repeating seasonal cycles and model them accurately (Hyndman & Athanasopoulos, 2021).**


### 2. Stable long-term patterns

Demand for high-end electronics typically follows:

- Multi-year life-cycles

- Slow-moving trends

- Recurring peaks and troughs

**SARIMA handles this type of stable structure extremely well.**


### 3. Interpretability matters for leadership

Executives care about clear explanations, not only accuracy.
SARIMA offers:

- Transparent model structure

- Easy-to-interpret parameters

- Forecasts that can be communicated directly in business terms

**This supports CRISP-DM’s requirement for models that can be understood and validated by business stakeholders (Bokrantz et al., 2023).**


### In simple words:

*SARIMA is perfect for the “normal” predictable part of Samsung’s demand — the patterns that repeat every year.*


# Why XGBoost?

While SARIMA handles stable, seasonal patterns, it cannot capture external drivers that have nonlinear effects. Samsung’s demand is often influenced by:

- Competitor launches (Apple iPhone release)

- Marketing campaigns

- Price discounts and bundles

- Economic indicators

- Supply-chain disruptions

- Retail channel performance

- Social media trends

**These relationships are not linear and not seasonal, which is exactly why XGBoost is needed.**


### 1. Handles complex, nonlinear relationships

XGBoost is a gradient-boosting model that learns:

- Interactions between variables

- Sudden demand jumps

- Irregular short-term spikes

- Unexpected changes in consumer behavior

**This is something SARIMA cannot do.**


### 2. Extremely strong predictive performance

XGBoost consistently ranks among the top-performing models in forecasting competitions (Makridakis et al., 2018). It is:

- Accurate

- Robust

- Fast

- Scalable

**Perfect for Samsung’s large dataset.**


### 3. Works with many types of data

XGBoost supports:

- Numerical features

- Categorical data

- Missing values

- Thousands of variables

**This flexibility matters because Samsung uses sales data, marketing data, competitor data, and manufacturing data—all from different sources.**


### In simple words:

*XGBoost captures the “unexpected” part of demand — rapid changes, promotions, competition, and real-world noise.*


### Why both together? (Perfect Combination)

Using SARIMA + XGBoost together gives Samsung:

#### 1. A stable baseline

(SARIMA: long-term, seasonal forecasts)

#### 2. A dynamic adjustment layer

(XGBoost: short-term spikes & nonlinear patterns)

#### 3. High overall accuracy

*Research strongly supports combining statistical + machine-learning methods for the best performance (Makridakis et al., 2018).*

#### 4. Business interpretability + technical power

A perfect mix for both executives and data scientists.


***SARIMA excels at capturing Samsung’s predictable seasonal sales cycles, offering interpretability and stability. XGBoost models complex, nonlinear factors like promotions, competition, and macroeconomic variables. Together, they deliver a forecasting system that is accurate, flexible, and aligned with CRISP-DM’s modeling expectations.***
