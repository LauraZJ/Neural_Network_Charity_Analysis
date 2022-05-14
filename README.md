# Neural_Network_Charity_Analysis

## Purpose

The purpose of this project is to use Tensorflow, neural networks in Python to analyze the success of charitable donations (with classification).  Overarching process includes:
* preprocessing the data
* compiling, training, and evaluating the model
* optimizing the model

## Results

### Data Preprocessing for a Neural Network 
* Identification information, EIN and NAME columns, were removed
* The IS_SUCCESSFUL column was identified as the target
* The APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT columns were selected as the features.
* The categorical variables were encoded and split into training and testing datasets.  Standardization was applied in the features.

### Compile, Train and Evaluate the Model 

* This neural network model (deep-learning) is made of two hidden layers, one with 80 and the other with 30 neurons.
* The input data has 43 features and 25,724 samples.
* The output layer is a binary classification.
* ReLU was used as activation function for the hidden layers and Sigmoid was used on the output layer.
* The optimizer is adam and the loss function is binary_crossentropy.


### Acuracy

* The initial model's accuracy is less than optimal at 73%(0.7286297082901001).  We would like to have at least 75% accuracy to help predict the outcome of the charity donations.
* In the second attempt, in an effort to increase the performance of the model, we applied bucketing to the ASK_AMT and organized the different values by intervals, increased the number of neurons on one of the hidden layers and used a model with three hidden layers.  The accuracy was barely improved, still at 73% (0.7300291657447815).
* I also used the tahn activation function in the last attempt. We increased the number of neurons on one of the hidden layers (with three hidden layers).  The accuracy in this final attempt was slightly better than our first attempt but not quite as good as the second attempt at 73% (0.7297959327697754)

## Summary
Essentially, all efforts produced 73% accuracy -- below the desired 75% target.  Given that this deep learning neural network model didn't achieve the desired results, we could consider using Random Forest Classifier (a supervised machine learning model), with this binary classification and multiple decision trees to generate a classified output and evaluate its performance against this deep learning model.