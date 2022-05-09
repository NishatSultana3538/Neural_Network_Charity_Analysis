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
We used columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT as features of the analysis.

* What variable(s) are neither targets nor features, and should be removed from the input data?
We took out the columns of EIN and NAME from the dataframe because these two columns are not relevant to the deep-learning model.




### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
In this project, we used 2 hidden layers with 80 and 30 neurons with relu activation function for the deep-learning model. After the train-test split, there are 25,724 samples and 43 features in this dataset. As we will use binary classification for output, we use sigmoid function for the output layer. For compilation, we use adam optimizer and binary_crossentropy loss function.


* Were you able to achieve the target model performance?
Since all our model accuracy are below 75%. In this case, the performance is not capable to help us predict the outcomes of charity donations.

* What steps did you take to try and increase model performance?

In order to optimize the model accuracy, I bucketed the Classification feature differently. When all other conditions are the same, I increased the number of neurons , increased hidden layers for the dataset, as well as change the activation function. I replaced relu function to tanh function for one of the hidden layer. However, all methods that I used did not help to increase the model accuracy.



## Summary: 



Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
