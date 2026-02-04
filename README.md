# Neural-Network
This code imports two essential libraries for working with deep learning in Python, specifically using PyTorch: torch is the main PyTorch library, providing fundamental tensor operations and utilities. torch.nn (aliased as nn) is PyTorch's module for building neural networks, offering a variety of layers, activation functions, and loss functions.

This code defines a neural network model using nn.Sequential. This is a common way in PyTorch to stack layers sequentially. The model has three main parts:

nn.Linear(2, 4): This is the first layer, a fully connected linear layer. It takes an input of size 2 and transforms it into an output of size 4.
nn.ReLU(): This is a Rectified Linear Unit activation function. It introduces non-linearity into the model, allowing it to learn more complex patterns. It outputs the input directly if positive, otherwise zero.
nn.Linear(4, 1): This is the second linear layer. It takes the 4-dimensional output from the ReLU activation and transforms it into a single-dimensional output. This type of model could be used for tasks like simple regression where you're predicting one value from two input features.
