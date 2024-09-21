Algorithms that classify data into categories
- Binary classification problems (only 2 classes, yes/no)
- Multi-class classification problems (multiple classes)
- Linearly separable problems (data can be divided by a hyper plane into two classes)
- Non-Linearly separable problems (data cannot be divided by a hyper plane into two classes)

### Logistic Regression
- Classification technique where the decision boundary is generally linear, derived from probability

### Linear Classifier for logistic regression:
- Decision function is linear
- Binary classification is done by hyper planes and half spaces
- Instead of classifying things into yes/no, we can use the probability of a yes or no to give a more accurate result. 
- probability of the data belonging to class is given by $p(x) = \beta_0 + \beta_1 x$ 
- but this function may give nonsensical results making it difficult to interpret
- we solve it by making log(p(x)) a linear function of x: $log(p(x)) = \beta_0 + \beta_1 x$, which is bounded only on one side

### Sigmoid function
- usage of a sigmoid function makes sure that p(x) is bounded by 1 and 0
- $$p(x) = \frac{e^{(\beta_0 + \beta_1 x)}}{1 + e ^{(\beta_0 + \beta_1 x)}}$$
- The parameters $\beta_0$ and $\beta_1$ are found by maximizing the likelihood function: $$L(\beta_0, ]beta_1) = \prod_{i=1}^n (p(x_i))^{y_i}(1-p(x_i))^{(1-y_i)}$$

### Regularization
Regularization is used to reduce overfitting in logical regression 
Regularization works by penalizing a coefficient that is identified to not really contribute to the solution
It avoids capturing noise in model due to overfitting