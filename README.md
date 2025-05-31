# SF Emergency Response Prediction

This project uses public 911 call data from the San Francisco Fire Department to model and predict emergency response times in minutes. The goal is to understand what factors impact how quickly units arrive on scene and to identify operational patterns that could help public agencies improve efficiency.

## Data

- Source: SF Open Data Portal  
- Dataset: Fire Department and Emergency Medical Services Calls for Service  
- Records: ~130,000 calls from 2016–2024  
- Target: `response_time` = minutes between call received and unit on scene

## Workflow

- Cleaned and filtered timestamp data
- Engineered features (hour, weekday, call type, unit type, station area, etc.)
- Built modeling pipeline with one-hot encoding and imputation
- Tested multiple regression models using RMSE and R²

## Best Model

- Gradient Boosting Regressor  
- Test RMSE: 4.68  
- Test R²: 0.32  
- Most important features: priority level, unit type, zip code

## Files

- `wrangling_eda.ipynb`: Data cleaning, feature engineering, and EDA
- `modeling.ipynb`: Preprocessing, modeling, evaluation, feature importance
- `cleaned_fire_response_data.csv`: Final processed dataset
- `Capstone3_Final_Report.pdf`: Written project summary

## Outcome

Model performance was moderate but reliable. Top predictors were operational in nature (e.g., unit priority and type). Results can support future city resource planning and analysis of dispatch delay trends.

