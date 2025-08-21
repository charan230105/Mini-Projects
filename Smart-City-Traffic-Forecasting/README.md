## Traffic Volume Prediction using Machine Learning

## Overview
This project aims to forecast traffic volume at different junctions in a smart city using machine learning. The dataset includes traffic data along with temporal features such as hour, day, month, weekday, and holidays.

## Dataset
- **File:** `Dataset.csv`
- **Columns:**
  - `DateTime`: Timestamp of the recorded traffic data
  - `Junction`: Junction number
  - `Vehicles`: Count of vehicles at the given timestamp
  - Additional derived features such as `Hour`, `Day`, `Month`, `Weekday`, and `Holiday`

## Requirements
Make sure you have the following Python libraries installed:
```
pandas
numpy
matplotlib
scikit-learn
```
Install them using:
```
pip install pandas numpy matplotlib scikit-learn
```

## Code Workflow
1. **Import Libraries**: Load necessary Python libraries.
2. **Load Dataset**: Read `ML2.csv` and parse `DateTime`.
3. **Feature Engineering**:
   - Extract `Hour`, `Day`, `Month`, `Weekday` from `DateTime`.
   - Identify holidays using `USFederalHolidayCalendar`.
4. **Prepare Data for Training**:
   - Select `Junction`, `Hour`, `Day`, `Month`, `Weekday`, `Holiday` as features.
   - Define `Vehicles` as the target variable.
   - Split data into training (80%) and testing (20%) sets.
5. **Train Model**: Use `RandomForestRegressor` to learn from training data.
6. **Predict & Evaluate**:
   - Predict vehicle count on test data.
   - Calculate Mean Absolute Error (MAE) to evaluate performance.
7. **Visualization**:
   - Plot actual vs. predicted traffic volume using a bar chart.

## Output
- **Mean Absolute Error (MAE)**: Displays model accuracy.
- **Bar Graph**: Visualizes actual vs. predicted traffic volume.


