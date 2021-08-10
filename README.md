# office-room-occupancy-detection

## Objective:

The objective of the project is to determine whether a given room is occupied or not, meaning whether there is some person present in the room or not based on various variables. We will be using non-linear models such as Logit and Probit in detecting the Room Occupancy.

## Approach:

- We have used Logit Regression model and Probit Regression Model to predict the Binary Dependent Variable – Occupancy. Also, we have used Linear Probability Model to classify the dependent variable to compare linear and non-linear model.

## Data Description:

https://archive.ics.uci.edu/ml/datasets/Occupancy+Detection

Dataset: Occupancy Detection Data Set

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
