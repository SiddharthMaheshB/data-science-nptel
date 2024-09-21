Linear regression is used to build a model (functional relationship) between a dependent variables(s) and an independent variable(s)
- dependent variables are also called response variables, regressand, predicted variable, output variable, and are denoted with **y**
- independent variables are also called Predictor variables, Regressor, Exploratory variable, input variable, and are denoted with **x**

### Types of Regression
- Univariate vs Multivariate:
	**Univariate**: One dependent and one independent variable
	**Multivariate**: Multiple dependent and Multiple independent variables
- Linear vs Nonlinear: relationship between x and y is linear/nonlinear
- Simple vs Multiple:
	**Simple**: One dependent and one independent variable (SISO)
	**Multiple**: One dependent and many independent variable (MISO)

### Regression analysis
Regression analysis is used to answer the following questions:
- Is there a relationship between these variables?
- Is the relationship linear and how strong is the relationship?
- How accurately can we estimate the relationship?
- How good is the model for prediction purposes?

### Regression Methods
**Linear Regression methods**:
- simple linear regression
- multiple linear regression
- ridge regression
- Principal Component regression
- Lasso
- Partial Least Squares

**Nonlinear Regression methods**:
- Polynomial Regression
- Spline Regression
- Neural networks

### Regression process
![[Pasted image 20240920180705.png]]

### Ordinary Least Squares (OLS)
- OLS method is used to build regression models
- Linear model between $y$ and $x_i, i=1,...,n$ is given by: $$y_i = \beta _0 + \beta _1 x_i + \epsilon_i$$
	where $\epsilon_i$ depicts the error
- The Sum of Squares of Errors (SSE) is given by: $$\sum_i \epsilon_i^2 = \sum(y_i - \beta_0 - \beta_1x_i$$
- the minimization of SSE gives estimates of $\beta_0$ and $\beta_1$: $$\beta_1 = \frac{\sum_{i=1}^n (x_i - \bar x)(y_i - \bar y)}{\sum_{i=1}^n (x_i - \bar x)} = \frac {S_{xy}}{S_{xx}}$$

### Testing the OLS method
- Prediction is done by using the regression equation: $y_i = \beta _0 + \beta _1 x_i$ 
- Coefficient of determination - $R^2$ is measure of variability in output variable given by: ![[Pasted image 20240920182438.png]]
- Values of $R^2$ closer to 0 indicate poor fit and closer to 1 indicate good fit

### Multiple Linear Regression
- General form: $y = \beta_0 + \beta_1x_1 + \beta_2x_2+ \beta_3x_3+... + \epsilon$
- Objective: using $n$ observations, estimate regression coefficients
- This is done by minimizing the SSE (Sum of Squares of Errors)
![[Pasted image 20240920233016.png]]
