# Consumer Spending and Economic Trends: A Data-Driven Analysis Using Affinity Insights

## Project Overview

This capstone project analyzes consumer spending patterns using high-frequency transaction data from Affinity Solutions to understand economic trends, income-based spending differences, and forecasting capabilities during the post-pandemic recovery period (2020-2024).

**Authors:** Naga Dheeraj S and Sai Dheeraj S.N.S  
**Course:** ADTA 5940: Analytics Capstone Experience  
**Institution:** University of North Texas  
**Data Period:** January 2020 - June 2024

## Research Questions

1. **Forecasting**: Can we predict future consumer spending using time series forecasting models?
2. **Income Analysis**: Are high-income and low-income spending behaviors significantly different?
3. **Trend Analysis**: What are the major trends in customer spending over time?
4. **Category Spending**: How does spending behavior in essential vs. non-essential categories differ across income levels?
5. **Employment Correlation**: Does an increase in consumer spending lead to higher employment rates in different states?

## Key Findings

### Forecasting Results
- **LSTM model** performed best on full dataset (RMSE: 0.004752)
- **ARIMA model** excelled during recovery phase (RMSE: 0.008813)
- Advanced ML models effectively capture complex spending patterns and seasonal variations

### Income-Based Insights
- Low-income groups consistently spent **45.3% more** than high-income groups during recovery
- Challenges conventional assumptions about high-income households driving economic recovery
- Statistical significance confirmed (p < 0.001, Cohen's d = -0.42)

### Economic Phases Identified
1. **COVID Crash** (Jan-Apr 2020): Unprecedented spending decline
2. **Pandemic Response** (Apr-Dec 2020): Gradual stabilization
3. **Early Recovery** (2021): Strong rebound begins
4. **Inflation Period** (2022): Peak spending levels
5. **Stabilization** (2023-2024): Normalized patterns

### Essential vs Non-Essential Spending
- Low-income households maintained higher spending across **both** categories
- Gap larger for non-essential items than essentials
- Suggests deferred discretionary spending resumed when conditions improved

## Dataset Information

**Primary Source:** Opportunity Insights Economic Tracker - Affinity Solutions  
**Records:** 50,694 observations with 29 variables  
**Geographic Coverage:** ZIP code level aggregation across all US states  
**Income Segmentation:** Four quartiles (Q1=lowest, Q4=highest)

### Key Variables
- `spend_all`: Total spending across all categories
- `spend_all_q1/q4`: Income quartile-specific spending
- Essential categories: Groceries, healthcare, food services
- Non-essential categories: Entertainment, sports, durables

## Methodology

### Technical Stack
- **Python** (Jupyter Notebook environment)
- **Libraries:** Pandas, NumPy, Matplotlib, TensorFlow, Scikit-learn
- **Models:** ARIMA, Prophet, LSTM, Transformer
- **Statistical Tests:** Paired t-tests, Wilcoxon tests, Cohen's d

### Data Processing
1. **Cleaning:** Created unified date columns, handled missing values via interpolation
2. **Segmentation:** Divided data into economic phases for improved model training
3. **Recovery Focus:** Analyzed Jan 2021 - Jun 2024 for stable pattern identification

### Statistical Analysis
- Normality testing with Shapiro-Wilk
- Non-parametric alternatives when assumptions violated
- Effect size calculations for practical significance
- Multiple comparison corrections applied

## Model Performance

| Model | Data Type | MAE | MSE | RMSE |
|-------|-----------|-----|-----|------|
| LSTM | Full Data | 0.003622 | 0.000023 | **0.004752** |
| ARIMA | Recovery Phase | 0.007297 | 0.000078 | **0.008813** |
| Prophet | Full Data | 0.014657 | 0.000264 | 0.016253 |
| Transformer | Full Data | 0.024015 | 0.000607 | 0.024639 |


## Key Visualizations

The analysis includes comprehensive visualizations covering:
- Time series decomposition (trend, seasonal, residual components)
- Income quartile spending comparisons
- Economic phase transitions
- Category-level spending heatmaps
- Forecasting model performance plots

## Implications

### For Policymakers
- Target financial support to low-income households for faster economic recovery
- Low-income spending drives immediate economic stimulus effects

### For Businesses
- Segment marketing strategies based on income-specific spending patterns
- Use forecasting models for inventory and workforce planning
- Consider seasonal patterns that persist through economic disruptions

### For Researchers
- Demonstrates value of high-frequency transaction data
- Shows effectiveness of combining traditional and advanced modeling approaches
- Provides methodology for analyzing economic recovery patterns

## Limitations

1. **Data Coverage:** Card transactions only (excludes cash and automated payments)
2. **Aggregation Level:** ZIP code grouping prevents individual analysis
3. **Time Period:** Pandemic-influenced data may not represent typical economic conditions
4. **Regional Scope:** Limited geographic granularity for detailed regional analysis

## Future Research

- **Regional Analysis:** Examine state and metropolitan-level spending variations
- **Demographic Expansion:** Include age, education, and household size variables
- **Policy Integration:** Incorporate unemployment benefits and stimulus timing
- **Long-term Validation:** Extend analysis as more post-pandemic data becomes available

## Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn tensorflow scikit-learn statsmodels
```

### Running the Analysis
1. Clone the repository
2. Download data from [Opportunity Insights](https://opportunityinsights.org)
3. Run notebooks in sequential order
4. Execute statistical tests and generate visualizations

## Citation

If you use this work, please cite:
```
@misc{dheeraj2025consumer,
  title={Consumer Spending and Economic Trends: A Data-Driven Analysis Using Affinity Insights},
  author={Dheeraj, Naga and Dheeraj, Sai},
  year={2025},
  institution={University of North Texas},
  note={ADTA 5940 Capstone Project}
}
```

## Contact

For questions about this research:
- **Authors:** Naga Dheeraj S, Sai Dheeraj S.N.S
- **Institution:** University of North Texas
- **Course:** Advanced Data Analytics Program

---

*This project demonstrates the power of high-frequency consumer data in understanding economic recovery patterns and provides actionable insights for policy and business decision-making.*
