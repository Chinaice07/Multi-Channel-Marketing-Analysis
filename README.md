# Multi-Channel Marketing Analysis

## 📌 Project Overview
This project explores the impact of various promotional budgets (TV, Radio, Social Media, and Influencers) on company sales. Using Python and Multiple Linear Regression, the goal is to identify which marketing channels are statistically significant drivers of revenue and to provide actionable recommendations for budget optimization. Through thorough data ingestion, cleaning, exploratory visualization, and residual diagnostics, this project isolates the marketing channels with the absolute highest financial impact, providing a transparent, data-driven recommendation for corporate budget allocation.

## 🎯 Project Goals
- Perform Exploratory Data Analysis (EDA) to understand feature distributions and relationships.
- Detect and handle multicollinearity using Variance Inflation Factor (VIF).
- Build and refine a Multiple Linear Regression model using `statsmodels`.
- Validate regression assumptions (Linearity, Normality, Homoscedasticity).
- Interpret model coefficients to deliver strategic business insights.
- Translate statistical metrics ($R^2$, coefficients, p-values) into non-technical corporate business intelligence.

## 📊 Dataset
The dataset (`marketing_sales_data.csv`) contains 572 observations of historical marketing campaigns.
- **TV**: Investment tier (Low, Medium, High)
- **Radio**: Budget allocated (in millions of dollars)
- **Social Media**: Budget allocated (in millions of dollars)
- **Influencer**: Influencer tier (Nano, Micro, Macro, Mega)
- **Sales**: Total revenue generated (in millions of dollars)

## 🛠️ Tools & Libraries
- **Python**: Primary programming language.
- **Juypter Lab**: Primary development environment
- **Pandas**: Data manipulation and cleaning.
- **Matplotlib & Seaborn**: Data visualization and diagnostic plots.
- **Statsmodels**: Statistical modeling and regression analysis.

## 🗂️ Repository Structure
```text
├── README.md                                  # Project Overview and Analytical Findings
├── marketing_and_sales_data_evaluate_lr.csv   # Raw corporate marketing dataset
├── multiple_ regression_analysis.ipynb        # Analysis Notebook
└── multiple_ regression_analysis.pdf          # Analysis Notebook in LaTeX format
```

## 💻 Environment Setup & Installation

To execute this analysis in Jupyter Lab, follow these steps:

### Clone repository
> `gh repo clone Chinaice07/Multi-Channel-Marketing-Analysis`

### Install necessary libraries
> `pip install pandas matplotlib seaborn statsmodels jupyterlab`

### Start Jupyter Lab
> `jupyter lab`

This will open Jupyter Lab in your default browser. Navigate to `multiple_regression_analysis.ipynb` in the file browser and open it to begin the analysis.

## 📈 Key Findings
1. **The Regression equation that best predict number of sales is given by:**
   $\\text{Sales} =  64.9254 + 77.3156*X_{TV} + 2.9558 *X_{Radio}$
2. **TV and Radio are the strongest drivers of sales.**
3. **Social Media and Influencer marketing are statistically insignificant** in this dataset (p-values > 0.05) and were dropped from the final parsimonious model.
4. **Model Performance**: The final model explains **90.4% of the variance** in Sales (Adjusted R-squared = 0.904).
5. **Impact Breakdown**:
   - Upgrading the **TV** ad campaign by one tier (e.g., Low to Medium) is associated with an estimated increase in Sales of **77.32 million dollars**, holding Radio spend constant.
   - Every **$1 million increase** in **Radio** spend is associated with an estimated increase in Sales of **2.96 million dollars**, holding TV tier constant.

## ⚠️ Model Limitations
This model assumes that sales variance is driven strictly by these media channels. It is limited by omitted variable bias, as it does not account for critical external factors such as seasonal shopping trends, macroeconomic conditions, or competitor pricing strategies.

## 💡 Strategic Recommendations
- **Prioritize TV and Radio:** Reallocate experimental budgets from Social Media and Influencers directly into the proven TV and Radio vectors.
- **Granular Data Tracking:** Future data collection should track exact dollar amounts for TV spend rather than broad categorical tiers to allow for more precise ROI calculations.
- **Incorporate External Factors:** Future analysis should incorporate seasonality and economic variables for long-term strategic forecasting.

## ✨ **Credits**
- [saswatsethda on Kaggle: Influencer Marketing Sales Modelling and Analysis](https://www.kaggle.com/code/saswatsethda/influencer-marketing-sales-modeling-and-analysis#Multiple-Linear-Regression:-Model-Building-and-Evaluation)

- [Chinaice07 on Github: Marketing ROI Analysis](https://github.com/Chinaice07/Marketing-ROI-Analysis)
