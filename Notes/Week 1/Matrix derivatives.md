#definition  
The derivative of a function $f(A)$ with respect to a $n x d$ matrix $A_{n \times d}$ is defined as:
$$
\nabla_Af(A) = \begin{bmatrix}

\frac {\partial f}{\partial A_{11}} & \dots &  \frac {\partial f}{\partial A_
{1d}} \\

\vdots & \ddots & \vdots \\

\frac {\partial f}{\partial A_{n1}} & \dots &  \frac {\partial f}{\partial A_{nd}} \\


\end{bmatrix}
$$
Also,
$$(i,j) = \frac {\partial f} {\partial A_{ij}}$$
The above shows the derivative matrix of a function that is applied to matrices. For example, given a function $f$, such that: $$f(A)=\frac{4}{3}A_{11} + 12A_{12}^2 + A_{21}A_{22}$$ Then, the derivative matrix is $$\nabla_Af(A) = \begin{bmatrix}\frac{4}{3} & 24A_{12} \\ A_{22} & A_{21}\end{bmatrix}$$
