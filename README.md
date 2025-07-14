# Heart Disease Prediction Project

This project was built to demonstrate core machine learning workflows and model evaluation strategies on a healthcare-related classification problem.

## Dataset Overview

The dataset contains information such as age, cholesterol, and max heart rate. The target variable indicates heart disease presence (`1`) or absence (`0`).

## Models Used

- **Decision Tree**: High interpretability, prone to overfitting
- **Random Forest**: Best performance due to ensemble learning
- **Logistic Regression**: Linear baseline model, lowest accuracy

## Key Results

| Model               | Accuracy |
|---------------------|----------|
| Decision Tree       | 91.7%    |
| Random Forest       | 98.5%    |
| Logistic Regression | 79.5%    |

The table above reflects performance **before model tuning**, when overfitting and underfitting were not yet addressed.

After correcting for these issues through parameter tuning (e.g., adjusting `max_depth` and `min_samples_leaf`), the models produced more realistic and generalizable results:

| Model               | Accuracy |
|---------------------|----------|
| Decision Tree       | 80.0%    |
| Random Forest       | 85.4%    |
| Logistic Regression | 79.5%    |

## Why Model Tuning Matters

Initial models can achieve deceptively high accuracy by overfitting the training data, especially with flexible algorithms like decision trees and random forests. However, overfit models perform poorly on real-world data because they memorize patterns instead of learning general rules.

To ensure generalization and robustness, I tuned key hyperparameters (e.g., `max_depth`, `min_samples_leaf`) to strike a balance between bias and variance. This led to more realistic accuracy scores and reduced the risk of false predictions which is critical in medical applications like disease detection.
While the original models appeared to achieve near-perfect accuracy, those results were specific to the training data and did not reflect true generalization. After tuning to address overfitting, the revised accuracy scores better represent how the models would perform on new, unseen data.

## Insights

- Random Forest outperformed other models due to its ability to reduce variance and generalize well.
- Proper `max_depth` tuning (tested 4–15) significantly impacted performance.
- Medical metrics like recall were emphasized to reduce missed diagnoses (false negatives).

## Next Steps

- Incorporate ROC/AUC analysis for better model discrimination
- Deploy the model using Streamlit to enable interactive use
- Explore feature selection or engineering to improve performance

## Technologies Used

- Python (pandas, numpy, scikit-learn, matplotlib)
- Jupyter Notebook
- Git/GitHub
