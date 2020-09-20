## About:

The following code implements Genetic Algorithm for the optimization of neural network architecture which includes learning rate, activation functions and number of hidden neurons with fixed 1 or 2 hidden layers and output activation function as sigmoid because of binary classification. The training for each neural network will be done using Keras python library.
The chromosome is defined as:

- Alpha (Learning Rate) -> 4 bits
  - Constraints are: > 0 and < 1
  - The value of alpha is calculated by get the decimal value as though the bits were after decimal i.e. if alpha is represented as - 0010 -> (1/2^1)*0 + (1/2^2)*0 + (1/2^3)*1 + (1/2^4)*0.
- Activation Functions -> 2 bits for 4 AF:
  - Relu = 0
  - Tanh = 1
  - Sigmoid = 2
  - Selu = 3
- Number of neurons in hidden layer 1 (5 bits)
  - Constraints are: >=2
- Number of neurons in hidden layer 2 (5 bits)
  - No Constraints can be from 0 to max value
- Output AF -> Sigmoid (binary classification)
- The population size = 30
- The chromosome size = 4 + 2 + 5 + 5 = 16
- Number of epochs for each training is 25
- We are using the same activation function for both the hidden layers and the input layer.

## Generation of Initial Population:

The chromosome is taken to be an integer array where each bit or value is a separate gene. For the generation of the initial population we will generate each parameter of the neural network is generated bit-wise. This is done by tossing a coin or generating a random number between 0 and 1, and then if it is greater than 0.5 then the bit is set, else the bit is unset. Also, we keep track of the constraints imposed on the number of hidden neurons.
