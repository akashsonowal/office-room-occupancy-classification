# office-room-occupancy-detection

**Objective:**

The objective of the project is to determine whether a given room is occupied or not, meaning whether there is some person present in the room or not based on various variables. We will be using non-linear models such as Logit and Probit in detecting the Room Occupancy.

The objective of the project is to determine whether a given room is occupied or not, meaning whether there is some person
present in the room or not based on various variables. We will be using non-linear models such as Logit and Probit in
detecting the Room Occupancy.
METHODOLOGY:
We have used Logit Regression model and Probit Regression Model to predict the Binary Dependent Variable – Occupancy.
Also, we have used Linear Probability Model to classify the dependent variable to compare linear and non-linear model.
DATA DESCRIPTION:
https://archive.ics.uci.edu/ml/datasets/Occupancy+Detection+
Dataset: Occupancy Detection Data Set
Attribute Information:
Independent variables
•
•
•
•
•
•
Date – date and time of the readings taken for a given room
Temperature – temperature of the room in degree Celsius
Humidity – relative humidity of the room
Light – intensity of light in lux
CO2 – carbon dioxide level in the room in ppm
HumidityRatio - derived quantity from temperature and relative humidity, in kgwater-vapor/kg-air
Dependent variables
•
Occupancy – binary variable (0 if room is not occupied, 1 if occupied)
Scatter Plots:
Please refer to Annexure I for all scatter plots

It can be evaluated from the boxplots that, occupied rooms have higher mean temperature than those which are not occupied,
same follows for CO2, Humidity, HumidityRatio. Also, is can seen that if a person is present in a room than it has more
chances of switching on the light which is seen in the boxplot of Light.
Model Application:
After, describing the data and getting an idea how the variables behave we will build non-linear models to predict the
dependent binary variable.
We have made a division of data points into train and test in ratio of 1:1, i.e., we have 10280 data points in training set and
another 10280 data points in testing set, split is done randomly
Probit Regression Model:
It uses Cumulative Probability Function (CDF) for determine the outcome of dependent Variable, it can be mathematically
represented as,
Pr(𝑌 = 1|𝑋) = ∅(𝑍)
𝑍 = 𝛽 0 + 𝛽 1 ∗ 𝑋 1 + 𝛽 2 ∗ 𝑋 2 + ⋯
Y = Binary Dependent Variable,X i = Independent Variables,
β i = coefficients
Φ = cumulative probability functions,
Based on our data set we, best fit Probit Regression Model is,
Pr(𝑂𝑐𝑐𝑢𝑝𝑎𝑛𝑐𝑦) = ∅(4.0622 − 0.4871 ∗ 𝑇𝑒𝑚𝑝𝑒𝑟𝑎𝑡
HumidityRatio is not present in the model equation as there is a high correlation between Humidity and
HumidityRatio, so either of them one is sufficient to explain the Binary Dependent Variable.
Coefficient of CO2 is very small compared to others as the value of CO2 in ppm is in range of 500-1000, which is
large compared to other variables such as Temperature which is in range of 15-30.
Maximum Likelihood Estimator method is used to predict the coefficients.
Log-Likelihood = -585.06, maximized value of the log-likelihood function
LL-Null = -5532.4, maximized log-likelihood function when only an intercept is included.
Pseudo R-squared = 0.8942, meaning that the model is very good fit as it is close to 1, the independent variables
are good enough to explain the dependent variable.
Logit Regression Model:
This model is popularly known as Logistic Regression Model, which uses sigmoid function to predict the probability of
Binary Dependent Variable, mathematically it can be represented as,

Y = Binary Dependent Variable,
X i = Independent Variables,
β i = coefficients
Φ = cumulative probability functions,
Best fit Logit model for the given data set is,
Pr(𝑂𝑐𝑐𝑢𝑝𝑎𝑛𝑐𝑦)
=
1
1 + 𝑒 −(4.3288 − 0.7863 ∗ 𝑇𝑒𝑚𝑝𝑒𝑟𝑎𝑡𝑢𝑟𝑒 + 0.0762 ∗ 𝐻𝑢𝑚𝑖𝑑𝑖𝑡𝑦 + 0.0236 ∗ 𝐿𝑖𝑔ℎ𝑡 + 0.0036 ∗ 𝐶𝑂2)
Summary and Observations:
Summary of the best fit Logit Regression Model is as follows,
Observations are very much similar to that of best fir Probit Regression Model
Maximum Likelihood Estimator method is used to predict the coefficients.
Log-Likelihood = -534.19, maximized value of the log-likelihood function
LL-Null = -5532.4, maximized log-likelihood function when only an intercept is included.
Pseudo R-squared = 0.9034, meaning that the model is very good fir as it is close to 1, the independent variables
are good enough to explain the dependent variable.
This is because both the models are quite efficient non-linear models for explaining the Binary Dependent Variable.Test and Results:
Variation Inflation Factor:
As both the results are having the same variables in the final model, we would perform VIF test on these variables.
Results of VIF test is given in the table below,

Variable Significance Test:
As all the variables in the final model of Probit Regression and Logit Regression are having p-value < 0.05, we can conclude
that all the variables in these models are statistically significant at 95% level.
ROC Curve:
Probit Model:
Below image shows the ROC curve for best fit Probit Model,
