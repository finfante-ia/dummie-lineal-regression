# dummie-linear-regression
Sometimes a simple feature may make a hugh difference in how to solve a lineal regression problem. This small code split the data by a categorical feature and run a linear regression per each one.

The example is particulary simple, beacause CO2 Emissions is linearly dependent by fuel consumption per each fuel type.

![plot](./images/plot1.png)

But it can be used for more complex problems.

Using this model with a test sample of 20% the results are:

|FUELTYPE | Accuracy 	|R2 	      |MSE 	      |MAE     |
| ------  |---------|-----|-----|-----|
|E 	      |0.068135 	|0.999983 	|0.068135 	|0.223066|
|Z 	      |0.086343 	|0.999980 	|0.086343 	|0.254018|
|X 	      |0.099788 	|0.999978 	|0.099788 	|0.270386|
|D 	      |0.201933 	|0.999927 	|0.201933 	|0.392293|
|Total 	  |0.095351 	|0.999979 	|0.095351 	|0.26439 |

Using DecisionTreeRegresor, with dummies features (0/1) for fuel type, the result was not as good.
| Dummie | Accuracy | R2 | MSE | MAE |
|-----|-----|-----|-----|----- |
| FUELTYPE_D | 474.4 | 0.828225 | 474.4 | 12.8 |
| FUELTYPE_E | 73.923077 | 0.981241 | 73.923077 | 3.923077 |
| FUELTYPE_X | 1.118644 | 0.999754 | 1.118644 | 0.288136 |
| FUELTYPE_Z | 4.230769 | 0.99902 | 4.230769 | 0.512821 |
| Total | 17.733645 | 0.99617 | 17.733645 | 0.883178 |

## I have two goals:

- Make this algorithm work with any current machine learning algorithm
- Design a decision tree algorithm to search the best way to split the data
