#lecture
# Hypothesis
A hypothesis (prediction function) is defined as a function $h: X \rightarrow y$, where $X$ could any collection of text, numbers, and/or images, and $y$ can be a discrete or continuous variable.
# Training set
A training set is defined as a set of pairs $\{(x^{(1)}, y^{(1)}), ..., (x^{(n)}, y^{(n)})\}$ such that $x^{(i)} \in X$ and $y^{(i)} \in y$ for $i = 1,...,n$

Here, if $y$ is continuous, it is a regression problem, otherwise it's a classification problem.
# Example: Housing price
If we let $X$ be a vector of features such as *size*, *# of bedrooms*, *lot size*, and so on, up to $d$ such features and $y$ be the house price, then one way of defining a prediction function $h$ is: $$h = \sum_{j=0}^{d}\theta_jx_j$$
Here, $\theta$ is called a parameter, $x$ is called the input or feature, and $y$ is the output or target (given by $h$). This is an example of an [[affine function]].