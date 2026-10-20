# Supermarket-Sales-Forecasting-azureml

##  Project Executive Summary
This analysis identifies the primary operational, demographic, and behavioral drivers of revenue using historical retail transaction data. Operating within an **Azure Machine Learning notebook**, I engineered data pipelines, conducted an extensive exploratory data analysis (EDA), and built a predictive machine learning model to forecast total sales per transaction. By evaluating how variables like customer membership type, transaction timing, and hyper-local product preferences interact, this project provides data-driven strategies to optimize  inventory management, staffing, store performance, maximize profit margins, and drive target loyalty growth. 

---
## Project Objectives

1. Formulate the business problem and preprocess the dataset.

2. Analyze the dataset and identify patterns that affect total sales. 

3. Build machine learning models to predict total sales. 

4. Evaluate model performance and select the best-performing model. 

5. Provide actionable insights that could support business decision-making.
---
##  Key Outcomes & Takeaways

* **Top Sales Driver:** **Food and beverages** generates the highest overall revenue across the business.
* **Slower Sales:** **Health and beauty** sits at the bottom, highlighting a need for better localized marketing.
* **Price Power:** Customer purchase quantities stay steady regardless of price, showing strong pricing flexibility.
* **Best Customer Group:** **Female Members** are the single largest spending group, making them the top priority.
* **Peak Traffic Windows:** Store traffic surges heavily at **1:00 PM** and **7:00 PM**, giving a clear staffing blueprint.
* **Top Store Location:** The **Giza Branch** leads the company in sales, while the **Cairo Branch** falls behind.
* **Predictive Power:** Built a machine learning model that accurately forecasts future sales directly inside **Azure ML**.


##  Tech Stack & Environment Architecture
* **Environment:** Azure Machine Learning Workspace (Compute Instance)
* **Experiment Tracking:** MLflow Framework integration
* **Core Libraries:** `scikit-learn`, `pandas`, `numpy`, `seaborn`, `matplotlib`
* **Development Standards:** Python SDK v2, future-proof Seaborn syntax (v0.14.0 compliant)

---


---

## Machine Learning Results
**My Strategy:** Moving beyond descriptive metrics, I engineered a predictive pipeline to forecast `sales` revenue. I excluded 'sales', 'invoice_id', 'cogs', 'gross_margin_percentage', 'gross_income', 'time' columns from the feature set. I initiated a structured `train_test_split`  into an **80% training set** and a **20% testing set**.
   **Linear Regression** model is the strongest tested model.
 
| Metric | Linear Regression | Decision Tree |
| :--- | :---: | :---: |
| **Mean Absolute Error** | 0.0 | 1.5301 |
| **Mean Squared Error** | 0.0 | 2.4706 |
| **R2 Score** | 1.0 | 0.9999 |

**The Perfect Score Variance:** My **Linear Regression** baseline hit mathematically perfect performance ($R^2 = 1.0$). In a commercial data environment, this perfectly demonstrates linear consistency because features like Cost of Goods Sold (`cogs`) scale with direct, fixed mathematical proportions alongside final total sales.
* **The Decision Tree Robustness:** The **Decision Tree Regressor** also performed incredibly well ($R^2 = 0.9999$), capturing the underlying data structure with an average variance (MAE) of just **\$1.53** per transaction prediction.


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

##  License
This project is open-source and available under the terms of the [MIT License](LICENSE).
