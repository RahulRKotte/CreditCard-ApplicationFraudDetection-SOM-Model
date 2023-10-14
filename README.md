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
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.preprocessing import MinMaxScaler
from minisom import MiniSom
```



## Importing Dataset
Load the credit card applications dataset and display some basic information about it.
```python
dataframe = pd.read_csv('Credit_Card_Applications.csv')
dataframe.head()
dataframe.shape
dataframe.info()
dataframe.columns
```

## Feature Scaling
Scale the features of the dataset to ensure that they have a consistent range.
```python
sc = MinMaxScaler(feature_range=(0, 1))
X = sc.fit_transform(X)
```

## Training SOM
Create and train the SOM model using the scaled dataset.
```python
som = MiniSom(10, 10, 15, 1.0, 0.5, random_seed=1)
som.random_weights_init(X)
som.train_random(X, 100)
```

## Visualizing the Result
Visualize the results of the SOM model by plotting the distance map and marking the detected frauds.
```python

```

## Finding The Frauds
Identify the potential frauds using the trained SOM model.
```python
mappings = som.win_map(X)
frauds = np.concatenate((mappings[(2,6)], mappings[(5,2)], mappings[(3,7)]), axis=0)
frauds = sc.inverse_transform(frauds)
```

## Finding Customers with Approved Applications
Identify customers whose credit card applications were approved.
```python
condition = dataframe['Class'] == 1
approved_df = dataframe.loc[condition, ['CustomerID', 'Class']]
```
## Customers with Approved Applications Who Are Fraudulent
Identify customers with approved applications who are also detected as potential fraudsters.
```python
approved_fraud_customers = approved_df[approved_df['CustomerID'].isin(fraud_id_list)]['CustomerID'].values
```

## Conclusion
This project demonstrates the use of a SOM model to detect credit card application fraud and identify customers with approved applications who are potential fraudsters.

Feel free to modify the code and adapt it for your specific needs.

**Note:** Ensure that you have the 'Credit_Card_Applications.csv' dataset in the same directory as your code.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
