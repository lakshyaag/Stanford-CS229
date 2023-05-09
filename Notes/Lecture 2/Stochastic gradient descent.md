#definition 
# Algorithm
Loop {
	for $i=1$ to $n$ 
	{
		$$
	\theta_j = \theta_j + \alpha(y^{(i)}-h(x^{(i)}))x_j^{(i)}\
	$$
	}
}

By grouping the updates for each $j$, we can re-write the above as: $$\theta = \theta + \alpha(y^{(i)}-h(x^{(i)}))x^{(i)}$$

Here, the method runs through each training example and updates the parameters according to the error of that single example only. As a result, the optimization is way faster than batch gradient descent since steps are taken for each training example, rather than waiting for the training data to get exhausted.