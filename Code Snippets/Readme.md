This folder contains commun code that can be used across multiple projects .The code snipets just show you how to use it with a simple example

## Sections
When you want to create a model there are several steps that normally you need to do, and based on your data, model and objective you might need to get deeper into one step or even skip others. In here each folder have code useful for that specific step.

#### EDA
Common code that you use to give yourself a sense of the data.

#### Data cleaning
Usual code for cleaning for dataset. 
- Statistics/Remove Outliers
1. Remove Outliers using Normal Distribution and S.D: remove the outlier points is by eliminating any points that aere above (Mean + 2SD) and any points below (Mean - 2SD) before plotting them. This based on the assumption that your data follows a normal (Gaussian) distribution. In a normal distribution:
About 95% of the data lies within ±2 standard deviations (SD) from the mean and about 99.7% of the data lies within ±3 standard deviations (SD) from the mean.ou can check this by plotting a histogram or using statistical tests (e.g., Shapiro-Wilk test).
2. Z-Score: based on the properties of the normal distribution  ∣Z∣>3, is prefered that the point before. In a normal distribution:
About 68% of data lies within ± 1 SD.
About 95% of data lies within ±2 SD.
About 99.7% of data lies within ±3 SD.
3. Interquartile Range (IQR): data is not normally distributed or when it contains skewness




#### Feature Engineering
 - Feature Scaling: Some machine learning algorithms perform better or converge faster when features are on a similar scale 

