## BMW Price Prediction Model
This project builds a machine learning model to predict the price of BMW cars using factors year, tax etc. The model is trained using a Decision Tree Regressor and optimized through feature selection and model tuning.
 
 ## Project Overview
The goal of this project is to predict BMW car prices based on key vehicle characteristics. The workflow follows a standard supervised machine learning pipeline:
Load dataset
Data was cleaned
Select target and predictors
Train a Decision Tree model
Validate using Mean Absolute Error (MAE)
Tune model complexity
Save model for reuse

## Target Variable
price → BMW selling price
  Features Used
The final model uses:
mileage → total distance driven
mpg → fuel efficiency
engineSize → engine capacity
year → manufacturing year
Feature tax was tested but removed because it did not improve validation performance.
## Model
Algorithm used:
Decision Tree Regressor (scikit-learn)
Final configuration:
max_leaf_nodes = 500
random_state = 1
This limits tree complexity and reduces overfitting.
## Model Evaluation
Evaluation metric:
Mean Absolute Error (MAE)
Final performance:
MAE ≈ 2461
Average BMW price ≈ 10,000
Interpretation:
Predictions are off by about $2,461 on average.
## Validation Strategy
The dataset was split into:
Training data → model learning
Validation data → performance evaluation
This ensures the model generalizes to unseen data.
## Model Persistence
The trained model is saved using joblib for reuse without retraining.
Save model
Copy code
