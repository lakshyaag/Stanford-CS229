#book
# Dataset
The housing prices dataset is used as the example. 
# Linear model

Let our vector of features $X$ be 2-dimensional currently, with *living area (sqft.)* and *# of bedrooms* as the features. Then, a linear function of $y$ on $x$ would be: $$h(x) = \theta_0 + \theta_1x_1 + \theta_2x_2$$

with $\theta_i$ as a parameter or weight. If we assume that $x_0=1$, then the function can be simplified as: $$h(x)=\sum_{i=0}^{d}\theta_ix_i=\theta^Tx$$

Now that we've defined our linear approximation function, how do we ensure that $h(x)$ is as close to $y$ as possible?
# Cost function

One way of thinking about the above question is to formalize a cost function as the difference between $h(x)$ and $y$ for each value of the $\theta$'s for each training point $i$, $$J(\theta)=\frac{1}{2}\sum_{i=1}^{n}(h(x_i)-y)^2$$

The above function calculates the **mean squared error**, a common cost function (most popularly used in Ordinary Least Squares), with the objective of minimizing $J(\theta)$.
# LMS algorithm
Since our objective is to minimize $J(\theta)$, we will start with some initial value of $\theta$ and then repeatedly change it such that $J$ is as small as possible. 
## Gradient descent

Given an initial value of $\theta$, the gradient descent algorithm performs the update: $$\theta_j = \theta_j - \alpha\frac{\partial}{\partial\theta_j}J(\theta)$$

for all values of $j = 0,...,d$, and where $\alpha$ is defined as the learning rate. Assuming $n=1$ and [[Derivative of J|working the derivative]], the above update rule can be re-written as $$\theta_j = \theta_j + \alpha(y-h(x))x_j$$

This rule is also known as the **least mean squares update rule**, or the *Widrow-Hoff* learning rule.

> For instance, the magnitude of the update is proportional to the error term $(y (i) − h(x (i) ))$; thus, for instance, if we are encountering a training example on which our prediction nearly matches the actual value of $y (i)$ , then we find that there is little need to change the parameters; in contrast, a larger change to the parameters will be made if our prediction $h(x (i) )$ has a large error (i.e., if it is very far from $y (i)$ ).

Over $n$ training points, the above rule can be re-written in two ways:
1. [[Batch gradient descent]]
2. [[Stochastic gradient descent]]

In practice, most (if not all) applications use a minibatch version of the stochastic gradient descent as it is computationally more efficient. In the minibatch version, instead of taking a step for each training example, steps are taken for a random batch of training examples, thereby reducing variation.

# [[Least squares with matrices|Normal equation]]

This method works only for linear regression and allows us to directly jump to the global optimum, instead of going through an iterative process of gradient descent. Using the matrix method of ordinary least squares, we can quickly find the optimum value of $\theta$, using $$\theta = (X^TX)^{-1}X^T\vec y$$

This vector can be plugged into $h(x)$ to generate the linear approximation function. For in-depth, see [[Least squares with matrices]]