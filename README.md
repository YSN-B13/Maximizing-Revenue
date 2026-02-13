# Maximizing Revenue: Payment Method Analysis

A data analysis project examining the relationship between taxi fare amounts and payment methods using NYC Yellow Taxi trip data from January 2020.

## 📊 Project Overview

This analysis investigates whether there is a statistically significant difference in fare amounts between customers who pay by credit card versus cash, with the goal of identifying opportunities to maximize revenue without negatively impacting customer experience.

## 🎯 Objectives

- Determine the relationship between total fare amount and payment type
- Identify patterns that could inform payment method recommendations
- Provide data-driven insights for revenue optimization strategies

## 🔍 Research Questions

1. **Is there a relationship between total fare amount and payment type?**
2. **Can we nudge customers towards payment methods that yield higher revenue for drivers without negatively impacting customer experience?**

## 📁 Dataset

- **Source**: NYC Yellow Taxi Trip Data (January 2020)
- **Initial Size**: 6,405,008 trips
- **Final Sample Size**: 2,748,932 trips (after cleaning)
- **Key Variables**:
  - Payment type (Card/Cash)
  - Fare amount
  - Trip distance
  - Trip duration
  - Passenger count

## 🛠️ Technologies Used

- **Python 3.x**
- **Libraries**:
  - pandas - Data manipulation
  - numpy - Numerical operations
  - matplotlib - Data visualization
  - scipy - Statistical testing
  - statsmodels - Advanced statistical analysis

## 📈 Methodology

### Data Preprocessing
1. Loaded raw taxi trip data
2. Filtered for relevant payment types (Card and Cash only)
3. Removed null values and duplicates
4. Applied passenger count filters (1-5 passengers)
5. Removed outliers using IQR method
6. Filtered for positive fare amounts, distances, and durations

### Exploratory Data Analysis
- Distribution analysis of fare amounts and trip distances by payment type
- Descriptive statistics comparison
- Payment preference visualization
- Passenger count analysis by payment method

### Statistical Testing
- **Hypothesis Test**: Two-sample t-test (Welch's t-test)
- **Null Hypothesis**: No difference in average fare between card and cash payments
- **Alternative Hypothesis**: Significant difference exists between payment methods
- **Significance Level**: α = 0.05

## 🔑 Key Findings

### Payment Distribution
- **67.3%** of trips paid by credit card
- **32.7%** of trips paid by cash

### Fare Comparison
| Payment Type | Mean Fare | Std Dev | Mean Distance | Std Dev |
|--------------|-----------|---------|---------------|---------|
| Card         | $13.11    | $5.85   | 2.99 miles    | 1.99    |
| Cash         | $11.76    | $5.61   | 2.60 miles    | 1.91    |

### Statistical Results
- **T-statistic**: 169.21
- **P-value**: < 0.001
- **Conclusion**: We reject the null hypothesis. There is a statistically significant difference in average fare between card and cash payments.

### Insights
1. **Credit card payments yield higher average fares** ($1.35 more per trip)
2. **Card users travel longer distances** on average (0.39 miles more)
3. **Card payments are already preferred** by the majority of customers
4. The difference is statistically significant and practically meaningful

## 💡 Recommendations

1. **Encourage Card Payments**: Implement incentives for credit card usage without penalizing cash users
2. **Optimize Payment Experience**: Ensure card readers are always functional and payment process is seamless
3. **Customer Education**: Inform customers about the convenience and benefits of card payments
4. **Monitor Impact**: Track changes in payment method adoption and average fare amounts

## 📊 Visualizations

The analysis includes:
- Distribution histograms for fare amount and trip distance by payment type
- Box plots for outlier detection
- Pie chart showing payment preference
- Stacked bar chart showing passenger count distribution by payment method
- Q-Q plot for normality assessment

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib scipy statsmodels
```

### Running the Analysis
```python
# Load the dataset
df = pd.read_csv('yellow_tripdata_2020-01.csv')

# Run the complete analysis pipeline
# (See notebook for full code)
```

## ⚠️ Limitations

- Analysis limited to January 2020 data only
- Does not account for seasonal variations
- Tips are included in card payments but not typically in cash payments
- External factors (weather, events) not considered

## 🔮 Future Work

- Expand analysis to multiple months/years
- Include tip amounts as a separate variable
- Analyze peak vs off-peak hour patterns
- Investigate geographic patterns (pickup/dropoff locations)
- Build predictive models for payment method selection

## 👥 Contributors

This analysis was conducted as part of a revenue optimization initiative.

## 📄 License

This project is available for educational and analytical purposes.

## 📧 Contact

For questions or collaboration opportunities, please reach out through the project repository.
