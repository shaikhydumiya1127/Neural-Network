# Neural-Network

This code uses PyTorch to build and train a simple neural network.
First, the torch library is imported to work with tensors and deep learning operations.
The torch.nn module is imported to create neural network layers like linear layers and activation functions.

The neural network is created using nn.Sequential, which allows layers to be arranged one after another in order.
The first layer is a linear layer that takes 2 input values and produces 4 outputs.
Next, a ReLU activation function is applied, which adds non-linearity by turning negative values into zero.
Then, a second linear layer converts the 4 values into 1 final output.
This type of model is suitable for simple regression problems.

The input data X is a tensor with 4 samples, and each sample has 2 features.
The target data y contains output values corresponding to the inputs.
However, there is a mismatch because X has 4 samples and y has only 3, which can cause errors during training.

The training loop runs for 1000 iterations to train the model.
Before each iteration, old gradients are cleared using opt.zero_grad().
The model predicts outputs using model(X).
The loss is calculated by comparing predicted values with actual values using Mean Squared Error loss.
The loss.backward() step calculates gradients for all model parameters.
The optimizer updates the weights using opt.step() to reduce the loss.

Finally, print(model(X)) displays the model’s predictions after training.
