#definition 
# Definition
The Hessian matrix for a function is simply the matrix of its second-order partial derivatives.

# Formula
$$
\nabla_x^2f(x) = H = \begin{bmatrix}
\frac{\partial^2f(x)}{\partial x_1^2} & \frac{\partial^2f(x)}{\partial x_1x_2} & \dots & \frac{\partial^2f(x)}{\partial x_1x_n} \\
\frac{\partial^2f(x)}{\partial x_2x_1} & \frac{\partial^2f(x)}{\partial x_2^2} & \dots & \frac{\partial^2f(x)}{\partial x_2x_n} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial^2f(x)}{\partial x_nx_1} & \frac{\partial^2f(x)}{\partial x_nx_2} & \dots & \frac{\partial^2f(x)}{\partial x_n^2}
\end{bmatrix}
$$

The $(i,j)$ element is given by:
$$
H_{(i,j)} = \frac{\partial^2f(x)}{\partial x_i x_j}
$$

