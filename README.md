# bank_campaign
Predicting Term Deposit Subscriptions in Direct Marketing Campaigns for a Portuguese Bank

## Overview
This project focuses on predicting whether clients will subscribe to a term deposit in direct marketing campaigns conducted by a Portuguese bank. The dataset used is sourced directly from UCI Machine Learning Repository.


### Data Loading
The data is loaded directly from the source using the `fetch_ucirepo` function from `ucimlrepo`.

```python
from ucimlrepo import fetch_ucirepo
fetch_ucirepo(id=222)
```

### Data Cleaning
dataset is reformated to the expected data structure

### Feature Analysis and Comparison
Comprehensive analysis and comparison of features for target prediction include:
- Feature Importance with Random Forest derived fro Pycaret Models
- Information Value Calculation
- Mutual Information Score
- Point-Biserial Correlation Coefficients

These metrics are combined and visualized to assess their contributions to predicting the target variable.

### Feature Transformation
Dataset undergoes transformation including binning and encoding considering data types, distribution, outliers, skewness, and variance.

### Model Evaluation
Models (XGB, Stacked, RF, RG, LR, KNN) are evaluated using metrics such as Accuracy, F1_score, and AUC_score, with XGB identified as the top performer.

### Model Interpretation
Interpretation of the best model (XGB) includes:
- ROC-AUC curve for probability estimation
- Lift and Gain Analysis
- LIME Methodology
- SHAP Methodology

## Insights
The analysis highlighted the significant predictors of term deposit subscriptions. Features such as duration, poutcome, month, pdays, and customer demographics (housing, job) played crucial roles in predicting subscription outcomes.

Among various models evaluated, XGBoost consistently outperformed others in terms of accuracy, F1 score, and AUC score. Its robustness in handling complex relationships within the data proved effective for predicting subscription likelihood.

Model interpretation using ROC-AUC curves, Lift and Gain Analysis, LIME, and SHAP methodologies provided deeper insights into how predictions were made. This understanding is essential for stakeholders to comprehend the driving factors behind subscription decisions.

In general, the insights gained can guide the bank's marketing strategies. By focusing efforts on clients identified as more likely to subscribe, resources can be allocated more efficiently, potentially increasing campaign effectiveness and overall ROI.

