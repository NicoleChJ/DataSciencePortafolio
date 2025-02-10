# Common Code Repository
This folder contains reusable code that can be utilized across multiple projects. The provided code snippets demonstrate how to implement these utilities through simple examples.

## Sections
When building a model, several steps are typically required. Depending on your data, model type, and objective, some steps may require more in-depth processing, while others might be optional. Each folder in this repository contains code specifically designed for a particular stage of the process.

#### EDA
Common code that you use to give yourself a sense of the data.

#### Data Cleaning
Includes standard preprocessing techniques for cleaning datasets and preparing them for modeling.

- Statistics/Remove Outliers:
1. Remove Outliers using Normal Distribution and S.D: remove the outlier points is by eliminating any points that aere above (Mean + 2SD) and any points below (Mean - 2SD) before plotting them. This based on the assumption that your data follows a normal (Gaussian) distribution. In a normal distribution:
About 95% of the data lies within ±2 standard deviations (SD) from the mean and about 99.7% of the data lies within ±3 standard deviations (SD) from the mean.ou can check this by plotting a histogram or using statistical tests (e.g., Shapiro-Wilk test).
2. Z-Score: based on the properties of the normal distribution  ∣Z∣>3, is prefered that the point before. In a normal distribution:
About 68% of data lies within ± 1 SD.
About 95% of data lies within ±2 SD.
About 99.7% of data lies within ±3 SD.
3. Interquartile Range (IQR): data is not normally distributed or when it contains skewness

#### Feature Engineering
 - Feature Scaling: Some machine learning algorithms perform better or converge faster when features are on a similar scale 

