Data is stored and represented using Matrices

### Identification of Independent Variables:
- **Rank** of a matrix refers to the number of linearly independent rows or columns of the matrix
- Rank of a matrix can be found using the command `rank(matrix)`

### Null Space:
- null space of a matrix consists of all vectors $\beta$ such that $A\beta=0$ and $\beta\ne 0$
- Nullity of a matrix is the number of vectors in the null space, also denotes number of linear relations among the attributes

### Rank Nullity theorem:
- Rank of a matrix + Nullity of a matrix = Total number of variables in the matrix

### Solving Linear Equations:
- Let $m$ denote the number of linearly independent eqns (rank)
- Let n denote the number of variables (cols)
- if:
	$m=n$ -> Single solution
	$m>n$ -> no solution
	$m<n$ -> multiple solutions
- we need to generalise a solution for all the above three cases
- for a solution x such that $Ax-B=0$, the most accurate solution for x with minimal least square error is given by $$x = (A^TA)^{-1}A^TB$$
For Example:
![[Pasted image 20240918201317.png]]
![[Pasted image 20240918201341.png]]


### Generalization of solutions of linear equations:
Pseudo Inverse can be used to solve matrix equations as so: $$Ax = B$$ $$x=A^+B$$
- Singular Value Decomposition can be used to calculate the pseudo inverse $A^+$.

### Projection of a vector on a plane:
let $v_1$ and $v_2$ be two vectors representing a plane, and $X$ be a vector
The projection of $X$ on the plane is: $$\frac{X^T v_1}{V_1 v_2} v_1 + \frac{X^T v_2}{v_1 v_2}v_2$$ 
Projection of a vector X on a space V is given by $$V(V^TV)^{-1}V^TX$$

### Hyperplanes
- a hyperplane is an entity whose dimension is one less than the space surrounding it
- planes are hyperplanes in a 3D space
- a hyperplane is written as $X^Tn+b=0$

### Half spaces
- a half space is one side of a space that is divided by a hyperplane
- half spaces are used for classification problems
- for a half space defined by $X^Tn + b = 0$, 
	if $X^Tn+b>0$ for a vector $X$, $X$ is part of the subspace in the $n$ direction
	if $X^Tn+b<0$ for a vector $X$, $X$ is part of the subspace in the $-n$ direction
- ![[Pasted image 20240919115058.png]]

### Eigenvalues and eigenvectors
- An Eigenvector is a vector whose direction is unchanged when a transformation is applied on it
- Eigenvalues of a matrix A are given by the solution for $\lambda$ in the equation $|A-\lambda I| = 0$ 
- the eigenvectors for given eigenvalues of a matrix can be found by the equation $AX = \lambda X$
![[Pasted image 20240919121434.png]]
