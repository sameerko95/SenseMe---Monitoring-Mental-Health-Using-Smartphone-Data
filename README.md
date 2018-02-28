# predict-emotional-state
There are often cases where university students undergo depression, stress or loneliness and early detection of the symptoms can prove to be very useful.
Our aim is to analyze the user’s mental health using smartphone sensor and usage data, and predict whether a particular user is experiencing any mental instability.

The target variable is the level of depression and stress faced by the student, which is obtained using various survey data taken at regular intervals.
As the dataset is highly inconsistent, we have generated all the features by summarizing existing attributes.
We have implemented a Lasso Linear Regression model because of the nature of our dataset.
We are collecting data from varied sources such as sensors, call logs, surveys etc., so there is a possibility that some features are redundant.

We have used Root mean square error (RMSE) as the evaluation metric for our model.
RMSE squares the errors, hence eliminating the sign of the error, giving a more accurate magnitude for the error.

### Results
  - People who engage in long duration phone calls, read books, and / or watch Movies & TV are least stressed.
  - Stressed students do not sleep for longer duration and are dissatisfied with their sleep, also they tend to ask lot of questions on Piazza.
  - There exists a correlation of both stress and depression with the dining place.
  - People undergoing depression tend to avoid interaction with people by not engaging much in phone calls, conversation, and SMS.
  - We trained a lasso regression model for different values of alpha (provides a trade-off between balancing RSS and magnitude of coefficients)
    over a logarithmic scale and found that for a certain value (usually 0.001 to 0.002) of alpha, the Root Mean Square Error was the least, 
    which is considered decent value for a predictive model.
