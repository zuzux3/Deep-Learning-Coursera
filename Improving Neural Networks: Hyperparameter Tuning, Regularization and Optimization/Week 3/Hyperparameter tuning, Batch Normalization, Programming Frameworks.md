1. With a relatively small set of hyperparameters, it is OK to use a grid search. True/False?
    - True 
**When the set of hyperparameters is small like a range for 𝑛𝑙=1,2,3 grid search works fine.**
2. Every hyperparameter, if set poorly, can have a huge negative impact on training, and so all hyperparameters are about equally important to tune well. True or False?
    - False
**We've seen in the lecture that some hyperparameters, such as the learning rate, are more critical than others.**
3. Even if enough computational power is available for hyperparameter tuning, it is always better to babysit one model ("Panda" strategy), since this will result in a more custom model. True/False?
    - False
**Although it is possible to create good models using the "Panda" strategy, obtaining better results is more likely using a "caviar" strategy due to the number of tests and the nature of the deep learning process of ideas, code, and experiment.**
4. Knowing that the hyperparameter 𝛼 should be in the range of 0.00001 and 1.0, which of the following is the recommended way to sample a value for 𝛼?
    - r = -5 * np.random.rand()
      alpha = 10**r
**This will generate a random value between 10**−5 and 10**0 chosen randomly in a logarithmic scale.**
5. Once good values of hyperparameters have been found, those values should be changed if new data is added or a change in computational power occurs. True/False?
    - True
**The choice of some hyperparameters such as the batch size depends on conditions such as hardware and quantity of data.**
6. When using batch normalization it is OK to drop the parameter 𝑊[𝑙] from the forward propagation since it will be subtracted out when we compute 𝑧~[𝑙]= 𝛾 𝑧_normalize[𝑙] + 𝛽[𝑙]. True/False?
    - False
**The parameter 𝑊[𝑙] doesn't get subtracted during the batch normalization process, although it gets re-scaled.**
7. In the normalization formula 𝑧_𝑛𝑜𝑟𝑚(𝑖) = (𝑧(𝑖)−𝜇) / (𝜎**2+𝜀)**0.5, why do we use epsilon?
    - To avoid division by zero.
8. Which of the following are true about batch normalization?
    - The parameters 𝛾[𝑙] and 𝛽[𝑙] set the variance and mean of 𝑧~[𝑙]
**When applying the linear transformation 𝑧~[𝑙]=  𝛽[𝑙] 𝑧_norm[𝑙] + 𝛾 we set the variance and mean of 𝑧~[𝑙].**
    - When using batch normalization we introduce two new parameters 𝛾[𝑙], 𝛽[𝑙] that must be "learned" or trained.
**Batch normalization uses two parameters 𝛽 and 𝛾 to compute 𝑧~[𝑙]=  𝛽[𝑙] 𝑧_norm[𝑙] + 𝛾**
9. After training a neural network with Batch Norm, at test time, to evaluate the neural network on a new example you should:
    - Perform the needed normalizations, use 𝜇 and 𝜎**2 estimated using an exponentially weighted average across mini-batches seen during training,
10. Which of these statements about deep learning programming frameworks are true? (Check all that apply)
    - A programming framweork allows you to code up deep learning algorithms with typically fewer lines of code than a lower-level language such as Python.
    - Even if a project is currently open source, good governance of the project helps ensure it remains open even in the long term, rather than become closed or modified to benefit only one company.
