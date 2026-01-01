#Housing Prices & Air Quality Analysis

**DSA210 Term Project**

## What's this about?

I was curious: do people pay more to live in areas with cleaner air? This project explores whether there's a connection between housing prices and air quality across different countries.

## The idea

It makes sense that people might prefer living in places with better air quality - and be willing to pay for it. So I wanted to find out if the data actually supports this.

## Datasets I used

1. **Housing data** - Global Housing Market Analysis (2015-2024)  
   [Kaggle link](https://www.kaggle.com/datasets/atharvasoundankar/global-housing-market-analysis-2015-2024)  
   Has stuff like house price index, rent index, mortgage rates, etc.

2. **Air quality data** - World Air Quality Data 2024  
   [Kaggle link](https://www.kaggle.com/datasets/kanchana1990/world-air-quality-data-2024-updated)  
   Air quality measurements for countries around the world.

## What I did

1. **Loaded & merged** the two datasets (matched by country name)
2. **Explored the data** - basic stats, scatter plots, bar charts
3. **Ran a t-test & p-test** to check if the difference is statistically significant
4. **Trained ML models** - Logistic Regression, Decision Tree, Random Forest, XGBoost
5. **Analyzed feature importance** to see what matters most
6. **Removed low-importance features** and compared results

## What I found

**Yes, there IS a significant difference!** (p-value way below 0.05)

The main findings:
- **Population Growth** is the biggest predictor - areas with different growth patterns have different air quality
- **Rent Index** and **Affordability Ratio** also matter
- Tree-based models (Random Forest, XGBoost) worked best
- Some features like GDP Growth and Inflation Rate didn't help much

## Conclusion

Housing markets do seem to reflect air quality to some extent. Population growth turned out to be the key factor linking the two. This could be useful for urban planners or anyone interested in how environmental factors affect real estate.