1. Which of the following are true? (Check all that apply.)
    - a^[2](12) denotes the activation vector of 2nd layer for the 12th training example.
    - a_4 ^[2] is the activation output by the 4th neuron of the 2nd layer
    - a^[2] denotes the activation vector of the 2nd layer 
2. The sigmoid function is only mentioned as an activation function for historical reasons. The tanh is always preferred without exceptions in all the layers of a Neural Network. True/False?
    False - **Yes. Although the tanh almost always works better than the sigmoid function when used in hidden layers, thus is always proffered as activation function, the exception is for the output layer in classification problems.**
3. Which of the following is a correct vectorized implementation of forward propagation for layer 2?
    Z^[2] = W^[2] A^[1] + b^[2]
    A^[2] = g^[2](Z^[2])
4. You are building a binary classifier for recognizing cucumbers (y=1) vs. watermelons (y=0). Which one of these activation functions would you recommend using for the output layer?
    Sigmoid **Yes. Sigmoid outputs a value between 0 and 1 which makes it a very good choice for binary classification. You can classify as 0 if the output is less than 0.5 and classify as 1 if the output is more than 0.5. It can be done with tanh as well but it is less convenient as the output is between -1 and 1.**
5.  Consider the following code:
    **A = np.random.randn(4,3)
    B = np.sum(A, axis = 1, keepdims = True)**
    What will be B.shape? (If you’re not sure, feel free to run this in python to find out).
    *(4,1)* - Yes, we use (keepdims = True) to make sure that A.shape is (4,1) and not (4, ). It makes our code more robust.
6.  Suppose you have built a neural network with one hidden layer and tanh as activation function for the hidden layers. Which of the following is a best option to initialize the weights?
    Initialize the weights to small random numbers. - **The use of random numbers helps to "break the symmetry" between all the neurons allowing them to compute different functions. When using small random numbers the values 𝑧^[𝑘] will be close to zero thus the activation values will have a larger gradient speeding up the training process.**
7.  Logistic regression’s weights should be initialized randomly rather than to all zeros, because if you initialize to all zeros, then logistic regression will fail to learn a useful decision boundary because it will fail to “break symmetry”, True/False?
    False - **Yes, Logistic Regression doesn't have a hidden layer. If you initialize the weights to zeros, the first example x fed into the logistic regression will output zero but the derivatives of the Logistic Regression depend on the input x (because there's no hidden layer) which is not zero. So at the second iteration, the weights’ values follow x's distribution and are different from each other if x is not a constant vector.**
8.  Which of the following are true about the tanh function?
    - The tanh is mathematically a shifted version of the sigmoid function.
    - For large values the slope is close to zero.
9.  Consider the following 1 hidden layer neural network: [Fig1.png] Which of the following statements are True? (Check all that apply).
    - b^[1] will have shape (4,1)
    - W^[2] will have shape (1,4)
    - b^[2] will have shape (1,1)
    - W^[1] will have shape (4,2)
10.  What are the dimensions of 𝑍[1] and 𝐴[1]? [Fig2.png]
    Z^[1] and A^[1] are (4,m)
