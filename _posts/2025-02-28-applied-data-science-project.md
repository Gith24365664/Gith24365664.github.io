---
layout: post
author: CHEN LONG
title: "Applied Data Science Project Documentation"
categories: ITD214
---
## Project Background
This project aims to develop a data-driven pricing strategy by analyzing the relationship between price and demand. The primary business objective is to optimize pricing to maximize revenue while maintaining competitive market positioning. The key problem statement is determining price elasticity and formulating an effective pricing adjustment strategy based on sales data and predictive modeling.

## Work Accomplished

### Data Preparation

- Collected and cleaned raw sales data, ensuring consistency and handling missing values.

- Performed feature engineering, including:
  - Creating derived variables related to price changes.
  - Encoding categorical features where necessary.
  - Removing outliers that could distort price elasticity calculations.
  
- Normalized or standardized numerical features to improve model performance.

- Split data into training (80%) and testing (20%) sets for model evaluation.

### Modelling
- Implemented multiple models to predict demand based on price changes:
  - Linear Regression: Provided a basic benchmark but had limitations in capturing complex relationships.
  - Random Forest: Performed well due to its ability to handle nonlinear patterns.
  - Gradient Boosting: Also showed strong results but required hyperparameter tuning for optimal performance.
  
- Identified Random Forest as the best-performing model and fine-tuned it using GridSearchCV, optimizing key hyperparameters.

### Evaluation
- Model Comparison:
  - Linear Regression: Lower accuracy due to price-demand complexity.
  - Random Forest: Best balance of accuracy and generalization.
  - Gradient Boosting: Competitive but more computationally expensive.
  
- Performance Metrics:
  - Initial Random Forest R² score: 0.4276
  - After tuning, R² improved to 0.6018, significantly enhancing prediction accuracy.

- Price Elasticity Estimation:
  - Since sales volume changes were not available, a 10% price adjustment was applied to approximate demand elasticity.
  - Products were categorized based on elasticity to define the pricing strategy.

## Recommendation and Analysis
- If a product has high price elasticity, a 10% price reduction is recommended to increase sales volume.
- If a product has low price elasticity, a 10% price increase is recommended to maximize revenue.
- If demand remains stable regardless of price changes, maintaining the current price is the best approach.
- Due to potential biases from limited customer reviews, pricing strategies should be periodically reviewed with additional data sources.


## AI Ethics
- Privacy: The dataset does not contain personal customer information, ensuring compliance with privacy regulations.
- Fairness: The pricing model is evaluated to prevent discrimination against specific customer groups or product categories.
- Accuracy: The model’s predictions are continuously refined through data-driven insights and validation processes.
- Accountability: Pricing decisions should be reviewed regularly, ensuring they align with business goals and market trends.
- Transparency: The methodology, data sources, and model performance metrics are documented for stakeholder understanding and trust.

## Source Codes and Datasets
https://github.com/Gith24365664/itd214_project

