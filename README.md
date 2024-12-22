# Handwritten Digit Recognition using Hough Transform and Neural Network

This project aims to recognize handwritten digits using neural networks and a low-dimensional feature vector. The project also explores clustering methods, but clustering attempts failed due to overlapping clusters.

## Requirements

- Python 3.12.7
- Jupyter Notebook
- Required Python packages:
  - kagglehub
  - numpy
  - matplotlib
  - scikit-learn
  - torch

## Data Preparation

The dataset used is a handwritten digits dataset not included in MNIST. The dataset is loaded and preprocessed to create feature vectors for each digit.

## Feature Extraction

Features are extracted from the images using Hough Line and Hough Circle transforms. The Hough Line Transform is used to detect lines in an image, while the Hough Circle Transform is used to detect circles. You can read more about these techniques [here](https://en.wikipedia.org/wiki/Hough_transform). The extracted features are combined into a 1D array representing each digit.

## Clustering

Clustering methods such as DBSCAN and K-Means were attempted to group similar digits. However, these attempts failed due to overlapping clusters, making it difficult to distinguish between different digits.

## Neural Network

A simple neural network is implemented using PyTorch to classify the digits. The network consists of two fully connected layers: the first layer has 128 neurons, and the second layer has 64 neurons, both with ReLU activation. The model is trained using the Adam optimizer on the extracted features and evaluated on a validation set.

## Results

The neural network achieved a validation accuracy of approximately 94%. Clustering methods were not successful due to overlapping clusters.

## Conclusion

This project demonstrates the use of neural networks for handwritten digit recognition using a low-dimensional feature vector. While clustering methods were not successful, the neural network provided good accuracy in recognizing the digits.
