# Neural Network Charity Analysis

## Overview
AlphabetSoup is a non-profit foundation founded to help organizations to protect the environment, improve people’s well-being, and unite the world. AlphabetSoup has raised and donated over $10 billion USD dollars in the past 20 years. This money was used to invest in lifesaving technology and helped reforestation groups throughout the world. The purpose of this analyzation is to see the impact of each donation and vet those who could potentially given funds. This ensures the money is being used effectively.

A deep learning neural network was designed using python’s tensorflow library. The model evaluates all types of data that was inputed and produced a clear decision-making result. Utilizing the features within the dataset, a binary classifier was created to see if applicants would be successful if funded. The dataset contained more than 34,000 organizations that over the years have gotten funds. Each organization is captured with the following columns used in the dataset: 

* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME_AMT**—Income classification
* **SPECIAL_CONSIDERATIONS**—Special consideration for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively


### Resources Utilized to Complete Analysis
* **Data Sources:** 
[charity_data.CSV](https://github.com/cmmgw/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv) 
* **Languages:** Python
* **Python Dependencies:** scikit-learn, pandas, tensorflow, os
* **Tools:** Jupyter Notebook

## Results

### Data Preprocessing
* **What variable(s) are considered the target(s) for the model?** The "IS_SUCCESSFUL" column is the target, as it contains data on whether the donations were used effectively. The target variable is the dependent variable, y.  
* **What variable(s) are considered to be the features for the model?** The following variables are considered to be the features for the model: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT. These variables are the independent variables, x.
* **What variable(s) are neither targets nor features, and should be removed from the input data?** The identification columns EIN and NAME were dropped, as they are not beneficial when completing the analysis.

### Compiling, Training, and Evaluating the Model
* **How many neurons, layers, and activation functions were selected for the neural network model, and why?** For the deep neural network model, 80 neurons were in the first hidden layer and 30 neurons were in the second hidden layer. The ReLU activation function was utilized on both hidden layers. An advantage for using the ReLU activation function is that it identifies nonlinear characteristics from the input values. If the output of the linear transformation is less than 0, the neurons will be deactivated. 
* **Was target model performance achieved?** Performance of 75% accuracy was not achieved by the target model, as it attained 73.78%. 
* **What steps were taken to try and increase model performance?** In an attempt to optimize model performance, a third hidden layer was added with 15 neurons and the activation functions were adjusted. The first hidden layer maintained the ReLU activation function, however the second and third layers utilized the Sigmoid activation function. Unfortunately, performance of 75% was not achieved by the optimized model. 


## Summary
Despite attempting to optimize the model four times, performance of 75% was not achieved. In an attempt to optimize model accuracy, it is recommended to adjust the number of hidden layers and neurons, along with the corresponding activation functions for each layer.
