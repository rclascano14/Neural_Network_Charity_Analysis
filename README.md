# Neural_Network_Charity_Analysis
`Creating a deep-learning neural network to analyze and classify the success of charitable donations.`

## Resources
- Jupyter Notebook
- Python 3.7.11
- Anaconda Navigator
- Conda
- Data: charity_data.csv

## Overview of the Analysis

In this module, I have learned to implement neural networks using the TensorFlow platform in Python. In addition to learning about the workings of nerial networks, I have been able to compare these networks to traditional machine learning models. Deep Learning Models are besr suited for complex and large datasets, whereas other machine learning models are used more aptly for smaller and less intricate datasets. With my pertinent knowledge and skills regarding Neural Networks, I am being asked to use a charity dataset to create a binary classifier that is capable of predicting the success of applicants to a business referred to as Alphabet Soup. As aforementioned, neural networks are best used for large fatasets, and our provided one contains over 34,000 organizations. Consequently, I will be utilizing various networks to test success and then attempt to optimize my created model to better predict the success of applicants. 

## Results

This assignment consists of the completion of the following 4 Deliverables:

### Deliverable 1 - Preprocessing Data for a Neural Network Model

In order to preprocess the data, the following steps were taken

- Non-beneficial ID columns such as `EIN` or `NAME` were dropped from the application dataset
- The number of unique values in each column were ascertained and binning is analyzed
- I identified the target as the `IS_SUCCESSFUL` column as we are testing the success of applicants to Alphabet Soup
- I identified the features as the `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, `ASK_AMT`

### Deliverable 2 - Compile, Train, and Evaluate the Model

- There are two hidden layers in the Neural Network Model and they have a neuron count of 80 and 30
- The model has 5,981 params
- The activation function for the two hidden layers is `relu` and the activation function for the output layer is `sigmoid`
- The optimizer is `adam` and the loss function is `binary_crossentropy`
- The accuracy of the model is 0.4689 or about 47%, which is not significant enought to be used as a predictor of success

### Deliverable 3 - Optimize the Model
In order to potentially increase the accuracy of the model, I utilized 5 different optimizations

#### Optimization 1 - Adding more neurons to a hidden layer
- I added 20 neurons to the first hidden layer of the model
- This had no effect on the accuracy of the model as it remained at 47%

#### Optimization 2 - Adding more hidden layers
- I added a third layer to the model in the hopes of improving accuracy
- This had no effect on the accuracy of the model as it remained at 47%

#### Optimization 3 - Using different activation functions for the hidden layers
- I changed the activation function of the first and second hidden layers to `tanh`
- Once again, this had no effect on the accuracy of the model

#### Optimization 4 - Adding the number of epochs to the training regimen
- I doubled the number of epochs in the model to 200
- This also had no influence upon the accuracy of the model

#### Optimization 5 - Reducing the number of epochs to the training regimen
- Lastly, I tried halfing the number of epochs in the model to 50
- Unfortunately, this resulted in no change, and the accuracy remained at 47%

### Deliverable 4 - A Written Report on the Neural Network Model (README.md) (As Seen Here)

## Summary

In summation, the accuracy of this Deep Learning Neural Network is 47%. This is well beneath my pursued accuracy score of 75%. Consequently, I would not advise the Alphabet Soup Business to utilize this model in predicting the success of applicants. Instead, I would insist that additional analysis of other optimizations or machine learning models is warranted. In regards to our analysis, we are well aware of what we are wanting out of the data, so I would suggest the usage of a supervised machine learning model. Several examples of pertinent supervised models are SVM, Logistic Regressions, and lastly, RandomForest, which I believe would be best suited to increasing the accuracy of the model. 
