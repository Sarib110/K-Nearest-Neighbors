# K-Nearest-Neighbors
# K-Nearest Neighbors Classifier

## Overview

This Python script implements a simple K-Nearest Neighbors (KNN) classifier for a dataset containing fruit data with color information. The classification is based on the Euclidean distance between feature vectors.

## Dependencies

- numpy (v1.19.5)
- pandas (v1.3.3)
- matplotlib (v3.4.3)

## Dataset

The dataset, "fruit_data_with_colours.xlsx," is loaded using the pandas library. It is assumed that the dataset has the following structure:

- Column 1: Fruit labels (class labels)
- Columns 2-4: Feature values (information)

## Functions

### Euclidean_distance

This function calculates the Euclidean distance between two data rows, representing training and testing instances.

### get_neighbors

Given a testing instance and the training set, this function computes the Euclidean distances and returns the indices and distances of the k nearest neighbors.

### predict_classification

Using the K-nearest neighbors, this function predicts the class label for a given testing instance.

### visualize_dataset

This function visualizes the dataset in a 3D scatter plot. Each point represents a fruit, colored according to its class label.

## Usage

```python
# Load the dataset
dataset = pd.read_excel("fruit_data_with_colours.xlsx")

# Predict the class label for a testing instance using K=5
prediction = predict_classification(dataset.values[1:], dataset.iloc[0, 1:].values, 5)
print("Predicted Class Label:", prediction)

# Visualize the dataset
visualize_dataset(dataset)
```

## Note

- Ensure that the dataset file ("fruit_data_with_colours.xlsx") is in the same directory as the script.
- Adjust the dependencies as needed, depending on your Python environment.

Feel free to explore and modify the code for your specific use case or dataset.
