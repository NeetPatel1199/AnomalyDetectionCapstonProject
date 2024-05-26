# Anomaly Detection with Neural Networks

# Project Overview
Predictive maintenance is crucial for many industries to reduce risks and gain actionable insights from their equipment data. This project aims to predict machine breakdowns by identifying anomalies in the data, allowing for maintenance to be performed before equipment degrades or breaks down. The dataset used contains over 18,000 rows collected over a few days, with the column 'y' indicating anomalies (1 for anomaly, 0 otherwise). The remaining columns serve as predictors.

# Problem Statement
System failures can occur in any machine, making it essential to predict and prevent these failures through predictive maintenance. This project focuses on:
Evaluating the condition of equipment through online monitoring
Performing maintenance proactively to avoid breakdowns
Using a neural network to predict anomalies in the data

# Methodology

The Neural Network anomaly detection model utilizes a Sequential architecture, a type of neural network commonly employed for sequential data processing tasks. The model comprises three densely connected layers:

Input Layer: The first layer consists of 64 neurons, activated by the Rectified Linear Unit (ReLU) function, which helps introduce non-linearity into the model. This layer takes input data with dimensions determined by the shape of the scaled training data (X_train_scaled).

Dropout Layer: To prevent overfitting and enhance model generalization, a dropout layer with a dropout rate of 0.3 is incorporated after the first dense layer. Dropout randomly sets a fraction of input units to zero during training, forcing the network to learn more robust features.

Hidden Layer: The second dense layer consists of 32 neurons, also activated by the ReLU function, facilitating the extraction of higher-level features from the input data.

Dropout Layer: Similar to the first dropout layer, a dropout layer with a dropout rate of 0.3 follows the second dense layer, aiding in regularization.

Output Layer: The final layer is a single neuron activated by the Sigmoid function. The Sigmoid activation function squashes the output between 0 and 1, enabling the model to output a probability indicating the likelihood of an input sample being anomalous.

This model architecture is well-suited for detecting anomalies within datasets, as it learns complex patterns and relationships from the data and outputs a binary classification indicating normal or anomalous instances. Training this model involves optimizing its parameters to minimize the discrepancy between predicted and actual labels, thereby enabling accurate anomaly detection.
