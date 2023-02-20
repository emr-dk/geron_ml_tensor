### Overfitting
When your model performs well on the training data, but does not generalize well. For instance by having too many parameters in play.

This can be mitigated by _regularization_. The amount of _regularization_ is controlled by a **hyperparameter**

### Underfitting
This occurs when the model is too simple to learn the structure of the data. If for instance you are trying to fit a linear model to a subject / phenomenon that is non-linear.

### Hyperparameter
A parameter of the learning algorithm, not of the model. 

### Holdout validation
Hold out part of the training set - validation set - to evaluate candidate models and select the best one.

The idea is to train multiple models with various hyperparameters on the reduced training set and then use the model that performs best on the validation set. 

Finally the model is trained on the validation + training set data which is the final model. 

### Pipelines
A series of connected processing components are called a pipeline. These usually work asynchronously.

### Performance measures
Root mean square error: 
$$\text{RMSE}({\bm{X},h}) = \sqrt{\frac{1}{m}\sum_{i=1}^m(h(\bm{x^{(i)}})-y^{(i)})}$$ 
This equates to the $L^2$ or $\ell_2$ norm or Euclidean distance

Mean absolute error:
$$\text{MAE}(\bm{X},h) = \frac{1}{m}\sum_{i=1}^{m}\lvert h(\bm{x}^{(i)}-y^{(i)})\rvert$$
This equates to the $L^1$ or $\ell_1$ norm or Manhattan distance

Higher levels of norms $L^k$ or $\ell_k$ :
$$\lVert \bm{v} \rVert _k = (\lvert v_1 \rvert ^k + \lvert v_1 \rvert ^k + \ldots + \lvert v_n \rvert ^k)^{\frac{1}{k}}$$
$\ell_0$ is the number of non-zero elements in the vector and $\ell_\infin$ is the maximum absolute value in the vector. 
The higher the norm index the more focus is on large values and less on small ones. This also means that higher norms are more sensitive to outliers, but when these are rare RMSE performs very well.

### Sampling strategies
Random sampling

Stratified sampling


### Usual notation
$$m = instances,\\
\bm{x} = vector, \\
\bm{X} = matrix, \\
h(x) = \text{prediction function / hypothesis}$$
