#solution 
# Linear Classifiers
## Problem A

$$
\begin{align}
J(\theta) = &= -\frac{1}{m}\sum_{i=1}^{n} y^{(i)}\log h_\theta(x^{(i)}) + (1-y^{(i)})\log(1-h_\theta(x^{(i)})) \\
J'(\theta) &= -\frac{1}{m}\sum_{i=1}^{n}(y^{(i)} - h_\theta(x^{(i)}))x_j^{(i)} \\
J''(\theta) &= \frac{1}{m}\sum_{j=1}^{n}\sum_{k=1}^{n}g'(\theta^Tx)x_j x_k \\ 
\\
H &= \frac{1}{m}g(\theta^Tx)(1-g(\theta^Tx))x_j x_k \\
H &= \frac{1}{m}[X^T.g(X\theta).(1-g(X\theta))]X
\end{align}
$$

$$
\begin{align}
z^THz&=\sum_{i=1}^m\sum_{j=1}^m\sum_{k=1}^m g(\theta^Tx^{(i)})[1-g(\theta^Tx^{(i)})]x_j^{(i)} x_k^{(i)} z_j z_k \\
&= \sum_{i=1}^m\sum_{j=1}^m\sum_{k=1}^m g(\theta^Tx^{(i)})[1-g(\theta^Tx^{(i)})][{x^{(i)}}^Tz]^2 \geq0
\end{align}
$$

## Problem B
Refer to file `p01b_logreg.py`

## Problem C
**To understand**

## Problem D
Derivations here: [8 – Gaussian Discriminant Analysis – Beginning with ML (wordpress.com)](https://beginningwithml.wordpress.com/2018/09/18/7-gaussian-discriminant-analysis/).

## Problem E
Refer to file `p01e_gda.py`


