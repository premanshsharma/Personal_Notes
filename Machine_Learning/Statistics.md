```mermaid
graph TD
  DS["Descriptive Statistics"]

  DS --> CT["Measure of Central Tendency"]
  DS --> D["Measures of Dispersion (Spread)"]
  DS --> P["Measures of Position"]
  DS --> S["Measure of Shapes"]
  DS --> SV["Summary and Visualisation Tools"]

  CT --> Mean
  CT --> Median
  CT --> Mode

  Mean --> Arithmetic
  Mean --> Weighted
  Mean --> Geometric
  Mean --> Harmonic

  Median --> "Even - Odd data"
  Median --> "Robustness to outliers"

  Mode --> "Uni-model"
  Mode --> "Bi-model"
  Mode --> "Multi-model"

  D --> Range
  D --> Variance
  D --> "Standard Deviation"
  D --> "Interquartile Range (IQR)"
  D --> "Coefficient of variation"

  P --> Percentiles
  P --> Quartiles
  P --> Deciles

  S --> "Skewness (Symmetry of distribution)"
  S --> "Kurtosis (Peakedness/tailedness)"

  SV --> "Five-number summary (min
graph TD
  DS["Descriptive Statistics"]

  DS --> CT["Measure of Central Tendency"]
  DS --> D["Measures of Dispersion (Spread)"]
  DS --> P["Measures of Position"]
  DS --> S["Measure of Shapes"]
  DS --> SV["Summary and Visualisation Tools"]

  CT --> Mean
  CT --> Median
  CT --> Mode

  Mean --> Arithmetic
  Mean --> Weighted
  Mean --> Geometric
  Mean --> Harmonic

  Median --> "Even - Odd data"
  Median --> "Robustness to outliers"

  Mode --> "Uni-model"
  Mode --> "Bi-model"
  Mode --> "Multi-model"

  D --> Range
  D --> Variance
  D --> "Standard Deviation"
  D --> "Interquartile Range (IQR)"
  D --> "Coefficient of variation"

  P --> Percentiles
  P --> Quartiles
  P --> Deciles

  S --> "Skewness (Symmetry of distribution)"
  S --> "Kurtosis (Peakedness/tailedness)"

  SV --> "Five-number summary (min

```

# Mind Map
- Descriptive statistics
  - Measure of Central Tendency
    - Mean
      - Arithmetic
      - Weighted
      - Geometric
      - Harmonic
    - Median
      - Even - Odd data
      - Robustness to outliers
    - Mode
      - Uni-model
      - Bi-model
      - Multi-Model
  - Measures of Dispersion (Spread)
    - Range
    - Variance
    - Standard Deviation
    - Interquaartile Raannge (IQR)
    - Coefficient of variation
  - Measures of Position
    - Percentiles
    - Quartiles
    - Deciles
  - Measure of Shapes
    - Skewness (Symmetry of distribution)
    - Kurtosis (Peakedness/tailedness)
  - Summary and Visualisation Tools
    - Five-number summary (min, Q1, median, Q3, max)
    - Boxplot
    - Histogram
   
      
- Inferential Statistics
  - Point estimation and confidence intervals
  - Hypothesis testing
    - Null vs Alternative Hypotheses
    - Type 1 and Type 2 errors
    - p-values
    - Significance levels
    - Power of a test
    - Common tests:
      - t-test (Independent, Paired, One-sample)
      - ANOVA (One-way, Two-way)
      - Chi-square test (Goodness-of-fit, Independence)
      - F-test (Variance comparison)
- Central Limit Theorem
# Descriptive statistics
## Mind Map
- Mean
- Median
- Mode
- Variance
- Standard Deviation
- Percentiles
- Quartiles
# Inferential Statistics
- Inferential statistics involves using data from a sample to make generalizations or inferences about a population.
- Unlike descriptive statistics, which only summarize the data, inferential statistics allow us to make predictions, test hypotheses, and estimate population parameters.
- Key concepts in inferential statistics include point estimation, confidence intervals, hypothesis testing, and various statistical tests.
## Mind Map
- Point estimation and confidence intervals
- Hypothesis testing
  - Null vs Alternative Hypotheses
  - Type 1 and Type 2 errors
  - p-values
  - Significance levels
  - Power of a test
  - Common tests:
    - t-test (Independent, Paired, One-sample)
    - ANOVA (One-way, Two-way)
    - Chi-square test (Goodness-of-fit, Independence)
    - F-test (Variance comparison)
- Central Limit Theorem
## Point estimation and confidence intervals
- Point Estimation: A point estimate is a single value given as an estimate of an unknown population parameter. For example, the sample mean x' is used as a point estimate for the population mean μ.
- Confidence Interval (CI): A confidence interval provides a range of values within which a population parameter is expected to lie, with a certain level of confidence. The interval is calculated from the sample data and typically expressed as:
