\#book 
Assuming $\sigma^2=1$ for convenience, the Gaussian distribution can be written as:

$$
\begin{align}
p(y;\mu) &= \frac{1}{\sqrt{2\pi}}\exp(-\frac{1}{2}(y-\mu)^2) \\
&= \frac{1}{\sqrt{2\pi}}\exp(-\frac{1}{2}y^2).\exp(\mu y -\frac{1}{2}\mu^2)
\end{align}
$$

Here,
- $\eta=\mu$
- $T(y)=y$
- $a(\eta) = \frac{\eta^2}{2}$
- $b(y)=\frac{1}{\sqrt{2\pi}} \exp(-\frac{y^2}{2})$

Therefore, using the values above, the Gaussian distribution is indeed a part of the exponential family.
