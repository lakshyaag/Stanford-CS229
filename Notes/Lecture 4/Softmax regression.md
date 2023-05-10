#lecture #book 
# Introduction
This form of regression (also called **cross-entropy minimization**) is used for multi-class classification, i.e., classification problems where there are $k$ number of classes.

Since there $k$ number of classes, we model the output using a multinomial distribution with parameters $\phi_1, \phi_2, \dots, \phi_k$, such that $\sum_{i=1}^{k}\phi_i = 1$. Therefore, we have to find out a set of parameters for each class $k$.

We can not use $\theta_1^Tx, \theta_2^Tx, \dots, \theta_k^Tx$ directly to represent our parameters because of two rules that are not necessarily followed:
1. $\theta_j^Tx$ must be between $[0,1]$
2. $\sum_{j=1}^k \theta_j^Tx = 1$

# Softmax function
The softmax function is defined as:

$$
softmax(t_1,\dots,t_k) = \begin{bmatrix}
\frac{\exp(t_1)}{\sum_{j=1}^{k}\exp(t_j)} \\
\vdots \\
\frac{\exp(t_k)}{\sum_{j=1}^{k}\exp(t_j)}
\end{bmatrix}
$$

The inputs to the above function, the vector $t$ is called the logits. By definition, the output of the softmax function will sum to 1.

By setting $(t_1,\dots, t_k) = (\theta_1^Tx,\dots, \theta_k^Tx)$, we get the model:

$$
\begin{bmatrix}
P(y=1|x;\theta) \\
\vdots \\
P(y=k|x;\theta)
\end{bmatrix} = softmax(t_1,\dots, t_k) = 
\begin{bmatrix}
\frac{\exp(\theta_1^Tx)}{\sum_{j=1}^{k}\exp(\theta_j^Tx)} \\
\vdots \\
\frac{\exp(\theta_k^Tx)}{\sum_{j=1}^{k}\exp(\theta_j^Tx)}
\end{bmatrix}
$$

Succinctly, letting $\phi_i = \frac{\exp(\theta_i^Tx)}{\sum_{j=1}^{k}\exp(\theta_j^Tx)}$, 

$$
P(y=i|x; \theta) = \phi_i
$$

# Optimization
Solving for the negative log-likelihood for a single example,

$$
l(\theta) = \sum_{i=1}^{n}- \log(\frac{exp(\theta_{y^{(i)}}^Tx^{(i)})}{\sum_{j=1}^{k}exp(\theta_{j}^T x^{(i)})})
$$

We can define the [[cross-entropy]] loss $l_{ce}$ as:

$$
l_{ce}((t_1,\dots,t_k), y) = - \log(\frac{exp(t_y)}{\sum_{j=1}^{k}exp(t_j)})
$$

Then, the log-likelihood becomes:

$$
l(\theta) = \sum_{i=1}^n l_{ce} ((\theta_1^Tx^{(i)},\dots, \theta_k^Tx^{(i)}), y^{(i)})
$$

Further, taking the derivative of $l(\theta)$ and implementing stochastic gradient descent, we can minimize the loss function.