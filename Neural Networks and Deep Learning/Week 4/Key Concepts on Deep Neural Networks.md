1. We use the "cache" in our implementation of forward and backward propagation to pass useful values to the next layer in the forward propagation. True/False?
    - False **The "cache" is used in our implementation to store values computed during forward propagation to be used in backward propagation.**
2. The "cache" is used in our implementation to store values computed during forward propagation to be used in backward propagation.
    - Size of hidden layers n^[l]
    - number of iterations
    - learning rate alpha
    - number of layers L in the neural network
3. Which of the following is more likely related to the early layers of a deep neural network?
    The early layer of a neural network usually computes simple features such as edges and lines.
4. Vectorization allows us to compute 𝑎[𝑙] for all the examples on a batch at the same time without using a for loop. True/False?
    True. **Vectorization allows us to compute the activation for all the training examples at the same time, avoiding the use of a for loop.**
5. Suppose W[i] is the array with the weights of the i-th layer, b[i] is the vector of biases of the i-th layer, and g is the activation function used in all layers. Which of the following calculates the forward propagation for the neural network with L layers.
    - for i in range(1, L+1):
        Z[i] = W[i] * A[i-1] + b[i]
        A[i] = g(Z[i])
6. Consider the following neural network [Fig1] What are all the values of 𝑛[0], 𝑛[1], 𝑛[2], 𝑛[3] and 𝑛[4]?
   - 4, 4, 3, 2, 1
7. During forward propagation, in the forward function for a layer 𝑙 you need to know what is the activation function in a layer (sigmoid, tanh, ReLU, etc.). During backpropagation, the corresponding backward function also needs to know what is the activation function for layer 𝑙, since the gradient depends on it. True/False?
   - True - **As you've seen in week 3 each activation has a different derivative. Thus, during backpropagation you need to know which activation was used in the forward propagation to be able to compute the correct derivative.**
8. There are certain functions with the following properties:
(i) To compute the function using a shallow network circuit, you will need a large network (where we measure size by the number of logic gates in the network), but (ii) To compute it using a deep network circuit, you need only an exponentially smaller network. True/False?
    - True
9. Consider the following 2 hidden layer neural network [Fig2] Which of the following statements are True? (Check all that apply).
    - b^[2] will have shape (3,1)
    - b^[3] will have shape (1,1)
    - b^[1] will have shape (4,1)
    - W^[3] will have shape (1,3)
    - W^[1] will have shape (4,4)
    - W^[2] will have shape (3,4)
10. In the general case if we are training with 𝑚 examples what is the shape of 𝐴[𝑙]?
    (n^[l], m)
