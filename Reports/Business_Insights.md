##  Exploratory Data Analysis (EDA) & My Insights

### 1. Revenue Anchors by Product Line
![Product Line Sales](https://github.com/ifejianyigrace31/Supermarket-Sales-Forecasting-azureml/blob/main/Outputs/product_line_sales.png?raw=true)

 I ranked product categories by gross volume to identify the baseline revenue anchors of the store.
* ** My Finding:** I discovered that **Food and beverages** leads as the highest total sales driver, closely followed by **Sports and travel**. Conversely, **Health and beauty** sits at the bottom, indicating a clear gap in inventory moving power or localized marketing focus.
----

### 2. Purchase Volume vs. Transaction Value
![](https://github.com/ifejianyigrace31/Supermarket-Sales-Forecasting-azureml/blob/main/Outputs/volume_vs_value_scatter.png?raw=true)

 I analyzed if the top-line growth relies on volume (bulk ordering) or value (premium item pricing).
* **My Finding:** The flat trendline reveals that consumer purchase quantity stays strictly between **1 and 10 units**, regardless of whether the unit price is \$10 or \$100. This shows that demand is highly inelastic; increasing prices does not cause our purchase volumes to drop off.

### 3. Customer Demographic Spending Power
![](https://github.com/ifejianyigrace31/Supermarket-Sales-Forecasting-azureml/blob/main/Outputs/customer_demographic_matrix.png?raw=true)

 I segmented spending across loyalty statuses (`Member` vs. `Normal`) and gender identities to isolate our highest-value customer profiles.
* **My Finding:** I hit a massive insight here—**Female Members** represent our single most dominant customer segment, contributing over \$120,000 in total sales. This is nearly double the revenue of male members, showing where our loyalty program holds the strongest financial influence.

### 4. Daily Hourly Sales Velocity and Revenue Peaks
![](https://github.com/ifejianyigrace31/Supermarket-Sales-Forecasting-azureml/blob/main/Outputs/hourly_sales_velocity.png?raw=true)

 I mapped total sales over a 24-hour cycle to identify peak operational transaction windows.
* **My Finding:** I observed two distinct daily peaks: a mid-day surge around **13:00 (1 PM)** and an evening spike peaking sharply at **19:00 (7 PM)**. There is a noticeable operational valley between 16:00–17:00, which can be used to optimize staff scheduling and time flash promotions.

### 5. Regional Performance Scorecard
![](https://github.com/ifejianyigrace31/Supermarket-Sales-Forecasting-azureml/blob/main/Outputs/regional_performance_scorecard.png)

 I aggregated total sales against customer satisfaction metrics to evaluate localized regional health.
* **My Finding:** the  data shows **Naypyitaw (Giza Branch)** leads the company with **\$110,568.71** in total sales and the highest average transaction value (\$337.10). Meanwhile, **Mandalay (Cairo Branch)** lags behind in revenue and holds the lowest average customer rating (6.82/10), signaling a clear location-based service bottleneck.

### 6. Payment Channel Ticket Sizes
![](https://github.com/ifejianyigrace31/Supermarket-Sales-Forecasting-azureml/blob/main/Outputs/payment_method_distribution.png)

 I used distribution box plots to evaluate if specific payment gateways structurally shift consumer basket size thresholds.
* **My Finding:** I noticed that the median, upper quartiles, and outlier distributions remain nearly identical across **Ewallet, Cash, and Credit cards**. This shows that the payment types do not heavily dictate spending habits, giving us the flexibility to push digital processing options to save on cash handling.

### 7. Product Line Performance Across Store Branches
![](https://github.com/ifejianyigrace31/Supermarket-Sales-Forecasting-azureml/blob/main/Outputs/average_sales_product_branch.png?raw=true)

 I mapped average transaction values across categories and branches side-by-side using a grouped bar chart to identify hyper-local product trends.
* **My Finding:** I found that specific branches dominate single categories; for example, **Cairo** holds a massive average basket size of **\$376.99** in *Health and beauty*, while **Giza** excels in *Food and beverages* at **\$360.10**. I can use this to strategically reallocate inventory styles to match local demand.
