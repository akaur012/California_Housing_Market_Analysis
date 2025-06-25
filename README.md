# California Housing Market Analysis – Final Project

**Tools:** Pandas, NumPy, Matplotlib, Seaborn, SciPy, Scikit-learn  
**Skills:** Data Cleaning, Feature Engineering, Visualization, Statistical Analysis

## Overview

This project explores the California housing dataset provided by Scikit-learn. The goal was to uncover meaningful relationships between housing features and median house value through data exploration, visualization, and statistical methods.

---

## Objectives

- Understand key factors that influence median house value in California.
- Engineer meaningful features to enhance analysis.
- Visualize distributions and relationships between variables.
- Apply statistical tests to support findings and detect outliers.

---

## Key Analyses & Methods

### Data Exploration
- Loaded and examined the structure of the dataset.
- Verified there were no missing values.
- Generated descriptive statistics for all numerical features.

### Feature Engineering
- Created `rooms_per_household` and `bedrooms_per_room` to better reflect housing density and quality.
- Standardized `MedInc` using z-score normalization to allow fair comparison.

### Visualizations
- Histograms revealed right-skewed distributions for home value and household occupancy.  
  ![Histogram of MedHouseVal](images/histogram_medhouseval.png)

- Scatter plot of `MedInc` vs `MedHouseVal` showed a clear positive trend: higher-income areas tend to have higher-valued homes.  
  ![Scatter plot of MedInc vs MedHouseVal](images/scatter_medinc_vs_medhouseval.png)

- Box plots highlighted variability and potential outliers in `AveOccup`.  
  ![Box plot of AveOccup](images/boxplot_aveoccup.png)

- Pair plots helped visualize multivariate relationships between income, room count, and household density.  
  ![Pairplot](images/pairplot_core_vars.png)

- Area plots compared trends in `AveRooms` and `AveOccup` across time-indexed rows.  
  ![Area plot](images/areaplot_averooms_aveoccup.png)

- Heatmap displayed strong positive correlation between median income and house value, and a negative correlation between `bedrooms_per_room` and house value.  
  ![Correlation heatmap](images/heatmap_correlations.png)

---

## Statistical Insights

- Pearson correlation test confirmed a statistically significant relationship between median income and house value.
- Two-sample t-test showed that areas above the median income had significantly higher home values than those below.
- Z-score method was used to detect outliers in `AveRooms`, identifying homes with exceptionally high room counts.

---

## Key Trends Observed

- Median income is one of the strongest predictors of median house value.
- A higher `rooms_per_household` ratio is generally associated with more valuable homes.
- A higher `bedrooms_per_room` ratio (more bedrooms per room) tends to negatively affect house value, possibly indicating cramped or less luxurious housing.
- Overcrowding (high `AveOccup`) is weakly associated with lower house values.
- Grouping by income bins showed a clear upward trend in house value with each successive income tier.

---

## Recommendations for Real Estate Analysts

- Focus on high-income areas when prioritizing markets for higher-value properties.
- Track metrics like `rooms_per_household` and `bedrooms_per_room` to better gauge property quality.
- Consider implementing thresholds or filters to flag potential undervalued or overcrowded listings.
- Use data-driven strategies when pricing properties based on location-specific household and income data.

---

## Dataset

- California Housing dataset from Scikit-learn: [`fetch_california_housing()`](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html)

---

## Conclusion

This project demonstrates how feature engineering, data visualization, and statistical analysis can be combined to extract meaningful insights from real-world housing data. These findings can inform pricing strategies, investment decisions, and targeted housing policy development.

---

