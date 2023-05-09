#book 
There is another method that can be used to maximize $l(\theta)$, called the Newton's method. 

Given a function $f$, if we wish to find a value $\theta$ such that $f(\theta) = 0$, Newton's method states that:
$$
\theta := \theta - \frac{f(\theta)}{f'(\theta)}
$$

Letting $f(\theta) = l'(\theta)$ (since we want to maximize $l(\theta)$ using $l(\theta) = 0$), we get:
$$
\theta := \theta - \frac{l'(\theta)}{l''(\theta)}
$$
Generalizing to a vector environment,
$$
\theta := \theta - H^{-1}\nabla_\theta l(\theta)
$$

where $H^{-1}$ is the [[Hessian matrix]] of dimensions $d+1 \times d+1$. 

## Benefits
Newton's method (or Newton-Raphson method) converges faster than batch gradient descent, provided the Hessian matrix is not too expensive to invert. When applied to maximizing the log-likelihood function $l(\theta)$, it is called Fisher scoring.


