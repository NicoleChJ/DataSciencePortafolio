# Common Code Repository
This folder contains reusable code that can be utilized across multiple projects, most of them for classical models. The provided code snippets demonstrate how to implement these utilities through simple examples.For a more detail explanation, please refer to the specific file.

## Sections
When building a clasical model, several steps are typically required. Depending on your data, model type, and objective, some steps may require more in-depth processing, while others might be optional. Each folder in this repository contains code specifically designed for a particular stage of the process.

#### EDA
Common code that you use to give yourself a sense of the data.In this section you will find:
- Data Inspection.
- Visualizations for univariate, bivariate and multivariate analysis.
- Statistical Tests.


#### Data Cleaning
Includes standard preprocessing techniques for cleaning datasets and preparing them for modeling based on the discovers done in EDA:
- Usual clean.
- Outliers


#### Feature Engineering
So normally with the 4 first steps you can start small and see performance.
- Feature Creation
- Feature Selection.
- Feature Extraction.
- Feature Scaling and normalization: Some machine learning algorithms perform better or converge faster when features are on a similar scale 
- Feature Enconding.
- Feature Importance 

1. Workflow Recommendations: Understand domain context, start with simple transformations,validate each feature's impact,avoid data leakage,use cross-validation and consider cosmputational complexity

2. Common Pitfalls: Overfitting through excessive feature engineering,introducing multicollinearity, losing interpretability and computational overhead. 

#### Data Preprocessing: 
Should focus on final data preparation tasks that are not directly related to feature transformation but rather making the dataset ready for modeling:
- Data Splitting
- Handling Imbalance: Imbalanced handling should be applied after splitting (to avoid information leakage) for clasification problems and just on training data.
- Stationarity: Techniques to apply for time series that are non-stationary,

#### Model Selection and Training
- Moldel Types: Choose candidate models based on the problem and train models with default hyperparameters to compare performance.
- Hyperparameter tunning: Optimize the best-performing model and train the model with the best hyperparameters on the full training set.
- Regularization and Early stopping: prevents overfiting 

#### Model Evaluation 
- Performance Metrics
- Model comparision

#### Model Deployment
This phase ensures that a trained and validated model is integrated into a production environment for real-world use.

- Model Serialization and Packaging: Saving it in a format that can be easily integrated into the production environment, include the preprocessing pipeline used on training data to ensure consistency during inference, implement version control for models and artifacts and create model registry for tracking deployment history
- Deployment infraestructure:  Make the model available for predictions in a production environment. This can include Docker, Virtual Environments (venv, conda) and model APIs, selection of deployment patterns (batch processing, microservices, edge deployment),Infrastructure as Code (IaC) implementation for reproducible deployments or Cloud-Specific Deployment.
- Governance and Operations: Documentation (eg trouble shoothing, rollbacks plans), security, scalability, CI/CD pipeline integration for automated deployment.

#### Monitor and Maintainance









