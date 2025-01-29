# deep-learning-challenge
Machine learning and neural networks project

## Repository Overview
- deep_learning.ipynb
  - Initial notebook used to format data and construct model.
- AlphabetSoupCharity_Optimization.ipynb
  - Notebook used to attempt to optimize model to perform better.
- h5_files
  - Directory that stores the h5 files for the models in the notebooks above.

## Overview of the Analysis
The purpose of this analysis is to develop a machine learning model for data acquired from previous charity grants received by the "Alphabet Soup" Organization. The machine learning program’s goal is to help the company make better financial decisions by accurately predicting which loans will be successful and which one’s will not be. To achieve this, it compares whether or not a loan was successful against various loan characteristics such as the application type, the organization’s affiliated sector, the organization’s classification, what the funding will be used for, the requester’s income, the loan amount, etc. 

## Results
### Data Preprocessing
- The target for this model is the "IS_SUCCESSFUL" field <br>
- The features for this model are the "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS”, “INCOME_AMT”, “SPECIAL_CONSIDERATIONS”, and “ASK_AMT” fields.
- The “NAME” and “EIN” fields were removed because they only serve as identifiers to the organization.
 
### Compiling, Training, and Evaluating the Model
- I used two hidden layers and an output layer. I used two neurons in the first layer and one in the second in order to not overload the model. I used the “relu” activations for the hidden layers and the “sigmoid” activation in the output because they seemed to be the most logical for this type of data. 
- The model achieved 71.87% accuracy and a 56.63% loss. This is slightly below the goal of 75% accuracy.
- In order to attempt to improve the model’s performance, the following steps were taken:
	1. Reduce number of buckets for application types and classification values.
	2. Add more neurons to hidden layers.
	3. Change to more optimal activation functions.
	4. Add an additional hidden layer.
	5. Double epochs to 200.

## Summary:
Overall, the model performs slightly under the 75% performance goal at 71.87%. Several changes were made but the accuracy of the model only slightly improved to 72.23%. It still performs fairly well and I would recommend that the company use it but with a grain of salt. A different, more complex model with different hidden layers and activation could improve the model, or collecting more data to improve the accuracy.
