# Supermarket-Sales-Forecasting-azureml
An end-to-end data science lifecycle project building building a predictive model for a supermarket to forecast total sales per transaction inside Azure ML Studio

## 🌟 Project Executive Summary
This analysis identifies the primary operational, demographic, and behavioral drivers of revenue using historical retail transaction data. Operating within an **Azure Machine Learning notebook**, I engineered data pipelines, conducted an extensive exploratory data analysis (EDA), and built a predictive machine learning model. By evaluating how variables like customer membership type, transaction timing, and hyper-local product preferences interact, this project provides data-driven strategies to optimize  inventory management, staffing, store performance, maximize profit margins, and drive target loyalty growth. 

---
## Project Objectives

1. Analyze the dataset and identify patterns that affect total sales. 

2. Build machine learning models to predict total sales. 

3. Evaluate model performance and select the best-performing model. 

4. Provide actionable insights that could support business decision-making.
---
## 🚀 Key Outcomes & Takeaways

* **Top Sales Driver:** **Food and beverages** generates our highest overall revenue across the business.
* **Slower Sales:** **Health and beauty** sits at the bottom, highlighting a need for better localized marketing.
* **Price Power:** Customer purchase quantities stay steady regardless of price, showing strong pricing flexibility.
* **Best Customer Group:** **Female Members** are our single largest spending group, making them our top priority.
* **Peak Traffic Windows:** Store traffic surges heavily at **1:00 PM** and **7:00 PM**, giving us a clear staffing blueprint.
* **Top Store Location:** The **Giza Branch** leads the company in sales, while the **Cairo Branch** falls behind.
* **Predictive Power:** Built a machine learning model that accurately forecasts future sales directly inside **Azure ML**.


## 🛠️ Tech Stack & Environment Architecture
* **Environment:** Azure Machine Learning Workspace (Compute Instance)
* **Experiment Tracking:** MLflow Framework integration
* **Core Libraries:** `scikit-learn`, `pandas`, `numpy`, `seaborn`, `matplotlib`
* **Development Standards:** Python SDK v2, future-proof Seaborn syntax (v0.14.0 compliant)

---

## 📈 Exploratory Data Analysis (EDA) & My Insights

### 1. Revenue Anchors by Product Line
* **My Objective:** I ranked product categories by gross volume to identify the baseline revenue anchors of the store.
* **My Finding:** I discovered that **Food and beverages** leads as our highest total sales driver, closely followed by **Sports and travel**. Conversely, **Health and beauty** sits at the bottom, indicating a clear gap in inventory moving power or localized marketing focus.

### 2. Purchase Volume vs. Transaction Value
* **My Objective:** I analyzed if our top-line growth relies on volume (bulk ordering) or value (premium item pricing).
* **My Finding:** The flat trendline reveals that consumer purchase quantity stays strictly between **1 and 10 units**, regardless of whether the unit price is \$10 or \$100. This tells me that demand is highly inelastic; increasing prices does not cause our purchase volumes to drop off.

### 3. Customer Demographic Spending Power
* **My Objective:** I segmented spending across loyalty statuses (`Member` vs. `Normal`) and gender identities to isolate our highest-value customer profiles.
* **My Finding:** I hit a massive insight here—**Female Members** represent our single most dominant customer segment, contributing over \$120,000 in total sales. This is nearly double the revenue of male members, showing where our loyalty program holds the strongest financial influence.

### 4. Daily Hourly Sales Velocity and Revenue Peaks
* **My Objective:** I mapped total sales over a 24-hour cycle to identify peak operational transaction windows.
* **My Finding:** I observed two distinct daily peaks: a mid-day surge around **13:00 (1 PM)** and an evening spike peaking sharply at **19:00 (7 PM)**. There is a noticeable operational valley between 16:00–17:00, which I can use to optimize staff scheduling and time flash promotions.

### 5. Regional Performance Scorecard
* **My Objective:** I aggregated total sales against customer satisfaction metrics to evaluate localized regional health.
* **My Finding:** My data shows **Naypyitaw (Giza Branch)** leads the company with **\$110,568.71** in total sales and the highest average transaction value (\$337.10). Meanwhile, **Mandalay (Cairo Branch)** lags behind in revenue and holds the lowest average customer rating (6.82/10), signaling a clear location-based service bottleneck.

### 6. Payment Channel Ticket Sizes
* **My Objective:** I used distribution box plots to evaluate if specific payment gateways structurally shift consumer basket size thresholds.
* **My Finding:** I noticed that the median, upper quartiles, and outlier distributions remain nearly identical across **Ewallet, Cash, and Credit cards**. This tells me that our payment types do not heavily dictate spending habits, giving us the flexibility to push digital processing options to save on cash handling.

### 7. Product Line Performance Across Store Branches
* **My Objective:** I mapped average transaction values across categories and branches side-by-side using a grouped bar chart to identify hyper-local product trends.
* **My Finding:** I found that specific branches dominate single categories; for example, **Cairo** holds a massive average basket size of **\$376.99** in *Health and beauty*, while **Giza** excels in *Food and beverages* at **\$360.10**. I can use this to strategically reallocate inventory styles to match local demand.

---

## Machine Learning Results
* **My Strategy:** Moving beyond descriptive metrics, I engineered a predictive pipeline to forecast `sales` revenue. I excluded 'sales', 'invoice_id', 'cogs', 'gross_margin_percentage', 'gross_income', 'time' columns from the feature set. I initiated a structured `train_test_split`  into an **80% training set** and a **20% testing set**.
*  **Scikit-Learn Linear Regression** model is the strongest tested model.
| Metric | Linear Regression | Decision Tree |
| :--- | :---: | :---: |
| **MAE** | 0.0 | 1.5301 |
| **RMSE** | 0.0 | 2.4706 |
| **R2 Score** | 1.0 | 0.9999 



---

## 📂 Project Structure
```text
├── outputs/                           # Directory generated for saved visual assets
│   ├── product_line_sales.png
│   ├── volume_vs_value_scatter.png
│   ├── customer_demographic_matrix.png
│   ├── hourly_sales_velocity.png
│   ├── regional_performance_scorecard.html
│   ├── payment_method_distribution.png
│   └── average_sales_product_branch_bars.png
├── azure_ml_sales_analysis.ipynb      # Main Azure ML execution notebook
├── LICENSE                            # MIT License file
└── README.md                          # Case study documentation
```

## 📜 License
This project is open-source and available under the terms of the [MIT License](LICENSE).
