# Credit Card Application Fraud Detection Using SOM Model

This repository contains a Python script for credit card application fraud detection using a Self-Organizing Map (SOM) model. The SOM is used to identify patterns and anomalies in the data, helping to detect fraudulent credit card applications.

## Dependencies

Before running the script, make sure to install the necessary Python dependencies. You can do this using `pip`:

```bash
pip install numpy pandas matplotlib minisom
- `numpy` for numerical operations.
- `pandas` for data manipulation.
- `matplotlib` for data visualization.
- `minisom` for the Self-Organizing Map implementation.

## Usage

1. **Importing and Preprocessing Data**:
   - The code starts by importing the required libraries and loading the credit card application dataset from the 'Credit_Card_Applications.csv' file.
   - It then splits the data into features (X) and the target variable (y), performing feature scaling to normalize the data.

2. **Training Self-Organizing Map (SOM)**:
   - A Self-Organizing Map (SOM) is created using the `MiniSom` library with a specified grid size.
   - The SOM's weights are initialized randomly, and it is trained on the dataset for a specified number of iterations.

3. **Visualizing the Result**:
   - The code visualizes the SOM's result by plotting a grid and coloring the grid cells based on the distance between neurons.
   - It also plots data points on the grid to visualize how well the SOM separates different classes.

4. **Finding The Frauds**:
   - The script identifies potential fraud cases by mapping data points to their winning neurons on the SOM grid.
   - It concatenates the frauds found at specific neuron locations and converts them back to the original feature values.

5. **Identifying Approved Fraud Cases**:
   - The code filters and identifies customers whose applications were approved (Class = 1) in the dataset.
   - It then finds customers who are detected as fraud cases by the SOM but still got their applications approved.

6. **Output**:
   - The script prints the Customer IDs of all detected fraud cases and those who had their applications approved despite being identified as fraud.

## Credits

- This code uses the `MiniSom` library for Self-Organizing Maps.
- Dataset source: Find it in the repository

