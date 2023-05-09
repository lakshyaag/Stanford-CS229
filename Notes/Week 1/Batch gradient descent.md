#definition 
# Algorithm
Repeat until convergence {

$$\theta_j = \theta_j + \alpha\sum_{i=1}^{n}(y^{(i)}-h(x^{(i)}))x_j^{(i)}$$

}

By grouping the updates for each $j$, we can re-write the above as: $$\theta = \theta + \alpha\sum_{i=1}^{n}(y^{(i)}-h(x^{(i)}))x^{(i)}$$

Here, the method looks at the entire training set on every step before updating $\theta$. Batch gradient descent moves the function directly towards its minima.