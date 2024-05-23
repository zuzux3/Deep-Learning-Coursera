1. Using the notation for mini-batch gradient descent. To what of the following does 𝑎[2]{4}(3)correspond?
    - The activation of the second layer when the input is the third example of the fourth mini-batch.
**In general 𝑎[𝑙]{𝑡}(𝑘) denotes the activation of the layer 𝑙 when the input is the example 𝑘 from the mini-batch 𝑡.**
2. Suppose you don't face any memory-related problems. Which of the following make more use of vectorization.
    - Batch Gradient Descent
**If no memory problem is faced, batch gradient descent processes all of the training set in one pass, maximizing the use of vectorization.**
3. We usually choose a mini-batch size greater than 1 and less than 𝑚, because that way we make use of vectorization but not fall into the slower case of batch gradient descent.
    - True
**Precisely by choosing a batch size greater than one we can use vectorization; but we choose a value less than m so we won't end up using batch gradient descent.**
4. While using mini-batch gradient descent with a batch size larger than 1 but less than m, the plot of the cost function 𝐽 looks like this: [Fig1] You notice that the value of 𝐽 is not always decreasing. Which of the following is the most likely reason for that?
    - In mini-batch gradient descent we calculate J(\hat{y}^{\lbrace t \rbrace}, y^{\lbrace t \rbrace})  thus with each batch we compute over a new set of data.
**Since at each iteration we work with a different set of data or batch the loss function doesn't have to be decreasing at each iteration.**
5. Suppose the temperature in Casablanca over the first two days of March are the following:
March 1st: 𝜃1=30∘C
March 2nd: 𝜃2=15∘C
Say you use an exponentially weighted average with 𝛽=0.5 to track the temperature: 𝑣0=0, 𝑣𝑡=𝛽𝑣𝑡−1+(1−𝛽)𝜃𝑡. If 𝑣2 is the value computed after day 2 without bias correction, and 𝑣2corrected is the value you compute with bias correction. What are these values?
    - v2 = 15, v2 corrected = 20
**v2 =βv t−1 +(1−β)θ t  thus 𝑣1=15, 𝑣2=15. Using the bias correction 𝑣𝑡 / (1 - 𝛽𝑡) we get 15 / (1−(0.5)^2) =20.**
6. Which of these is NOT a good learning rate decay scheme? Here, 𝑡 is the epoch number.
    - alpha = 1.01^t alpha_0
**This is not a good learning rate decay since it is an increasing function of 𝑡.**
7. You use an exponentially weighted average on the London temperature dataset. You use the following to track the temperature: 𝑣𝑡=𝛽𝑣𝑡−1+(1−𝛽)𝜃𝑡. The red line below was computed using 𝛽=0.9. What would happen to your red curve as you vary 𝛽? (Check the two that apply) [Fig2]
    - Increasing 𝛽 will shift the red line sligthly to the right
**Remember that the red line corresponds to β=0.9. In the lecture we had a green line β=0.98 that is slightly shifted to the right.**
    - Decreasing 𝛽 will create more oscillation within the red line
**Remember that the red line corresponds to β=0.9. In lecture we had a yellow line β=0.98 that had a lot of oscillations.**
8. Which of the following are true about gradient descent with momentum?
    - Gradient descent with momentum makes use of moving averages
**Gradient descent with momentum makes use of moving averages, which smooths out the gradient descent process.**
    - Increasing the hyperparameter β smooths out the process of gradient descent.
**Gradient descent with momentum makes use of moving averages, which smooths out the gradient descent process.**
    - It generates faster learning by reducing the oscillation of the gradient descent process.
**The use of momentum makes each step of the gradient descent more efficient by reducing oscillations.**
9. Suppose batch gradient descent in a deep network is taking excessively long to find a value of the parameters that achieves a small value for the cost function 𝐽(𝑊[1],𝑏[1],...,𝑊[𝐿],𝑏[𝐿]). Which of the following techniques could help find parameter values that attain a small value for 𝐽? (Check all that apply)
    - Try using gradient descent with momentum.
**The use of momentum can improve the speed of the training. Although other methods might give better results, such as Adam.**
    - Try better random initialization for the weights.
**As seen in previous lectures this can help the gradient descent process to prevent vanishing gradients.**
    - Normalize the input data
**In some cases, if the scale of the features is very different, normalizing the input data will speed up the training process.**
10. Which of the following are true about Adam?
    - Adam combines the advantages of RMSProp and momentum.
**Precisely Adam combines the features of RMSProp and momentum that is why we use two-parameter 𝛽1 and 𝛽2, besides 𝜖.**
