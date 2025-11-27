# Housing Prices and Air Quality (DSA210 Project Proposal)

## 1. Project Title
Exploring the Relationship Between Housing Market Indicators and Air Quality

## 2. Motivation
Housing prices and air quality are two important indicators of quality of life.  
In this project, I aim to explore whether countries with cleaner air also tend to have stronger housing markets.  
By combining housing market data with global air quality measurements, I hope to identify simple patterns or differences between cleaner-air and more-polluted countries.

## 3. Datasets
- **Dataset 1:** *Global Housing Market Analysis 2015–2024*  
  https://www.kaggle.com/datasets/atharvasoundankar/global-housing-market-analysis-2015-2024  
  (Contains house price index, rent index, mortgage rates, inflation, GDP growth, etc.)

- **Dataset 2:** *World Air Quality Data 2024*  
  https://www.kaggle.com/datasets/kanchana1990/world-air-quality-data-2024-updated  
  (Contains air quality measurements for countries and cities in 2024.)

## 4. Data Collection
Both datasets will be downloaded as CSV files from Kaggle.  
For the analysis, I will:
- Select only the **2024** entries from the housing dataset.
- Clean the air quality dataset (dropping missing or irrelevant rows).
- Rename and align columns where necessary.
- Merge the two datasets using the **Country** column.

## 5. Planned Analysis
I plan to perform the following steps:
- Basic data cleaning and preparation.
- Exploratory Data Analysis (EDA) with summary statistics.
- Visualizations such as scatter plots and bar charts.
- Divide countries into groups (clean-air vs polluted) based on median AQI.
- Perform a **simple hypothesis test (independent samples t-test)** to check if the average housing price index differs between the two groups.

## 6. Expected Outcome
I expect to observe whether air quality has any meaningful relationship with housing market indicators.  
The results may show:
- If cleaner-air countries have higher housing price index values,
- Or if there is no significant difference between clean and polluted countries.

Overall, the project aims to provide a simple and clear comparison using real-world data.