# house-price-prediction-ml
House price prediction using Multiple Linear Regression with Python, Pandas, NumPy, Matplotlib and Scikit-learn.
# House Price Prediction using Multiple Linear Regression

This project uses **Multiple Linear Regression** to predict house prices based on different property features.

The model uses the following features:

* Area of the house in square feet
* Number of bedrooms
* Age of the property
* Distance from the city

The target variable is the **House Price in Lakhs**.

## Dataset

The dataset contains **160 records** and **6 columns**.

| Column            | Description                          |
| ----------------- | ------------------------------------ |
| Property_ID       | Unique property ID                   |
| Area_sqft         | Area of the property in square feet  |
| Bedrooms          | Number of bedrooms                   |
| Age_years         | Age of the property                  |
| Distance_City_km  | Distance from the city in kilometers |
| House_Price_Lakhs | House price in lakhs                 |

## Machine Learning Model

The project uses **Multiple Linear Regression** from Scikit-learn.

The model predicts the house price using four independent variables:

```text
Area_sqft
Bedrooms
Age_years
Distance_City_km
```

Target:

```text
House_Price_Lakhs
```

## Workflow

1. Import the required libraries
2. Load the dataset
3. Explore the dataset
4. Select features and target
5. Split the data into training and testing sets
6. Create the Linear Regression model
7. Train the model
8. Make predictions
9. Compare actual and predicted prices
10. Evaluate the model using MSE, RMSE and R²

## Train-Test Split

The dataset is divided into:

* **80% training data**
* **20% testing data**

The split uses `random_state=42`.

## Model Coefficients

The trained model produced the following coefficients:

| Feature          | Coefficient |
| ---------------- | ----------: |
| Area_sqft        |    0.046232 |
| Bedrooms         |    8.638083 |
| Age_years        |   -0.622968 |
| Distance_City_km |   -1.100034 |

**Intercept:** `4.624057`

The coefficients show how each feature contributes to the predicted house price while considering the other features in the model.

## Model Evaluation

The model is evaluated using:

### Mean Squared Error (MSE)

MSE measures the average squared difference between the actual and predicted house prices.

### Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and represents the prediction error in the same unit as the target.

### R² Score

R² shows how well the model explains the variation in house prices.

The notebook calculates all three metrics:

```python
mse = mean_squared_error(y_test, y_pred)
rmse = np.sqrt(mse)
r2 = r2_score(y_test, y_pred)
```

The notebook records an **R² score of approximately 0.9742**.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## Libraries

```text
pandas
numpy
matplotlib
scikit-learn
```

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/house-price-prediction-multiple-regression.git
```

### 2. Open the project folder

```bash
cd house-price-prediction-multiple-regression
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

```bash
jupyter notebook
```

Open:

```text
Multiple Regression.ipynb
```

Run the cells from top to bottom.

## Project Output

The model generates predicted house prices and compares them with the actual prices.

Example:

| Actual Price | Predicted Price |
| -----------: | --------------: |
|        37.07 |           37.82 |
|        82.68 |           80.57 |
|        76.48 |           69.98 |
|       126.91 |          127.92 |
|        94.51 |           99.54 |

## Project Goal

The main goal of this project is to understand how **Multiple Linear Regression** can be used to predict a continuous value using multiple input features.

This project also demonstrates the complete basic machine learning workflow from loading the dataset to evaluating the trained model.

## Author

**Ashi**
