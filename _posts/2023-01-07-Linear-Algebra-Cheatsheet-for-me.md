---
title: Linear Algebra Cheatsheet for me
date: 2023-01-07
author: Chanhaeng Lee
layout: post
comments: true
category: Linear Algebra
---



# Linear Algebra Cheat Sheet for me.

I'd like to summarize important things that I often forget in linear algebra.



### Definition of the Eigenvector and Eigenvalue.

* An **eigenvector** of an $n \times n$ matrix $A$ is a nonzero vector $\mathbf{x}$ such that $A \mathbf{x} = \lambda \mathbf{x}$ for some scalar $\lambda$. A scalar $\lambda$ is called an **eigenvalue** of $A$ if there is a nontrivial solution $\mathbf{x}$ of $A\mathbf{x} = \lambda \mathbf{x}$; such an $\mathbf{x}$ is called an *eigenvector corresponding to* $\lambda$.

* $\lambda$ is an eigenvalue of an $n \times n$ matrix $A$ if and only if the equation
  $$
  (A - \lambda I) \mathbf{x} = \mathbf{0}
  $$
  has a nontrivial solution. The set of all solutions of the above equation is just the null space of the matrix $A - \lambda I$. So this set is a *subspace* of $\mathbb{R}^n$ and is called the **eigenspace** of $A$ corresponding to $\lambda$. The eigenspace consists of the zero vector and all the eigenvectors corresponding to $\lambda.$



### How do you find eigenvalues from a square matrix $A$?

* We can know that $\lambda$ is an eigenvalue of a square matrix $A$ if and only if the equation $(A - \lambda I)\mathbf{x} = \mathbf{0}$ has a nontrivial solution, which means that checking $(A-\lambda I)$ can be invertible or not will give us solutions for this.

* If we have this kind of matrix and want to know its eigenvalues
  $$
  \begin{bmatrix}
  4 & -2 \\
  -2 & 1
  \end{bmatrix}
  $$
  , we can construct this matrix
  $$
  \begin{bmatrix}
  4 - \lambda & -2  \\
  -2 & 1 - \lambda 
  \end{bmatrix}
  $$
  and then, the determinant of this matrix let us know  what values could be the eigenvalues for this matrix.
  $$
  \det(A) =  (4 - \lambda)(1 - \lambda) - 4
  $$
  The values will be the eigenvalues which makes the determinant as zero, because it means that you can't invert the matrix $A$, and that you will have nontrivial solutions:
  $$
  (\lambda - 4)(\lambda - 1) - 4 = 
  \lambda^2 - 5\lambda = \lambda(\lambda - 5) = 0
  $$
  So, the eigenvalues are $0$ and $ 5$.

* This scalar equation $\det(A - \lambda I) = 0$ is called the **characteristic equation** of $A$.

  

### How do you find eigenvectors from a square matrix $A$?

* If you found eigenvalues for a square matrix $A$, then the last thing is to solve the linear equation $(A - \lambda I) \mathbf{x} = \mathbf{0}$. Because you know what the $\lambda$s are, you can put the eigenvalues and then try to get $\mathbf{x}$s, which are eigenvectors. 

* However, as you already know, the $A - \lambda I$ has nontrivial solutions, because you can't invert $A - \lambda I$. So, you can get the set of the solutions (null space) like this:
  $$
  \begin{split}
  & A\mathbf{x} = \mathbf{0} \;\;\; (\lambda = 0) \\
  
  & 
  \begin{bmatrix}
  4 & -2 & 0 \\
  -2 & 1 & 0 
  \end{bmatrix} \sim
  \begin{bmatrix}
  1 & - \frac{1}{2} & 0 \\
  0 & 0 & 0
  \end{bmatrix} \;\;\; \text{(by row operations)}
  \\
  &
  \begin{bmatrix}
  x_1 \\ x_2
  \end{bmatrix} 
  = 
  
  x_2
  \begin{bmatrix}
  \frac{1}{2} \\
  1
  \end{bmatrix}
  
  \end{split}
  $$
  For the lambda value $0$, you get the eigenvectors $x_2 \begin{bmatrix} \frac{1}{2} \\ 1 \end{bmatrix}$. You can put any real to the $x_2$ and you can check that $A \mathbf{x}$ will be always $\mathbf{0}$.

* I will also do this for the lambda value $5$:
  $$
  \begin{split}
  & (A - 5I) \mathbf{x} = \mathbf{0} \;\;\; (\lambda = 5) \\
  
  & 
  \begin{bmatrix}
  -1 & -2 & 0 \\
  -2 & -4 & 0 
  \end{bmatrix} \sim
  \begin{bmatrix}
  1 & 2 & 0 \\
  0 & 0 & 0
  \end{bmatrix} \;\;\; \text{(by row operations)}
  \\
  &
  \begin{bmatrix}
  x_1 \\ x_2
  \end{bmatrix} 
  = 
  
  x_2
  \begin{bmatrix}
  -2 \\
  1
  \end{bmatrix}
  
  \end{split}
  $$
  you can also check that $A \times x_2 \begin{bmatrix} -2 \\ 1 \end{bmatrix} = 5x_2 \begin{bmatrix} -2 \\ 1 \end{bmatrix} $ always with your real values on $x_2$.



### How do you implement the function to calculate eigenvalues and eigenvectors?

* As for the $2 \times 2$ matrix, it will be easy and you don't need to worry for precision problems due to the small number of floating-point operations
* Converting a square matrix into a reduced row-echelon form will  cause floating-point errors.
* Due to the error, iterative methods with better precisions are preferred such as the Jacobi eigenvalue algorithm and the QR algorithm.
* Refer to these links:
  * https://en.wikipedia.org/wiki/Jacobi_eigenvalue_algorithm
  * https://en.wikipedia.org/wiki/QR_algorithm
  * https://on-demand.gputechconf.com/gtc/2017/presentation/s7121-lung-sheng-chien-jacobi-based-eigenvalue-solver.pdf

* If I understand those and implement them, I will update this document again. The eigenvalue solvers have lots of application to many problems. 



---

Lay, D. C., Lay, S. R., & McDonald, J. J. (2016). *Linear algebra and its Applications* (Fifth). Pearson. 