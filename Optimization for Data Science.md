An optimization problem consists of maximizing or minimizing a real function by systematically choosing input values from within an allowed set and computing the value of the function
It is the use of specific methods to determine the "best" solution to a problem (finding best functional representation fort data, finding best hyperplane to classify data)

### Components of an optimization problem
- **Objective Function**: Function to find min/max value of
- **Decision Variables**: variables that are the main thingy of the function (x in f(x))
- **Constraints**: constraints to which decision variables are bound

### Types of optimization problems
optimization problems are categorized based on type of objective function, constraints, and decision variables
- **Linear Programming Problem**: problem of maximizing or minimizing a linear function
- **Non-Linear Programming Problem**: problem of maximizing or minimizing a non-linear function
- **Integer programming problem (linear and non linear)**: where the decision variables are constrained to integers
- **mixed integer programming problem**: where some of the decision variables are constrained to integers

### Nonlinear univariate optimization
![[Pasted image 20240919235244.png]]
**Conditions for $x*$ to be minimum value of f(x)**:
- $f'(x*)=0$ 
- $f''(x*)>0$ 

### Nonlinear multivariate optimization
![[Pasted image 20240920004247.png]] 
**Conditions for multivariate optimization**:
- $\nabla f=0$ (gradient matrix) and $\nabla ^2 f>0$ (Hessian matrix) is positive definite
- ![[Pasted image 20240920094215.png]]
- a matrix is said to be positive definite if all the eigen values of the matrix are positive
![[Pasted image 20240920095032.png]]

<hr>
### Unconstrained multivariate optimization - Directional Search
This section focuses on searching for minimal point, as sometimes we might want to climb to higher points to be able to find a lower point
- Find steepest direction at given point ($S^K$), then find how far to move in that direction (governed by learning rate $\alpha$), go to the next point and then find new steepest descent direction.
- at a local minimum point, we have no option other than to climb

This is called the **learning rule** in ML techniques.
In Neural Networks we use,
- Back-propogation algorithm
- Gradient descent with chain rule

The formula for **Gradient Descent** is given by: $$X^{K+1} = X^K -\alpha S^K$$
where:
	$X^{K}$ -> current point
	$\alpha$ -> step length (learning rate)
	$S^K$ -> steepest descent direction

### Multivariate Optimization with equality constraints
Sometimes we may have to find the optimal minimum that also satisfies a relation between the decision variables. In these cases we have equality constraints where $h_i(x)=0$ with $h_i(x)$ being the constraints applied

At optimum; $$-\nabla f(x^*) = \sum_{i=1}^l[ \nabla h_i(x^*)]\lambda_i$$
where $f(x)$ is the objective function,
	$h_i(x)$ is the ith equality constraint applied
	$\lambda_i$ is a constant
	$l$ is number of constraints
ie, the equation will be of the form $-\nabla f(x^*) = \lambda_1 \nabla h_1(x^*) + \lambda_2 \nabla h_2(x^*)+...$

### Multivariate Optimization with inequality constraints
Sometimes we may have to find the optimal minimum on one side of a classifying hyperplane. In these cases we have inequality constraints where $h(x)>0$ or $h(x)<0$
At optimum; $$-\nabla f(x^*) = \sum_{i=1}^l[ \nabla h_i(x^*)]\lambda_i^* + \sum_{j=1}^m[ \nabla g_i(x^*)]\mu_j^*$$
where $g_i(x)$ is the ith inequality constraint applied
	$\mu_i$ is a constant

Along with the above condition, the optimum must satisfy the KKT (Karush Kuhn Tucker) conditions
![[Pasted image 20240920125555.png]]
