#definition 
Given a training example $(x^{(i)},y^{(i)})$, the **functional margin** of $(w,b)$ is defined as:

$$
\hat\gamma^{(i)} = y^{(i)}(w^Tx^{(i)}+b)
$$

Here, if $y=1$, then for $\hat\gamma$ to be large, $w^Tx+b$ needs to be large (similarly for $y=-1$). However, for a linear classifier, the functional margin is not a good measure of confidence since $(w,b)$ can be scaled arbitrarily to inflate the value of $h_{w,b}(x)$.

For a training set $S$, the functional margin of $(w,b)$ is defined as the minimum of functional margins of the individual training examples,

$$
\hat\gamma = \min_{i=1\dots n} \hat\gamma^{(i)}
$$