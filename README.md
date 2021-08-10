# office-room-occupancy-detection

## Objective:

The objective of the project is to determine whether a given room is occupied or not, meaning whether there is some person present in the room or not based on various variables. We will be using non-linear models such as Logit and Probit in detecting the Room Occupancy.

## Approach:

- We have used Logit Regression model and Probit Regression Model to predict the Binary Dependent Variable – Occupancy. Also, we have used Linear Probability Model to classify the dependent variable to compare linear and non-linear model.
- Performed Tests – Variation Inflation Factor (VIF) for multicollinearity check, Variable Significance Test @ 95% level. 
- Evaluated models on ROC curve, Precision, Recall, F1-Score, Accuracy. 

## Result:
- Obtained accuracy as 0.99, Pseudo R2 0.9034 (Logit) and 0.8942 (Probit) 

## Data Description:

Dataset: [Occupancy Detection Data Set](https://archive.ics.uci.edu/ml/datasets/Occupancy+Detection)

Attribute Information:

        Independent variables
        - Date – date and time of the readings taken for a given room
        - Temperature – temperature of the room in degree Celsius
        - Humidity – relative humidity of the room
        - Light – intensity of light in lux
        - CO2 – carbon dioxide level in the room in ppm
        - HumidityRatio - derived quantity from temperature and relative humidity, in kgwater-vapor/kg-air
        Dependent variables:
        - Occupancy – binary variable (0 if room is not occupied, 1 if occupied)
