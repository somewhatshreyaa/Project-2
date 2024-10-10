# Superstore-Sales-POWER-BI-Dashboard
Guided Project -  Learnt Power BI and made this project by refering to @Rishab Mishra.

## Introduction 
- In the business world of today, making decisions based on data is essential to success. Using data, the Superstore Sales Analysis and Forecasting project finds important trends, patterns, and insights in a sales dataset. This project uses modern data analysis and visualization approaches to help stakeholders analyze previous sales performance and forecast future trends.

## Process

### Data Preparation
- In order to ensure data quality, the first step involved cleaning the data. This included removing null values, removing unnecessary columns, dealing with duplicates, and modifying data types.
### Data Modeling
- The next step was to use Power BI's DAX (Data Analysis Expressions) to generate calculated measures and tables that would improve the dataset's analytical capabilities.

  
```dax
# Created time-series table of sales for forecasting.
TimeSeriesTable =
SUMMARIZE(
    SuperStore_Sales_Dataset,
    SuperStore_Sales_Dataset[Order Date],
    "Total Sales", SUM(SuperStore_Sales_Dataset[Sales])
)

# Calculate a measure to determine the number of days it took for delivery.
DaysToDeliver =
DATEDIFF(
    SuperStore_Sales_Dataset[Order Date],
    SuperStore_Sales_Dataset[Ship Date],
    DAY
)```

### Data Analysis
- After data modeling, a thorough data analysis was executed in Power BI using a variety of visualization tools, such as matrices, to find sales trends, sales by region, sales by category, and other relevant insights.

### Dashboard Creation
- The project moved forward with the creation of a dynamic and interactive Power BI dashboard. The inclusion of bookmark functions in this dashboard design facilitates fluid switching between various graphs and visualizations for a more thorough analysis of the data.

### Sales Forecasting
- A 10-day sales prediction was created using Power BI's advanced forecasting capability to provide insights into the future. This forecasting skill helps decision-makers foresee future trends and make well-informed choices.


