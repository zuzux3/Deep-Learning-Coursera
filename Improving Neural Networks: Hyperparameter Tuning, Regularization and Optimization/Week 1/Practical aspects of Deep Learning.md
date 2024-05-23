1. If you have 20,000,000 examples, how would you split the train/dev/test set? Choose the best option.
    - 99% train, 0.5% dev, 0.5% test
2. The dev and test set should:
    - Come from the same distribution
3. If your Neural Network model seems to have high bias, what of the following would be promising things to try? (Check all that apply.)
    - Increase number of units in each hidden layer
    - Make the Neural Network deeper
4. You are working on an automated check-out kiosk for a supermarket and are building a classifier for apples, bananas, and oranges. Suppose your classifier obtains a training set error of 19% and a dev set error of 21%. Which of the following are promising things to try to improve your classifier? (Check all that apply, suppose the human error is approximately 0%)
    - Use a bigger network
5. In every case it is a good practice to use dropout when training a deep neural network because it can help to prevent overfitting. True/False?
    - False **In most cases, it is recommended to not use dropout if there is no overfit. Although in computer vision, due to the nature of the data, it is the default practice.**
6. The regularization hyperparameter must be set to zero during testing to avoid getting random results. True/False?
    - False **The regularization parameter affects how the weights change during training, this means during backpropagation. It has no effect during the forward propagation that is when predictions for the test are made.**
7.  Which of the following are true about dropout?
    - It helps to reduce the variance of a model
    - In practice, it eliminates units of each layer with a probability of 1 - keep_prob
8.  Decreasing the parameter keep_prob from (say) 0.6 to 0.4 will likely cause the following:
    - Increasing the regularization effect.
9.  Which of the following actions increase the regularization of a model? (Check all that apply)
    - Increase the value of hyperparameter lambda
    - Decrease the value of keep_prob in dropout
10.  Which of the following is the correct expression to normalize the input 𝑥?
    - x = (x - mu) / sigma
