#book 
# Assumptions
1. $y | x; \theta$ ~ Exponential$(\eta)$
2. $h(x) = E[y|x]$
3. $\eta=\theta^Tx$

# Examples
Here we show how the two models discussed earlier, linear and logistic, can be derived from the GLM class.
## [[Linear regression|Ordinary least squares (OLS)]]
The OLS method is a special case of the GLM family of models. Consider setting the target (response) variable $y$ as a Gaussian distribution, i.e., $y \sim N(\mu, \sigma^2)$.

From [[Gaussian distribution]], we know that $\mu=\eta$, therefore, $h_\theta(x) = E[y|x] = \eta = \theta^Tx$

## [[Maximum likelihood model|Logistic regression]]
Consider setting the target variable $y$ as a Bernoulli distribution, i.e., $y \sim Bernoulli(\phi)$.

From [[Bernoulli distribution]], we know that $\phi = {1}/{1+e^{-\eta}}$, therefore, $h_\theta(x) = E[y|x] = \phi = ({1}/{1+e^{-\theta^Tx}})$


Therefore, from the above discussion, it is clear that any model where the target variable has a distribution of the [[Exponential family|exponential family]], the GLM approach gives us the hypothesis function directly as $h_\theta(x)=E[y|x;\theta]$. 

By extending the same to likelihood and maximizing, 

$$
\max_\theta \log P(y^{(i)}; \theta^T x^{(i)})
$$

we get the stochastic gradient algorithm as: 

$$
\theta^{(t+1)} = \theta^t+\alpha(y^{(i)}-h_{\theta^{t}}(x^{(i)}))x^{(i)}
$$

