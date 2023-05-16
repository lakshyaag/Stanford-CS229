#definition 
The **geometric margin** of $(w,b)$ is defined as:

$$
\gamma = y^{(i)}((\frac{w}{||w||})^Tx^{(i)}+\frac{b}{||w||})
$$

Of course, if $||w|| = 1$, then the [[Functional margins|functional margin]] is equivalent to the geometric margin. Moreover, the geometric margin does not depend on the scale of $(w,b)$.

For a training set $S$, the geometric margin of $(w,b)$ is defined as the minimum of geometric margins of the individual training examples,

$$
\gamma = \min_{i=1\dots n} \gamma^{(i)}
$$
