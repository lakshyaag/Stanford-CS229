#book 
Given a training set, define matrix $X$ to be the design or feature matrix, containing $n$ input vector as rows, 

$$X = \begin{bmatrix} (x^{(1)})^T 
\\ 
(x^{(2)})^T 
\\ 
\vdots
\\
(x^{(n)})^T 
\end{bmatrix}$$ 

and a target vector $\vec y$, 

$$\vec y = \begin{bmatrix} 
y^{(1)} \\ 
y^{(2)} \\ 
\vdots \\ 
y^{(n)}
\end{bmatrix}$$

Since $h(x) = x^T\theta$,

$$
\begin{align} X\theta - \vec y &= \begin{bmatrix} (x^{(1)})^T\theta \\ 
(x^{(2)})^T\theta \\ 
\vdots \\ (x^{(n)})^T\theta 
\end{bmatrix} - \begin{bmatrix} y^{(1)} \\ 
y^{(2)} \\ 
\vdots \\ 
y^{(n)}
\end{bmatrix}
\\
&= \begin{bmatrix} h(x^{(1)}) - y^{(1)} \\ 
h(x^{(2)}) - y^{(2)} \\ 
\vdots \\ 
h(x^{(n)}) - y^{(n)} 
\end{bmatrix} \end{align}
$$
Then, using the vector property $z^Tz = \sum_{i}z_i^2$,
$$\frac{1}{2}(X\theta-\vec y)^T(X\theta-\vec y) = \frac{1}{2}\sum_{i=1}^n (h(x^{(i)}) - y^{(i)})^2 = J(\theta)$$

Then, to minimize $J$, we can find its [[Matrix derivatives|derivatives]] w.r.t to $\theta$. Hence, 
$$\nabla_\theta J(\theta)=X^TX\theta - X^T\vec y$$
Setting this derivative to 0 (to find the minima), we get the value of $\theta$ that minimizes $J$, 

$$\begin{align}
X^TX\theta &= X^T\vec y
\\
\theta &= (X^TX)^{-1}X^T\vec y
\end{align}
$$
