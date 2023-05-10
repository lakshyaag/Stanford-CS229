#book #lecture 
# Introduction
A class of probability distribution is said to belong to the exponential family, if it can be written in the form:

$$
p(y; \eta) = b(y)\exp(\eta^TT(y)-a(\eta))
$$

where, 
- $\eta$ is the **natural parameter** of the distribution
- $T(y)$ is the **sufficient statistic**
- $a(\eta)$ is the **log partition function**. 

The term $e^{-a(\eta)}$ normalizes the distribution and ensures that the probability density function integrates to 1.

A fixed choice of $T$, $a$, and $b$, defines a family of distributions parameterized by $\eta$. By varying $\eta$, we get different distributions in the defined family.

# Examples
## [[Bernoulli distribution]]
A Bernoulli distribution with a mean of $\phi$ is in the exponential family for a particular set of $T$, $a$ and $b$.

## [[Gaussian distribution]]
A Gaussian distribution with a mean of $\mu$ and a variance of $\sigma^2$ is in the exponential family for a particular set of $T$, $a$ and $b$.

There are other distributions as well that are part of this family, such as Poisson, gamma, exponential, beta, multinomial, and others.

![[Pasted image 20230510215427.png]]

# Properties
1. The maximum likelihood estimation with respect to $\eta$ is a concave function, meaning that it  has only one maximum, which is the global maximum
2. $E[y;\eta]=\frac{\partial}{\partial \eta}a(\eta)$
3. $Var[y;\eta]=\frac{\partial^2}{\partial \eta^2}a(\eta)$

