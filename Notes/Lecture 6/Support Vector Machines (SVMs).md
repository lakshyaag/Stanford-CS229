#book #lecture 
# Margins
Intuitively thinking, a good goal for any model to have would be to have a high level of confidence in the prediction that the model makes. In other words, if the value of $p(y=1|x;\theta)$ is large, then the model is confident. 

Graphically, this can be thought of as the distance between a prediction and the decision boundary.
![[Pasted image 20230516203810.png]]

In the image above, point $A$ has higher confidence than point $C$, based on the distance from the line $\theta^Tx=0$.

The two kinds of margins are:
1. [[Functional margins]]
2. [[Geometric margins]]

# Optimal margin classifier
From the margin definition above, we can say that by maximizing the geometric margin, we can hope to achieve a high degree of confidence in the predictions (as the distance between the decision boundary and the prediction will be the highest). 

As an optimization problem then,

$$
\begin{equation}
\begin{aligned}
max_{\gamma,w,b} \quad \gamma \\
s.t. & \quad y^{(i)}(w^Tx^{(i)}+b) \geq \gamma, i = 1,\dots,n \\
& ||w|| = 1
\end{aligned}
\end{equation}
$$

By taking a few assumptions (namely $\hat\gamma=1$), the problem becomes:

$$
\begin{equation}
\begin{aligned}
max_{w,b} \quad \frac{1}{2}||w||^2 \\
s.t. & \quad y^{(i)}(w^Tx^{(i)}+b) \geq \gamma, i = 1,\dots,n \\
\end{aligned}
\end{equation}
$$

which can be solved using quadratic programming to give the **optimal margin classifier**.