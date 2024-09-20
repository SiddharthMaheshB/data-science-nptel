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
