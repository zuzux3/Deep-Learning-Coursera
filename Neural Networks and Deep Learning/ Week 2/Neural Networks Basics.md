1. In logistic regression given x and parameters w incl. R^n_x, b incl. R. Which of the following best expresses what we want y_hat to tell us?
   - P(y=1|x)
2. Which of these is the "Logistic Loss"?
   - L^i(yhat^i, y) = - (y^i log(yhat^i) + (1 - y^i)(log(1-yhat^i))
3. Suppose img is a (32,32,3) array, representing a 32x32 image with 3 color channels red, green and blue. How do you reshape this into a column vector 𝑥?
   - x = img.reshape((32*32*3, 1))
4. Consider the following random arrays 𝑎 and 𝑏, and 𝑐:
   a = np.random.randn(3, 4) #a.shape = (3, 4)
   b = np.random.randn(1, 4) #b.shape = (1, 4)
   c = a + b
   - c.shape = (3, 4)
5. Consider the two following random arrays 𝑎 and 𝑏:
   a = np.random.randn(1, 3) #a.shape = (1, 3)
   b = np.random.randn(3, 3) #b.shape = (3, 3)
   c = a * b
   - c.shape = (3, 3)
6. Suppose you have 𝑛_𝑥 input features per example. Recall that 𝑋=[𝑥^(1)𝑥^(2)...𝑥^(𝑚)]. What is the dimension of X? 
   - (n_x, m)
7. Recall that 𝑛𝑝.𝑑𝑜𝑡(𝑎,𝑏) performs a matrix multiplication on 𝑎 and 𝑏, whereas 𝑎∗𝑏 performs an element-wise multiplication.Consider the two following random arrays 𝑎 and 𝑏:
   a = np.random.randn(12288, 150) #shape = 12288, 150
   b = np.random.randn(150, 45) #shape = 150, 45
   c = np.dot(a, b)
   - c.shape = 12288, 45
8. Consider the following code snippet:
   a.shape = (3, 4)
   b.shape = (4, 1)
   for i in range(3):
     for j in range(4):
       c[i][j] = a[i][j]*b[j]

   How do you vectorize this?
    - c = a * b.T
9. Consider the following code:
    a = np.random.randn(3, 3)
    b = np.random.randn(3, 1)
    c = a * b
   What will be 𝑐? (If you’re not sure, feel free to run this in python to find out).
    - This will invoke broadcasting, so b is copied three times to become (3, 3), and * is an element-wise product so c.shape will be (3, 3)
10. Consider the following computational graph.
![Image](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/74f440e3-3f74-4936-ba94-fdde83e116ebimage3.png?expiry=1715644800000&hmac=Us8aFQO9-p8DiWlzVPWWMVsLhvfPBomhXvvvzONsw9A)
    - (a + c)(b - 1)
