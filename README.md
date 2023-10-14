# Credit Card Application Fraud Detection Using SOM Model

## Overview
This project demonstrates the use of a Self-Organizing Map (SOM) model to detect credit card application fraud. The SOM is a type of artificial neural network that can help identify patterns and anomalies in the data.

## Table of Contents
- [Dependencies](#importing-dependencies)
- [Importing Dataset](#importing-dataset)
- [Feature Scaling](#feature-scaling)
- [Training SOM](#training-som)
- [Visualizing the Result](#visualizing-the-result)
- [Finding The Frauds](#finding-the-frauds)
- [Finding Customers with Approved Applications](#finding-customers-with-approved-applications)
- [Customers with Approved Applications Who Are Fraudulent](#customers-with-approved-applications-who-are-fraudulent)

## Importing Dependencies
This section imports necessary Python libraries for data analysis, visualization, and the SOM model.
```
dataframe = pd.read_csv('Credit_Card_Applications.csv')
dataframe.head()
dataframe.shape
dataframe.info()
dataframe.columns
```


## Importing Dataset
Load the credit card applications dataset and display some basic information about it.

## Feature Scaling
Scale the features of the dataset to ensure that they have a consistent range.

## Training SOM
Create and train the SOM model using the scaled dataset.

## Visualizing the Result
Visualize the results of the SOM model by plotting the distance map and marking the detected frauds.

## Finding The Frauds
Identify the potential frauds using the trained SOM model.

## Finding Customers with Approved Applications
Identify customers whose credit card applications were approved.

## Customers with Approved Applications Who Are Fraudulent
Identify customers with approved applications who are also detected as potential fraudsters.

## Conclusion
This project demonstrates the use of a SOM model to detect credit card application fraud and identify customers with approved applications who are potential fraudsters.

Feel free to modify the code and adapt it for your specific needs.

**Note:** Ensure that you have the 'Credit_Card_Applications.csv' dataset in the same directory as your code.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
