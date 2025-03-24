# Comparing-Classifiers
**Link to Jupyter Notebook** - http://localhost:8888/lab/tree/prompt_III.ipynb

****#Bank Marketing Campaign - Term Deposit Prediction**

This project uses data from a Portugese bank's direct marketing campaigns to predict whether a client will subscribe to a term deposit. The data comes from the UCI Machine Learning Repository - https://archive.ics.uci.edu/ml/datasets/bank+marketing

**#Business Objective**
The goal is to develop a predictive model to help the bank identify which clients are most likely to subscribe to a term deposit. This enables more efficient targeting , reduces marketing costs, and increases the effectiveness of campaigns.

## Dataset Summary

- **Source**: UCI Bank Marketing Dataset
- **Samples**: ~41,000 client contacts
- **Target Variable**: 'y' (binary) — has the client subscribed to a term deposit ('yes' or 'no')
- **Feature Groups**:
  - Bank client info: 'age', 'job', 'marital', 'education', 'default', 'housing', 'loan'
  - Campaign data: 'contact', 'month', 'day_of_week', 'duration', 'campaign', 'pdays', 'previous', 'poutcome'
  - Socioeconomic context: 'emp.var.rate', 'cons.price.idx', 'cons.conf.idx', 'euribor3m', 'nr.employed'

## Modeling Process

### 1. Data Preprocessing
- Replaced 'unknown' values with NaN.
- Converted categorical features to one-hot encoded variables.
- Binary target converted from 'yes/no' to '1/0'.
- Trained/test split: 80/20.

### 2. Baseline
- Majority class accuracy baseline: **~88%**
- Models must outperform this to be useful.

### 3. Models Compared
| Model                 | Train Accuracy | Test Accuracy | Fit Time (s) |
|----------------------|----------------|---------------|--------------|
| Logistic Regression  | 0.89           | 0.88          | 0.01         |
| K-Nearest Neighbors  | 0.84           | 0.85          | 0.01         |
| Decision Tree        | 1.00           | 0.89          | 0.01         |
| Support Vector Machine | 0.89         | 0.87          | 0.05         |

## Observations

- All models performed similarly in terms of test accuracy.
- **Decision Tree** achieved the highest test accuracy but showed signs of overfitting (Train Acc = 1.0).
- **Logistic Regression** was fast and fairly balanced in performance.
- **KNN** had lower training accuracy and can be sensitive to scaling and neighbor count.
- **SVM** performed well but had a longer training time.

## Next Steps

- Tune hyperparameters using 'GridSearchCV'
- Explore additional features (e.g., duration, past outcomes)
- Consider alternative metrics like **precision**, **recall**, **F1-score**

## Author

Reshma Holla Vaddarse Subbarama 
Date: March 24 2025
