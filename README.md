# Charity Analysis using Neural Networks

## Overview 

The client, Alphabet Soup, donates to organizations that help protect and promote the environment. They noticed that some of these donations did not have a significant impact. We were therefore tasked with developing a deep learning model that would more accurately vet possible recipients of these donations in terms of the likely impact. 

We therefore preprocessed the data, trained the dataset, and tried several different deep learning models.  

## Results 

### Data Preprocessing 

* Target variable: "Is_SUCCESSFUL" column
* Feature variables: "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT"
* Removed variables: "EIN", "NAME"

### Compiling, Training, and Evaluating the Model 

Initial deep learning model: 
* Layers: two hidden layers with 80 and 30 nodes respectively 
* Activation function: ReLU was used for the input layers, because of it's ability to handle nonlinear data. The sigmoid activation function was used for the output layer in order to better predict probability of the binary classification  

![initial](https://github.com/msprech/Neural_Network_Charity_Analysis/blob/44f3a45eba37af2ae2b84c9df069f013591199fe/Screen%20Shot%202022-01-14%20at%203.12.56%20PM.png)

Target model performance models:
* We were not able to create a target model that achieved over 75% accuracy
We tried the following methods to increase performance accuracy 
* We first added a third hidden layer with 15 neurons which yielded .74 accuracy 
* We then tried adjusting the activation function for the input layers to the tanh function which gave .742 accuracy 
* We finally attempted to run the model for slightly longer, at 150 epochs, to avoid any risk of overfitting which gave .74 accuracy


## Summary 

The deep learning model should be reevaluated to increase the accuracy percentage. There are several other methods for improving the performance of a deep learning model, in particular focusing on the preprocessing stage since our analysis centered around later stages of the model. 

Other machine learning models that perform competitively to deep learning models should also be considered. Since we are focused on tabular data, Random Forest could be a good fit. In basic binary classification problems, logistic regression models can also outperform neural networks in terms of limiting overfitting. 
