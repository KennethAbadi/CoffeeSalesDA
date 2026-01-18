# Coffee Sales Data Analysis

A comprehensive exploratory data analysis (EDA) and predictive modeling project analyzing coffee sales patterns, revenue trends, and forecasting future sales using machine learning.

## Project Overview

This project analyzes coffee sales data to uncover patterns in customer purchasing behavior, identify top-performing products and time periods, and build predictive models to forecast future sales. The analysis includes visualizations of sales trends by date, week, month, day of week, and coffee type, along with revenue analysis and machine learning predictions.

## Dataset

- **Source**: `raw_data/index_1.csv` From [Kaggle.com](https://www.kaggle.com/datasets/ihelon/coffee-sales/data)
- **Records**: Coffee sales transactions
- **Date Range**: March 1, 2024 - March 23, 2025 (381 days)
- **Key Fields**:
  - `datetime`: Transaction timestamp
  - `coffee_name`: Type of coffee sold
  - `money`: Transaction amount (gross revenue)
  - `cash_type`: Payment method
  - `card`: Card information

## Analysis Performed

### 1. Data Cleaning
- Handled missing values in card column
- Removed duplicate entries
- Converted datetime fields to proper format
- Feature engineering: extracted week, day of week, date, and month

### 2. Sales Volume Analysis
- Daily sales trends
- Weekly sales patterns
- Monthly sales distribution
- Day-of-week performance
- Coffee type breakdown by day of week

### 3. Revenue Analysis
- Total money by date, week, and month
- Average revenue by day of week
- Revenue breakdown by coffee type
- Top 10 best performing days
- Monthly revenue trends by coffee type

### 4. Predictive Modeling
Compared 4 different machine learning models for sales forecasting:
- **Linear Regression**
- **Ridge Regression**
- **Random Forest** 
- **Gradient Boosting**

**Best Performing Model (Random Forest)**:
- R² Score: 0.56
- Mean Absolute Error: 2.95 sales
- RMSE: 3.72 sales
- Last week prediction accuracy: 94.1%

## Key Findings

### Top Selling Coffee Types
- **Best Sellers**: Cappuccino, Latte, Americano, Americano with Milk
- **Consistent Performance**: These drinks show strong sales across all days
- **Slower Sellers**: Espresso and Cortado

### Seasonal Trends
- Drinks like Americano with Milk, Latte, and Cocoa show increased sales during winter months
- All drinks (except Cortado and Espresso) experienced a significant sales boost after New Year's
- Clear day-of-week patterns with varying performance by coffee type

### Prediction Insights
- Recent sales trends (3-day and 7-day rolling averages) are the strongest predictors (73% feature importance)
- Non-linear models vastly outperform linear models due to complex weekly/seasonal patterns
- Random Forest successfully captures sales momentum and weekly patterns

## Requirements

```python
pandas
numpy
matplotlib
```

## Getting Started

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd CoffeeSalesDA
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn plotly scipy scikit-learn
   ```

3. **Run the analysis**
   - Open `eda_analysis.ipynb` in Jupyter Notebook or VS Code
   - Run all cells to reproduce the analysis

## Notebook Structure

1. **Import Libraries**: Load required Python packages
2. **Load Dataset**: Import coffee sales data
3. **Data Cleaning**: Handle missing values and duplicates
4. **Sales Analysis**: Visualizations for sales counts by various time periods
5. **Revenue Analysis**: Money/revenue visualizations and breakdowns
6. **Predictive Modeling**: Machine learning models for sales forecasting

## Visualizations Included

- Line graphs: Daily, weekly, and monthly sales trends
- Bar charts: Day-of-week performance, top 10 days, coffee type breakdowns
- Grouped bar charts: Sales and revenue by coffee type and day
- Stacked bar charts: Top days with coffee type breakdown
- Subplots: Monthly revenue by coffee type
- Model comparison: Actual vs predicted sales for 4 different algorithms

## Model Comparison Results

| Model | R² Score | MAE | RMSE |
|-------|----------|-----|------|
| Random Forest | 0.5592 | 2.95 | 3.72 |
| Gradient Boosting | 0.3876 | 3.56 | 4.38 |
| Ridge Regression | -13.97 | 18.58 | 21.68 |
| Linear Regression | -14.56 | 18.89 | 22.10 |

## Future Improvements

- Incorporate external factors (holidays, weather, promotions)
- Analyze hourly sales patterns if timestamp data available
- Customer segmentation analysis
- Inventory optimization recommendations
- A/B testing for promotional strategies

## Author

Kenneth Abadi

---

*Last Updated: January 2026*
