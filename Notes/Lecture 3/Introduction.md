#book 
# Classification
In a classification problem, instead of predicting a continuous value (such as the price of a house), a function is trained to predict one of two or more classes. 

A binary classification problem is one where $y$ can take on values of either 0 (negative class) or 1 (positive class).

# Logistic regression
For this type of regression, where we know that $y \in [0,1]$, it does not make sense to keep using the linear regression function. Here, we define a new hypothesis function $h_\theta(x)$,

$$
\begin{align}
h_\theta(x) = g(\theta^Tx)&=\frac{1}{1+e^{(-\theta^Tx)}} \\
g(z) &= \frac{1}{1+e^{-z}}
\end{align}
$$

In the above definition, $g(z)$ is called the **[[sigmoid function]]**.


