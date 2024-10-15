Deep-learning-challenge
=========

## Overview of the analysis: 

This analysis aims to develop a tool to assist the nonprofit foundation Alphabet Soup in selecting applicants. The dataset consists of a CSV file with over 34,000 organizations that have received funding from Alphabet Soup over the years.

This analysis focuses on the `IS_SUCCESSFUL` column as the target variable, with the following columns serving as features:

- **APPLICATION_TYPE:** Type of application submitted to Alphabet Soup
- **AFFILIATION:** Sector of industry the organization is affiliated with
- **CLASSIFICATION:** Classification of the government organization
- **USE_CASE:** Purpose for which funding is requested
- **ORGANIZATION:** Type of organization
- **STATUS:** Current active status of the organization
- **INCOME_AMT:** Classification of income level
- **SPECIAL_CONSIDERATIONS:** Any special considerations noted in the application
- **ASK_AMT:** Amount of funding requested


## Results: 

In this analysis, we utilized the `Scikit-learn (sklearn)` library to develop a predictive model for the Alphabet Soup nonprofit foundation. The following steps outline the process:

1.	**Data Preprocessing:**
   >Loaded the CSV file containing the dataset. Drop the non-beneficial ID `'EIN'` and ` 'NAME'`. and identify features values and replaced with `"Other"`
   
2.	**Columns Identified:**
   >Identified `IS_SUCCESSFUL` as target and relevant features, including `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT`.
   
3.	**Splitting the Data:**
   >Divided the dataset into training and testing sets to evaluate the model's performance.
   
4.	**Building the Deep Neural Network:**
   >Created a sequential model using Keras. Added an input layer, two hidden layers with 80 and 40 neurons (using ReLU activation), and an output layer with a sigmoid activation. The model input is based on the training dataset features, ensuring comprehensive learning from the data. For hidden layer, ReLU is commonly used because it helps with the vanishing gradient problem, allowing the model to learn faster and perform better.
  
5.	**Training the Model:**
    >Trained the model on the training data with a set number of epochs

6.	**Evaluate the model using the test data:**
    >Evaluated the model using the test data.
	
7.	**Result:**
    > Loss: 0.5597  and   Accuracy: 73.34%



* Attempts to achieve 75% accuracy included dropping additional columns in dataset, adjusting epochs and batch size; modifying neurons counts, adding hidden layers; adding Dropout in layers, adding hidden layers, incorporating dropout layers, specifying an Adam optimizer with a learning rate of 0.0001, and implementing early stopping callbacks. However, these adjustments led to decreasing accuracy.



## Summary: 


The model correctly identified approximately 73.34% of the applicants in the test set. The loss value of 0.5597 indicates the model's error in predicting the target variable. This approach aims to create a robust tool for Alphabet Soup to improve its applicant selection process based on historical funding data.
