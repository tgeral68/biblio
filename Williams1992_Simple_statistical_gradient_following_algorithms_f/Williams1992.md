<h1>Learn a policy by gradient</h1>
<p>The papers describe the basis of policy gradient.  The authors present method aiming to learn a stochastic sampling by gradient descent, allowing to use policy jointly to a deep architectures.
</p>
<h4>Short description of the algorithm</h4>
<p>
Let consider $y_i \in \mathbb{Y}$ the ground truth, $x_i \in X$ the input representation vector, we want to learn an distribution $g_i$ depending on input $x^i$, learned weight $w^i$ and $\zeta$ the sampled hypothetic value. The probability $P(\zeta|w^i,x^i)$ is defined by (considering a bernouilli distribution):

$$
   g_i(\zeta, w^i, x^i) =
   \left\{
     \begin{array}{ll}
      1 - p_i &\text{ for } \zeta = 0 \\
      p_i &\text{ for } \zeta = 1
     \end{array}
   \right.
$$
With $p_i$ the bernouilli parameters associate, depending on weight and input.
Let define $\nabla w_{ij}$ the update of the matrix $W \in \mathbb{R}^{n \times m}$ such that :

$$
\nabla w_{ij} = \alpha_{ij}(r-b_{ij})\frac{\delta ln(g_i)}{\delta w_{ij}}
$$
With $\alpha_{ij}$ th learning rate, r the reinforce value and $b_{ij}$ the reinforcement baseline. </p>
