# Flight Safety Predicition


## Project Description

**Overview** : This project uses machine learning to predict if the weather conditions are feasible for flight or not.  
**Purpose** : The  goal is to create a model that can accurately predict flight safety to assist in decision-making for flight operations.  

## DataSet

**Description**  
The "weather_data.csv" contains these columns:
* Rain (cm)
* Visibility (km)
* Wind_speed_180m (km/h)
* Temperature_180m (Celsius)

  
To classify flight safety, the following thresholds are used for the weather conditions:  

  * Rain: If the rain exceeds 2.5 cm per hour, the flight is considered unsafe.
   * Visibility: If visibility is less than 1.6 km (1600 meters), the flight is considered unsafe.
   * Wind Speed at 180 meters: If the wind speed exceeds 46.3 km/h, the flight is considered unsafe.
   * Temperature at 180 meters: If the temperature is below -10°C or above 35°C, the flight is considered unsafe.

**Source**:
The data is acquired via openmeteo api and some of it is synthethic 

**Preprocessing**:
EDA(Exploratory Data Analysis) was performed before implementation of the ML model. The "Safety_status" column was encoded as it is a categorical variable  

## Model  
**Logistic Regression** : Logistic Regression is a simple and highly interpretable model that is particularly well-suited for binary classification problems like predicting whether a flight is "Safe" or "Unsafe."
The model provides clear insights into the relationship between the independent variables (rain, visibility, wind speed, and temperature) and the probability of the target outcome. Additionally, Logistic Regression is less prone to overfitting,
especially in cases where the dataset size is small, making it a robust choice for your project.  

## Results   
The Logistic Regression model achieved an accuracy of 1.00 on the testing data. 
However, it's important to note that the dataset used for training and testing is relatively small, which can limit the model's generalizability. 
While the model performs well overall, there are instances where it doesn't predict correctly for certain variables, likely due to the limited amount of data and potential overfitting.  


## References 
[Open-mateo](https://open-meteo.com/) : To acquire weather forecasting data  
[Geopy](https://pypi.org/project/geopy/) : To acquire co-ordinates of specific cities  







