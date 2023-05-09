#solution
# Gradients and Hessians
## 1. Problem A
$$
\nabla f(x) = Ax + b
$$

## 2. Problem B
$$
\begin{align}
\nabla f(x) &= \nabla g(h(x)) \\
&= \frac{\partial g(h(x))}{\partial h(x)} \frac{\partial h(x)}{\partial x_i} \\
&=g'(h(x))\nabla_xh(x)
\end{align}
$$

## 3. Problem C
$$
\nabla^2f(x)=A
$$

## 4. Problem D
$$
\nabla f(x) = \frac{\partial g(a^Tx)}{\partial (a^Tx)} \frac{\partial (a^Tx)}{\partial x}=g'(a^Tx)a
$$

$$
\nabla^2f(x)=\frac{\partial g'(a^Tx)}{\partial (a^Tx)^2} \frac{\partial a^Tx}{\partial x_i} \frac{\partial a^Tx}{\partial x_j} = g''(a^Tx)a_ia_j=g''(a^Tx)aa^T
$$
# Positive definite matrices
## Problem A
$$
\begin{align*}
z &= \begin{bmatrix} 
z_1 \\
z_2 \\
\vdots \\
z_n
\end{bmatrix} \\
z^T &= \begin{bmatrix} 
z_1 &
z_2 &
\dots &
z_n
\end{bmatrix} \\
A &= zz^T=\begin{bmatrix} z_1^2 & z_1z_2 & \dots & z_1z_n \\
z_1z_2 & z_2^2 & \dots & z_2z_n \\
\vdots & \vdots & \ddots & \vdots \\
z_nz_1 & z_nz_2 & \dots & z_n^2 \\
\end{bmatrix}
\end{align*}
$$

$$
A_{i,j} = z_iz_j
$$

Now, 
$$
A^T = (zz^T)^T = (z^T)^Tz=zz^T
$$
$$
x^TAx = x^Tzz^Tx=x^Tz(x^Tz)^T=(x^Tz)^2\geq0
$$

## Problem B
$$
N(A) = \set{x \in \mathbb R^{n} : x^Tz = 0}
$$
$$
R(A) = R(zz^T) = 1
$$

## Problem C
Assuming $A = zz^T$,
$$
(BAB^T)^T=BA^TB^T = BAB^T
$$

$$
x^TBAB^Tx = x^TBA(x^TB)^T \geq 0
$$
Therefore, $BAB^T$ is PSD.

# Eigenvectors and eigenvalues
## Problem A
$$ 
\begin{align}
A = T\Lambda T^{-1} &= \begin {bmatrix} t^{(1)} & \dots & t^{(n)} \end{bmatrix} \Lambda T^{-1} \\
&= 
\begin {bmatrix} t^{(1)}\lambda_1 & \dots & t^{(n)}\lambda_n \end{bmatrix}
T^{-1}
\end{align}
$$
$$
 
\begin{align}
A &= T\Lambda T^{-1}  \\
AT &= T\Lambda \\
A \begin {bmatrix} t^{(1)} & t^{(2)} & \dots & t^{(n)} \end{bmatrix} &= \begin {bmatrix} t^{(1)} & t^{(2)} & \dots & t^{(n)} \end{bmatrix} \Lambda \\
\begin {bmatrix} At^{(1)} & At^{(2)} & \dots & At^{(n)} \end{bmatrix} &= \begin {bmatrix} t^{(1)}\lambda_1 & t^{(2)}\lambda_2 & \dots &  At^{(n)}\lambda_n \end{bmatrix} \\
At^{(i)} &= \lambda_it^{(i)}
\end{align}
$$

## Problem B
$$
\begin{align}
A &= U \Lambda U^T \\
AU &= U \Lambda U^TU \\
AU &= U \Lambda I \\
AU &= U \Lambda \\
A \begin {bmatrix} u^{(1)} & u^{(2)} & \dots & u^{(n)} \end{bmatrix} &=  \begin {bmatrix} \lambda_1 u^{(1)} & \lambda_2 u^{(2)} & \dots & \lambda_n u^{(n)} \end{bmatrix} \\
Au^{(i)} &= \lambda_i u^{(i)}
\end{align}
$$

## Problem C
$$
\begin{align}
At^{(i)} &= \lambda_it^{(i)} \\
(t^{(i)})^TAt^{(i)} &= \lambda_i (t^{(i)})^Tt^{(i)} \\
&= \lambda_i \lvert\lvert t^{(i)}\rvert\rvert_2 \\
&= \lambda_i \geq 0
\end{align}
$$