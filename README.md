# Apartment Rent Prediction Using Artificial Neural Networks (ANN)

## Project Overview

This project uses an Artificial Neural Network (ANN) to predict monthly apartment rent in Indian rupees based on property characteristics, location, furnishing, amenities, and other relevant features.

The project demonstrates a complete machine learning workflow, from data cleaning and preprocessing to neural network training, model evaluation, and performance comparison.

## Problem Statement

Apartment rental prices vary depending on location, property size, furnishing, amenities, and other factors. This project explores how machine learning can use these features to estimate monthly apartment rent.

## Objectives

- Analyze apartment rental data and identify important features.
- Clean the dataset and handle missing values.
- Prepare numerical and categorical features for model training.
- Build and train an Artificial Neural Network.
- Improve prediction performance using log transformation and early stopping.
- Compare models using MAE, RMSE, and R².

## Dataset

- **Records after duplicate removal:** 9,300
- **Input features:** 18
- **Target variable:** `monthly_rent_inr`

The dataset includes property size, BHK, bathrooms, city, locality, furnishing, amenities, building information, and other rental-related features.

*Note: The dataset is not included in this repository at present.*

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- TensorFlow / Keras
- Jupyter Notebook

## Project Workflow

1. Data loading and exploratory data analysis
2. Duplicate removal and data quality checks
3. Missing-value imputation
4. Numerical feature scaling
5. Categorical feature encoding
6. Train-test splitting
7. ANN model development and training
8. Log transformation of the target variable
9. Early stopping to control overfitting
10. Model evaluation and visualization

## Model Performance

The following results were obtained on the test dataset:

| Model | MAE (₹) | RMSE (₹) | R² Score |
|---|---:|---:|---:|
| Baseline ANN | 33,359.46 | 67,154.17 | 0.138 |
| Log-Transformed ANN | 10,827.43 | 27,724.99 | 0.853 |
| Log-Transformed ANN + Early Stopping | 10,227.56 | 30,011.08 | 0.828 |

### Key Findings

- Log-transforming the rent target substantially improved model performance compared with the baseline ANN.
- The log-transformed ANN achieved the highest R² score and lowest RMSE among the three models.
- The early-stopping model achieved the lowest MAE.
- High-rent properties remained more challenging to predict accurately.

## Visualization

The repository includes an actual-versus-predicted rent scatter plot to help assess model performance.

![Actual vs Predicted Apartment Rent](images/actual_vs_predicted.png)

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries.
3. Obtain the dataset from its authorized source.
4. Update the notebook's dataset path if necessary.
5. Open `apartment_rent_prediction.ipynb` in Jupyter Notebook or Google Colab.
6. Run the cells in order.

## Future Improvements

- Compare ANN performance with Random Forest and Gradient Boosting models.
- Perform systematic hyperparameter tuning.
- Investigate prediction errors for high-rent properties.
- Develop an interactive rent prediction application.

## Disclaimer

This project is intended for educational and portfolio purposes. Predictions are estimates and should not be treated as guaranteed rental market prices.

## Author

Developed as a machine learning project demonstrating data preprocessing, artificial neural networks, regression evaluation, and model comparison.
