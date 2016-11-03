<p>A <i>Q-learning</i> method based to select classifiers in multi-labels problems.  Action is a classifier to select in order to learn the politic $\pi$ selecting the action with best <i>Q-value</i>  with : $$Q(s_t, a_t) = Accuracy(s_{t +1} +\lambda \max_{a'} Q(s_{t+1}, a'))$$  </p>
<p>This methods can not scale up for a large number of labels since $ 2^{\#classifiers} $state is needed</p>
