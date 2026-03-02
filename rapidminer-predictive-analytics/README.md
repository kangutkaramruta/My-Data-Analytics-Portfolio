# RapidMiner Predictive Analytics Project
This project demonstrates predictive modelling using RapidMiner.

# Predictive Analytics (RapidMiner) – Airbnb Sydney Reviews

## Objective
Analyse whether host listing descriptions align with customer review sentiment, identify drivers of review score ratings, and segment properties into actionable clusters.

## Data
- ~37k listings and ~549k reviews (Sydney Airbnb).
- Mixed data types (numeric, nominal, text). Text was processed into sentiment features.

## Problems Solved
1) Sentiment alignment: host description vs guest review sentiment
2) Prediction: estimate review score ratings using listing/host features
3) Segmentation: cluster properties into distinct groups for targeted decision-making

## Methods
### 1) Text + Sentiment Engineering
- Document processing and sentiment extraction from review text
- Pearson correlation between host-description sentiment and review sentiment

### 2) Predictive Modelling
- Multiple Linear Regression (numeric target)
- Correlation-weighted feature selection
- Leakage avoidance (excluded derived review sub-scores)
- Multicollinearity handling (excluded correlated structural fields)
- Evaluation: R², residual analysis, and model refinement

### 3) Clustering
- K-means clustering with K selection (Davies–Bouldin + elbow method)
- PCA to reduce multicollinearity and assess variance structure

## Key Findings (Technical)
- Host vs review sentiment showed weak alignment (expectation gap exists).
- Multiple regression model achieved low explanatory power (R² ≈ 0.047); used mainly for interpretability.
- 3 clusters identified:
  1) smaller, cheaper listings with fewer host listings
  2) larger, costlier listings with higher security deposits
  3) pricier listings with lower sentiment reviews and higher host listing counts

## Recommendations
- Improve listing accuracy and address negative-experience themes.
- Prioritise quality uplift in shared/hostel-style inventory.
- Use cluster segments to tailor host support and marketing strategies.

## Repo Contents
- `/process/` RapidMiner process files (.rmp)

  
