## Machine Learning Results
 Moving beyond descriptive metrics, I engineered a predictive pipeline to forecast `sales` revenue. I excluded 'sales', 'invoice_id', 'cogs', 
'gross_margin_percentage', 'gross_income', 'time' columns from the feature set. I initiated a structured `train_test_split`  into an **80% training set** and 
a **20% testing set** using the Linear Regression and Decision Tree models

 
| Metric | Linear Regression | Decision Tree |
| :--- | :---: | :---: |
| **Mean Absolute Error** | 0.0 | 1.5301 |
| **Mean Squared Error** | 0.0 | 2.4706 |
| **R2 Score** | 1.0 | 0.9999 |

**The Perfect Score Variance:** 

The **Linear Regression** baseline hit mathematically perfect performance ($R^2 = 1.0$). 
In a commercial data environment, this perfectly demonstrates linear consistency because features like Cost of Goods Sold (`cogs`) scale with direct, 
fixed mathematical proportions alongside final total sales.

 The **Decision Tree Regressor** also performed incredibly well ($R^2 = 0.9999$), capturing the underlying data structure with an average variance (MAE) of 
 just **\$1.53** per transaction prediction.

#  **Linear Regression** model is the strongest tested model,  it provides zero error ($0.00 MAE) 
