# Bike Demand Prediction Using Machine Learning

This project predicts the hourly number of rented bikes using weather and time-related data from the Seoul Bike Sharing Demand dataset.

Two machine learning models were trained and compared:

- Linear Regression
- Random Forest Regressor

Random Forest achieved the best performance for this dataset.

## Project Files

```text
bike-demand-prediction-ml/
├── bike_demand_prediction_ml.ipynb
├── SeoulBikeData.csv
├── requirements.txt
└── README.md
```

## Project Workflow

1. Load the dataset
2. Rename and prepare the columns
3. Create date features
4. Convert categorical values into numeric columns
5. Create `Day_Type` as Work or Leisure
6. Explore hourly and seasonal bike demand
7. Split the data into training and testing sets
8. Train Linear Regression and Random Forest models
9. Evaluate both models using RMSE and R²
10. Test the models on a real-world scenario

## Models Used

### Linear Regression

Used as a simple baseline model.

### Random Forest Regressor

Used to capture more complex and nonlinear relationships between weather, time, and bike demand.

## Model Results

| Model | RMSE | R² |
|---|---:|---:|
| Linear Regression | 435.58 | 0.5363 |
| Random Forest | 170.86 | 0.9287 |

Random Forest performed better because it achieved:

- Lower RMSE
- Higher R² Score

## Feature Importance

The Random Forest model showed that the most important features included:

- Temperature
- Hour
- Solar Radiation
- Humidity

## Real-World Scenario

The models were tested using the following conditions:

- Monday
- Summer
- 8:00 AM
- 25°C
- No rain
- Working day

| Model | Predicted Bike Demand |
|---|---:|
| Linear Regression | 1005 bikes |
| Random Forest | 1988 bikes |

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## How to Run

Install the required libraries:

```bash
pip install -r requirements.txt
```

Then open `bike_demand_prediction_ml.ipynb` using Visual Studio Code or Jupyter Notebook and select **Run All**.

## Dataset

Seoul Bike Sharing Demand Dataset.

Source: Kaggle.

## Author

Ali Shaya Al-Masar
