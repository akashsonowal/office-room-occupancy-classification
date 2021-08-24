# office-room-occupancy-classification

## Objective:

To determine whether a given room is occupied or not, meaning whether there is some person present in the room or not based on various variables.

## Approach:

- Applied Linear Probability model, Non-Linear Logit and Probit models to predict the Occupancy class. 
- Used Variation Inflation Factor (VIF) for multicollinearity check, Variable Significance Test with 95% confidence for feature selection. 
- Evaluated and compared models on F1-Score, Accuracy for all models and Pseudo R<sup>2</sup> for non-linear models.

## Result:
- Obtained best accuracy of 0.98, F1-Score of 0.97, Pseudo R<sup>2</sup> of 0.9034 with Logit model.

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
