# dummie-lineal-regression
Sometimes a simple feature may make a hugh difference in how to solve a lineal regression problem. This small code split the data by a categorical feature and run a linear regression per each one.

The example is particulary simple, beacause CO2 Emissions is linearly dependent by fuel consumption per each fuel type.

![plot](./images/plot1.png)

But it can be used for more complex problems.

Using this model with a test sample of 20% the results are:

|FUELTYPE | Accuracy 	|R2 	      |MSE 	      |MAE     |
| ------  |:---------:|:-----:|:-----:|:-----:|
|E 	      |0.068135 	|0.999983 	|0.068135 	|0.223066|
|Z 	      |0.086343 	|0.999980 	|0.086343 	|0.254018|
|X 	      |0.099788 	|0.999978 	|0.099788 	|0.270386|
|D 	      |0.201933 	|0.999927 	|0.201933 	|0.392293|
|Total 	  |0.095351 	|0.999979 	|0.095351 	|0.26439 |
