#book 
The Bernoulli distribution can be written as:

$$
\begin{align}
p(y;\phi)&=\phi^y(1-\phi)^{(1-y)} \\
&=exp(y \log \phi + (1-y) \log(1-\phi)) \\
&=exp(y \log \phi + \log(1-\phi) - y\log(1-\phi)) \\
&=exp((\log (\frac{\phi}{1-\phi})y) + \log(1-\phi)) \\
\end{align}
$$

Here, 
- $\eta = \log {(\frac{\phi}{1-\phi})}$
- $T(y) = y$
- $a(\eta)= -\log(1-\phi)=\log(1+e^\eta)$
- $b(y)=1$

Therefore, using the values above, the Bernoulli distribution is indeed a part of the exponential family.