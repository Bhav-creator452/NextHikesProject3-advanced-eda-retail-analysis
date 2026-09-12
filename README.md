# Advanced Exploratory Data Analysis of Retail Transaction Data

### Univariate, Bivariate & Multivariate Analysis Using Python

An advanced Exploratory Data Analysis (EDA) project based on a large-scale
retail transaction dataset containing **100,000 records and 18 original
variables**.

The project focuses on understanding customer behavior, product patterns,
pricing, discounts, delivery, payment methods and returns through statistical
analysis and advanced data visualization.

---

## 📌 Project Overview

Exploratory Data Analysis is a critical stage of the data-analysis workflow
used to understand data before applying statistical or predictive techniques.

This project follows a complete EDA workflow covering:

- Initial dataset exploration
- Data-quality validation
- Data preparation and feature engineering
- Univariate analysis
- Bivariate analysis
- Multivariate analysis
- Correlation analysis
- Skewness and kurtosis analysis
- Outlier detection and investigation
- Business insights and recommendations

The complete analysis is implemented in a **Jupyter Notebook using Python**.

---

## 🎯 Project Objectives

The primary objectives of this project are to:

- Understand the structure and characteristics of the retail dataset
- Identify distributions and patterns within numerical and categorical
  variables
- Analyze relationships between variables
- Perform univariate, bivariate and multivariate analysis
- Measure correlations between numerical variables
- Detect and interpret statistical outliers
- Evaluate skewness and kurtosis
- Extract meaningful business insights
- Develop data-driven analytical recommendations

---

## 📊 Dataset Overview

| Property                   | Details                      |
| -------------------------- | ---------------------------- |
| Dataset                    | Retail Transaction Data      |
| Original Records           | 100,000                      |
| Original Variables         | 18                           |
| Final Analytical Variables | 26                           |
| Data Types                 | Numerical, Categorical, Date |
| Time Period                | January 2023 – December 2025 |

### Original Variables

The dataset contains information related to:

- Customer identification and demographics
- Gender
- City and state
- Customer segment
- Order identification and date
- Product category and subcategory
- Product price
- Quantity
- Discount percentage
- Final transaction price
- Payment method
- Shipping type
- Delivery days
- Return status

---

## 🛠️ Technologies Used

| Technology       | Purpose                                |
| ---------------- | -------------------------------------- |
| Python           | Core programming language              |
| Pandas           | Data manipulation and analysis         |
| NumPy            | Numerical computation                  |
| Matplotlib       | Data visualization                     |
| Seaborn          | Statistical and advanced visualization |
| Jupyter Notebook | Interactive analysis environment       |

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Initial Exploration
     ↓
Data Quality Validation
     ↓
Data Preparation & Feature Engineering
     ↓
Univariate Analysis
     ↓
Bivariate Analysis
     ↓
Multivariate Analysis
     ↓
Correlation Analysis
     ↓
Outlier Detection & Investigation
     ↓
Business Insights
     ↓
Recommendations
```

## 🔎 1. Initial Data Exploration

The dataset was initially explored using Python and Pandas through:

head() and tail()
shape
columns
info()
dtypes
describe()
Unique-value analysis
Categorical frequency analysis
Initial Dataset
100,000 rows × 18 columns

---

## ✅ 2. Data Quality Assessment

Before performing visualization and statistical analysis, the dataset was
validated for missing values, duplicates, invalid values and logical
inconsistencies.

Validation Results
Data Quality Check Result
Missing Values 0
Duplicate Rows 0
Invalid Numerical Values 0
Invalid Date Values 0
Categorical Whitespace Issues 0
Missing Calendar Dates 0
Pricing Formula Consistency 100%

The dataset passed the validation stage without requiring row deletion or
value correction.

---

## ⚙️ 3. Data Preparation & Feature Engineering

The original dataset contained 18 variables. Additional analytical
features were created to support time-based and multivariate analysis.

Date Features Created
order_year
order_month
order_month_name
order_quarter
order_day_of_week
order_day_name
order_year_month
Additional Analytical Feature
age_group
Final Analytical Dataset
100,000 rows × 26 columns

---

## 📈 4. Univariate Analysis

Univariate analysis was performed to understand individual variables and their
distributions.

Numerical Analysis

The following statistical measures were evaluated:

Mean
Median
Standard deviation
Minimum and maximum
Skewness
Kurtosis
Distribution shape
Potential outliers
Key Finding — Final Price Distribution

final_price was the most positively skewed numerical variable.

Final Price Skewness = 0.93

The distribution contains a long upper tail caused by a smaller number of
high-value transactions.

Major Visualizations
Histograms
KDE plots
Boxplots
Log-transformed distribution
Skewness comparison

---

## 👥 5. Categorical & Temporal Analysis

Frequency distributions were analyzed for:

Gender
City
State
Customer segment
Product category
Product subcategory
Payment method
Shipping type
Return status

Temporal analysis was also performed using monthly transaction trends and
year-month heatmaps.

Key Observations

Customer segments are broadly balanced:

New → 33.5%
Regular → 33.4%
Premium → 33.2%

Product-category transaction volumes are also broadly balanced.

Transaction activity remains relatively stable across the 2023–2025 period,
with some recurring monthly variation.

---

## 🔗 6. Bivariate Analysis

Bivariate analysis was used to study relationships between two variables.

Product Price vs Final Price

Pearson correlation:

r = 0.7308

This is the strongest positive linear relationship identified among the
numerical variables.

Higher product prices are strongly associated with higher final transaction
values.

Quantity vs Final Price

Average final transaction value increases consistently with order quantity.

Quantity Average Final Price
1 ₹25,595.96
2 ₹51,382.11
3 ₹76,837.73
4 ₹102,663.72

Pearson correlation:

r = 0.58
Age vs Final Price

Pearson correlation:

r = -0.0008

The relationship is effectively zero.

Customer age does not appear to be a meaningful linear indicator of final
transaction value.

Customer Segment vs Final Price
Customer Segment Average Final Price
Premium ₹64,430.45
Regular ₹64,303.15
New ₹63,766.75

Premium customers have the highest average final price, but the differences
between segments are relatively small and their distributions overlap
substantially.

Product Category vs Return Rate
Product Category Return Rate
Fashion 15.05%
Home & Kitchen 14.89%
Grocery 14.87%
Health 14.83%
Beauty 14.76%
Electronics 14.47%

Return rates remain tightly clustered across product categories.

Shipping Type vs Delivery Days
Shipping Type Average Delivery
Express 5.50 days
Standard 5.51 days

The two shipping types show almost identical average delivery times.

Delivery Days vs Return Rate

Spearman correlation:

ρ = -0.0061

Return rates fluctuate across delivery durations but do not show a consistent
increasing or decreasing pattern.

---

## 🧩 7. Multivariate Analysis

Multivariate analysis was used to study interactions among three or more
variables.

Product Category × Discount × Final Price

Average final transaction price generally decreases as discount percentage
increases.

0% Discount → ₹76,029.98 average final price
30% Discount → ₹52,051.12 average final price

The overall pattern is broadly similar across product categories.

Customer Segment × Age × Final Price

The relationship between age and final transaction price was examined within
New, Regular and Premium customer segments.

All segment-wise age-price correlations were approximately zero.

The highest average Premium transaction value occurred in:

Age Group: 46–55
Average Final Price: ₹65,432.07
Delivery Days × Shipping Type × Return Status

Return rates were compared across delivery durations for Express and Standard
shipping.

The highest observed combination was:

Express + 7 days → 16.21% return rate

However, the return rate does not consistently increase with longer delivery
times.

---

## 📐 8. Correlation Analysis

Pearson correlation was calculated across the primary numerical variables.

Strongest Relationships with Final Price
Variable Pair Pearson Correlation
Product Price ↔ Final Price 0.73
Quantity ↔ Final Price 0.58
Discount ↔ Final Price -0.14
Age ↔ Final Price ≈ 0
Delivery Days ↔ Final Price ≈ 0
Key Interpretation

Final transaction value is most strongly associated with direct transaction
components such as product price and quantity.

Discount percentage shows a weak negative linear relationship with final price,
while age and delivery duration show virtually no linear relationship with
final price.

---

## 🚨 9. Outlier Detection & Investigation

Potential outliers were identified using:

Boxplots
Interquartile Range (IQR)
Z-score
Outlier Results
Variable IQR Outliers Z-Score Outliers
Age 0% 0%
Product Price 0% 0%
Quantity 0% 0%
Discount Percentage 0% 0%
Final Price 1.34% 0.50%
Delivery Days 0% 0%
Outlier Investigation

The statistical outliers were concentrated in final_price.

The extreme transactions were investigated using their associated:

Product price
Quantity
Discount percentage
Product category
Payment method
Shipping type
Delivery duration

The high-value transactions were found to be internally consistent with the
dataset's pricing relationship.

Therefore, the observations were considered legitimate high-value
transactions rather than invalid data.

Treatment Decision

No observations were removed, capped or replaced solely because they were
statistical outliers.

---

## 💡 10. Key Business Insights

1. Product Price is the Strongest Transaction-Value Driver

product_price has the strongest numerical association with final_price,
with a Pearson correlation of 0.73.

2. Larger Orders Have Higher Transaction Values

Average final price increases consistently as quantity rises from 1 to 4.

3. Discounts are Associated with Lower Final Transaction Values

Average final price generally decreases as the discount percentage increases.

4. Customer Age is Not a Strong Transaction-Value Indicator

Age has virtually no linear relationship with final transaction value.

5. Return Rates are Relatively Stable

Return rates remain close across product categories, payment methods,
shipping types and delivery durations.

6. Shipping Type Shows Little Overall Difference

Express and Standard shipping have almost identical average delivery times and
very similar return rates.

7. High-Value Outliers are Valid

Statistically unusual high-value transactions are internally consistent and
were therefore retained.

---

## 📌 11. Recommendations

Based on the findings from the EDA:

Focus transaction-value analysis primarily on product price and order
quantity.
Evaluate discount strategies together with transaction value and product
mix.
Avoid using customer age as a primary indicator of transaction value.
Use multi-factor analysis when investigating return behavior instead of
relying on a single variable.
Preserve valid high-value transactions when analyzing transaction-value
distributions.

---

## 📁 12. Project Structure

Advanced EDA in Python/
│
├── retail_large_dataset.csv
├── Advanced_EDA_Retail_Analysis.ipynb
├── Advanced_EDA_Retail_Analysis_PPT.pptx
├── README.md
├── requirements.txt
└── screenshots/
├── data_quality.png
├── final_price_distribution.png
├── product_price_vs_final_price.png
├── discount_category_heatmap.png
├── segment_age_heatmap.png
└── correlation_heatmap.png

Update the filenames above if your actual repository uses different names.

---

## ▶️ 13. How to Run the Project

Clone the repository
git clone <your-github-repository-url>
Navigate to the project directory
cd "Advanced EDA in Python"
Install dependencies
pip install -r requirements.txt
Launch Jupyter Notebook
jupyter notebook

Open the project notebook and run the cells from top to bottom.

---

## 📦 14. Requirements

The project uses the following Python libraries:

pandas
numpy
matplotlib
seaborn
jupyter

---

## 📊 15. Visualizations Included

The notebook contains a range of statistical and advanced visualizations,
including:

Histograms
KDE distributions
Boxplots
Scatter plots
Regression plots
Bar charts
Line charts
Time-series visualizations
Heatmaps
Faceted plots
Correlation heatmaps
Outlier analysis

The visualizations were selected based on the analytical question being
investigated rather than simply increasing the number of charts.

---

## 🔮 16. Future Scope

The completed EDA provides a foundation for further analytical and predictive
work.

Possible extensions include:

Return-probability prediction
Customer segmentation and clustering
Transaction-value prediction
Pricing and discount optimization
Product-level return-risk analysis
Statistical hypothesis testing
Machine-learning models for retail behavior
👩‍💻 Author

Bhavdeep Kaur

BCA Student | Python | Data Analytics | Machine Learning

Project: Advanced Exploratory Data Analysis of Retail Transaction Data
Organization: NextHikes IT Solutions

---

⭐ Conclusion

This project demonstrates a complete Exploratory Data Analysis workflow,
beginning with data validation and preparation and progressing through
univariate, bivariate and multivariate analysis, correlation analysis,
skewness and kurtosis evaluation, outlier investigation and business
interpretation.

The analysis shows that transaction value is primarily associated with direct
transaction components such as product price and quantity, while the
demographic and operational variables examined in this project show
comparatively weak standalone relationships with transaction value or return
behavior.

The project provides a strong foundation for further statistical analysis and
predictive modelling.

```

```
