#definition 
# Function

$$
f(x) = \frac{1}{1+e^{-x}}
$$

# Plot
![[Pasted image 20230509205757.png]]

The function $f(x) \rightarrow 1$ as $x \rightarrow \infty$, while $f(x) \rightarrow 0$ as $x \rightarrow -\infty$.

# Derivative
$$
\begin{align}
f'(x) &= \frac{1}{(1+e^{-x})^2}e^{-x} \\
&= \frac{1}{(1+e^{-x})}.(1-\frac{1}{1+e^{-x}}) \\
&= f(x).(1-f(x))
\end{align}
$$