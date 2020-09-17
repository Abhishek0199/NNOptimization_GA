## About:

The following code implements Genetic Algorithm for the optimization of neural network architecture which includes learning rate, activation functions and number of hidden neurons with fixed 1 or 2 hidden layers and output activation function as sigmoid because of binary classification.
The chromosome is defined as:

- Alpha (Learning Rate) -> 4 bits
  - Constraints are: >0 and <1
- Activation Functions -> 2 bits for 4 AF:
  - Relu = 00
  - Tanh = 01
  - Sigmoid = 10
  - Selu = 11
- Number of neurons in hidden layer 1 (5 bits)
  - Constraints are: >=2
- Number of neurons in hidden layer 2 (5 bits)
  - No Constraints can be from 0 to max value
- Output AF -> Sigmoid (binary classification)
