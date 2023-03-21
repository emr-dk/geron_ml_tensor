### Overfitting
When your model performs well on the training data, but does not generalize well. For instance by having too many parameters in play.

This can be mitigated by _regularization_ (constraining). The amount of _regularization_ is controlled by a **hyperparameter**. 
It can also be done by simplifying the model or getting more data. 

### Underfitting
This occurs when the model is too simple to learn the structure of the data. If for instance you are trying to fit a linear model to a subject / phenomenon that is non-linear.

Either the features do not provide enough information to make good predictions, or the model is not powerful enough.

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

### Normalising data
Outliers can have a large effect on the values the are output when performing standardization. Additionally, heavy tailed data should be transformed to a more symmetrical distribution (for instance by taking the ln of a power law dsitribution).
Bucketizing data can also be a way of standardising it. This is also a good way of handling multimodal distributions.

min-max scaling: Each attributes values are shifted and rescaled so they range from 0 to 1. This is done by subtracing the min value and dividing by max - min. 

standardisation: Values have the mean subtracted (i.e. zero mean) then divide the result by the standard deviation (i.e. standard deviation of 1)

### Shuffling the training set
Some times it is relevant to shuffle the training set. This is important as it ensures that all cross-validation folds will be similar. Some ML algorithms are also sensitive to the order of the training instances and perform poorly if there are many similar ones in a row. 

### Precision and recall
$$
\text{precision} = \frac{TP}{TP+FP}
$$

$$
\text{recall} = \frac{TP}{TP+FN}
$$

Increasing recall reduces precision and vice-versa. The precision/recall trade-off.
