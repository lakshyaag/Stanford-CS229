#book 
# Assumptions
$$
\begin{align}
p(y=1|x;\theta) &= h_\theta(x) \\
p(y=0|x;\theta) &= 1-h_\theta(x)
\end{align}
$$

Or, more compactly,
$$
p(y|x;\theta) = (h_\theta(x))^y(1-h_\theta(x))^{1-y}
$$

# Model
Assuming $n$ training items, the likelihood model becomes:
$$
\begin{align}
L(\theta) &= p(\vec y|X; \theta) \\
&= \prod_{i=i}^n p(y^{(i)} | x^{(i)};\theta) \\
&= \prod_{i=i}^n (h_\theta(x^{(i)}))^{y^{(i)}}(1-h_\theta(x^{(i)}))^{1-{y^{(i)}}} \\
\end{align}
$$

Taking the log of this function for ease of calculation,
$$
l(\theta) = \log L(\theta) = \sum_{i=1}^{n} y^{(i)}\log h_\theta(x^{(i)}) + (1-y^{(i)})\log(1-h_\theta(x^{(i)}))
$$

# Gradient ascent
Using the same principle as [[Stochastic gradient descent|stochastic gradient descent]] but for maximization, we can define the update rule as:
$$
\theta := \theta + \alpha \nabla_\theta l(\theta)
$$
The derivative of the log-likelihood function (using [[sigmoid function#Derivative|the sigmoid derivative]]), calculated for just one training example gives
$$
\frac{\partial}{\partial \theta_j} l(\theta)=(y-h_\theta(x))x_j
$$

The stochastic gradient ascent rule then becomes:
$$
\theta_j := \theta_j + \alpha (y^{(i)}-h_\theta(x^{(i)}))x^{(i)}_j
$$

which is of a similar form to the [[Linear regression#LMS algorithm|LMS algorithm]] described in linear regression, except the fact that $h(x)$ is a non-linear function now.

With the gradient ascent rule, the value of $\theta$ that maximizes $L(\theta)$ can be computed.

