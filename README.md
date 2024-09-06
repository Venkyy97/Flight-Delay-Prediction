# Flight-Delay-Prediction


## Overview
This project is part of the **Applied Machine Learning** course at the University of Texas, Dallas. Our objective was to build a predictive model to forecast flight delays using historical data, helping airlines and passengers manage potential delays more effectively.

The project utilized various machine learning models to analyze factors such as weather conditions, flight schedules, and airport congestion, which influence flight delays.

## Project Objectives
- Develop a machine learning model to predict flight delays based on historical data.
- Identify key factors that impact flight delays (e.g., weather, airport congestion, carrier details).
- Evaluate the performance of different classification models and improve them through hyperparameter tuning.

## Dataset
We used a dataset sourced from **Kaggle**, which originally comes from an IEEE transportation research paper. The dataset contains:
- 28,000 rows and 23 columns
- Data from **JFK Airport** between November 2019 and December 2020
- Features including weather (temperature, humidity, wind speed), flight details (departure, scheduled times), and flight delay (target variable)

Key features include:
- **Weather conditions** (temperature, humidity, wind speed, pressure)
- **Flight details** (departure delay, scheduled time, carrier code)
- **Temporal information** (day of the week, month, time of day)

## Data Preprocessing
- **Standardized Column Names**: Renamed columns for clarity and consistency.
- **Deduplication**: Removed any duplicate rows to ensure data integrity.
- **Feature Selection**: Focused on key features by removing irrelevant columns (e.g., day of the month, tail number).
- **Wind Direction Conversion**: Converted wind direction into degrees for standardized representation.
- **Target Variable Creation**: Created the target variable, **departure delay**, using actual vs. scheduled departure times.

## Exploratory Data Analysis (EDA)
We performed EDA to identify trends and relationships in the data, focusing on:
- **Departure delays by airline**: Determined which airlines were more prone to delays.
- **Weather impact**: Explored how weather conditions such as "Mostly Cloudy" affected delays.
- **Airport performance**: Analyzed delay frequency across major airports like LAX, BOS, and SFO.

### Sample Visualizations:
1. **Flight Delays by Airline**  
   A graph showing which airlines have the highest percentage of delayed flights.
![image](https://github.com/user-attachments/assets/bac22af0-010c-4978-bc5d-a288ccf16589)

2. **Weather vs. Delays**  
   This graph visualizes how weather conditions impact flight delays.
![image](https://github.com/user-attachments/assets/8e363283-e687-4867-86f9-3846257db436)

3. **Delays by Airport**  
   A comparison of the delay frequency at major airports, including LAX, BOS, and SFO.
![image](https://github.com/user-attachments/assets/d0e5c78f-55bb-4260-a038-51b64b5dbca3)

## Machine Learning Models
We tested several machine learning models to classify whether a flight would be delayed:
- **Logistic Regression**
- **Decision Trees**
- **Bagging**
- **Isolation Forest**
- **XGBoost** (best-performing model)

### XGBoost Model
The XGBoost model outperformed other models, achieving:
- **Training accuracy**: 99%
- **Testing accuracy**: 90%

### Model Evaluation
We used the following evaluation metrics to assess model performance:
- **Accuracy**: Overall prediction correctness.
- **Precision & Recall**: How well the model predicts delayed vs. non-delayed flights.
- **ROC Curve & AUC**: Evaluated model performance across different thresholds.

## Feature Importance
We analyzed which features had the most significant impact on flight delays. The top features include:
- **Scheduled Departure Time**
- **Carrier**
- **Weather Conditions (e.g., temperature, wind speed)**

## Testing on Unseen Data
The model was tested on unseen data and achieved an accuracy of 90%. It successfully predicted 9 out of 10 flight delays.

## Technologies Used
- **Python** (Pandas, NumPy, Scikit-learn, PyCaret, XGBoost)
- **Jupyter Notebooks** for analysis and model development
- **Matplotlib & Seaborn** for visualizations

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/flight-delay-prediction.git
