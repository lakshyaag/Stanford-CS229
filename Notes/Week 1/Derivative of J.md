$$\begin{align}
\frac{\partial}{\partial\theta_j}J(\theta) & =\frac{\partial}{\partial\theta_j}\frac{1}{2}(h(x)-y)^2 
\\ 
& = 2.\frac{1}{2}(h(x)-y).\frac{\partial}{\partial\theta_j}(h(x)-y)
\\
& = (h(x)-y).\frac{\partial}{\partial\theta_j}(\sum_{i=0}^{d}\theta_ix_i-y)
\\
& = (h(x)-y).x_j
\end{align}
$$
