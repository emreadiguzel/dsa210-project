# Housing Markets and Air Quality: A Cross-Country Analysis  
**DSA210 – Introduction to Data Science | Term Project**

## Motivation
Air quality is an important factor affecting quality of life. Intuitively, people may prefer to live in places with cleaner air, and this preference could be reflected in housing markets.

In this project, I investigate whether **countries with different air quality levels also show differences in housing market indicators**, such as rent, house prices, and affordability.

To meet the DSA210 requirement of using multiple datasets, I combine **global housing market data** with **world air quality data** at the country level.

---

## Research Questions
1. Is there a **statistically significant difference** in housing indicators between clean-air and polluted countries?
2. Can housing-related variables be used to **predict air quality categories**?
3. Which housing and macroeconomic features are **most informative** for air quality differences?

---

## Datasets
### 1) Global Housing Market Analysis (2015–2024) (https://www.kaggle.com/datasets/atharvasoundankar/global-housing-market-analysis-2015-2024) 
- House Price Index
- Rent Index
- Affordability Ratio
- Mortgage Rate
- Population Growth
- Construction Index
- GDP Growth, Inflation, Urbanization Rate

### 2) World Air Quality Data (2024)  (https://www.kaggle.com/datasets/kanchana1990/world-air-quality-data-2024-updated)  
- Country-level air quality measurements
- Converted into **4 air quality categories**:
  - 1 = Bad  
  - 2 = Bad–Mid  
  - 3 = Mid–Good  
  - 4 = Good  

---

## Methodology
1. Merged datasets by **country name**
2. Performed **exploratory data analysis (EDA)** to inspect distributions and relationships
3. Applied **Welch’s t-test** to test differences between clean-air and polluted countries
4. Trained multiple **machine learning models**:
   - Logistic Regression
   - Decision Tree
   - Random Forest
   - XGBoost
5. Analyzed **feature importance**
6. Removed low-importance features and retrained models as a robustness check

---

## Key Statistical Result
A Welch t-test comparing clean-air and polluted countries produced:

- **t-statistic ≈ −23.16**
- **p-value ≈ 9.28 × 10⁻¹¹⁸**

Since p ≪ 0.05, I **reject the null hypothesis** and conclude that there is a **statistically significant difference** between clean-air and polluted countries in housing-related measures.

---

## Machine Learning Results
Classification accuracy (predicting air quality category):

| Model | Accuracy |
|------|----------|
| Logistic Regression | 0.527 |
| Decision Tree | 0.533 |
| Random Forest | 0.533 |
| XGBoost | 0.533 |

Tree-based models performed slightly better, though overall accuracy suggests this is a **challenging multi-class problem**.

---

## Feature Importance (Key Findings)
Across Random Forest and XGBoost models:

Top features:
1. **Population Growth (%)**
2. **Rent Index**
3. **Affordability Ratio**

Low-impact features (removed in reduced model):
- Mortgage Rate
- Urbanization Rate
- Inflation Rate
- GDP Growth

After removing low-importance features, model performance remained similar, indicating that most predictive power comes from a **small subset of housing indicators**.

---

## Conclusion
This project shows that **housing markets and air quality are strongly related at the country level**. Population growth and rental affordability emerge as the most important factors distinguishing clean-air and polluted countries.

While the analysis is correlational rather than causal, the results suggest that environmental conditions are reflected in housing market dynamics.

---

## Limitations
- Country-level aggregation hides within-country variation
- Air quality data is from a single year
- Machine learning accuracy is moderate due to limited sample size and multi-class setup

---

## Future Work
- Use city-level housing and air quality data
- Treat air quality as a continuous variable
- Incorporate additional environmental indicators