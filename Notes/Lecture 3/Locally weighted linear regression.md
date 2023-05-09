#lecture #book 
# Underfit vs. overfit
Instead of fitting a linear function to the training set, we could go ahead and fit a quadratic function or any polynomial function. However, simply adding more features does not guarantee an improvement in accuracy, but rather leads to the problems of underfitting/overfitting.

Briefly, underfitting occurs when the model is unable to accurately fit even the known data points, while overfitting occurs when the model is so fine-tuned to the known data that it is unable to predict properly on unknown data.

# Non-parametric learning algorithm
Locally weighted linear regression (LWR) is a "non-parametric" algorithm, wherein the data/parameters keeps growing with the training data.

>The term “non-parametric” (roughly) refers to the fact that the amount of stuff we need to keep in order to represent the hypothesis $h$ grows linearly with the size of the training set.

## Steps
In LWR, we use a modified cost function:

$$
min \sum_{i=1}^{n}w^{(i)}(y^{(i)}-\theta^Tx^{(i)})^2
$$

where $w$ is a vector of **"weights"**, generally given by:

$$
w^{(i)}=exp(-\frac{(x^{(i)}-x)^2}{2\tau^2})
$$

It can be seen that if $|x^{(i)}-x|$ is small, then $w^{(i)}$ is close to 1, while if the difference is large, then the weight will be close to 0. Essentially, this allows the model to remove from the training set entries that are far away from the $x$ that is being predicted and only keep the ones near $x$.

The parameter $\tau$ controls the width (or **bandwidth**), which dictates how quickly the weight should fall off with distance from the prediction point $x$. In other words, $\tau$ controls the scope of search.