# Neural_Network_Charity_Analysis
## Overview of the analysis:
Our goal here is to use machine learning and neural networks, to use the  features in the provided dataset to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

We use the following methods for the analysis:

* reprocessing the data for the neural network model,
* compile, train and evaluate the model,
* optimize the model.


## Results: 

### Data Preprocessing

* What variable(s) are considered the target(s) for your model? 
The column IS_SUCCESSFUL considered as the target of this analysis. In this column, we can use binary classification to predict whether or not the charity donation was used effectively.

* What variable(s) are considered to be the features for your model?
We used columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT as features of the analysis. Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.


* What variable(s) are neither targets nor features, and should be removed from the input data?
We took out the columns of EIN and NAME from the dataframe because these two columns are not relevant to the deep-learning model.


### Compiling, Training, and Evaluating the Model

* How many neurons, layers, and activation functions did you select for your neural network model, and why?

This model is made with an input features & two hidden layers. The first hidden layer has 80 neurons, the second has 30 there is also an output layer. Each layer has an activation function. The first and second hidden layers have an activation function "relu" & the output layer is "sigmoid".

![]()

* Were you able to achieve the target model performance?
Since all our model accuracy are below 75%. In this case, the performance is not capable to help us predict the outcomes of charity donations.

* What steps did you take to try and increase model performance?

In order to optimize the model accuracy, I bucketed the Classification feature differently. When all other conditions are the same, I increased the number of neurons , increased hidden layers for the dataset, as well as change the activation function. I replaced relu function to tanh function for one of the hidden layer. However, all methods that I used did not help to increase the model accuracy.



## Summary: 

The models accuracy ended up being less than 75% . We started with a data set and tried to predict whether or not the project would be successful on all of the features that we used after dropping two features that we figured to be irrelevant. Although I did not get to the accuracy of 75% , it is possible the reason for this is we may have had to drop more features which may have affected how good the neural network actually is. Another way to increase the accuracy of  model is to have more data. If we have more data added to this model, the accuracy of this model could possibly increase.

Since we are in a binary classification situation, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.