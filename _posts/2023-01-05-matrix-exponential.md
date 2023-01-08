---
title: The Matrix Exponential 
categories: [Math, Linear Algebra ]
tags: [PDF, Matrix Exponential]
math: true
mermaid: true
---

If a matrix A is diagonalizable, then there exists an invertible P so that $A = PDP^{−1}$, where D is a diagonal matrix of eigenvalues of A, and P is a matrix having eigenvectors of A as its columns. In this case, $e^A = Pe^D P^{-1}$.



If A is an $n \times n$ matrix with a single eigenvalue $\lambda$, then there exist a nonnegtive integer $k < n$ such that 
$$
e^{tA} = e^{\lambda t} \left[ \mathbb I + t(A-\lambda \mathbb I)+ \frac{t^2}{2!}(A-\lambda \mathbb I)^2+\cdots+\frac{t^k}{k!}(A-\lambda \mathbb I)^k\right]
\,.
$$

If $\lambda$ is an eigenvalue of $A$ and $(A-\lambda \mathbb I)^p \, {\mathbf v} = 0$ for some $p\ge 1$, 
then $\mathbf v$ is called a generalized eigenvector of $A$.
When eigenvalues have algebraic multiplicity greater than one, we can compute extra solutions by looking for vectors in the nullspace of $(A-\lambda \mathbb I)^p$.

Ref: [The Ordinary Differential Equations Project](http://faculty.sfasu.edu/judsontw/ode/html-20180819/odeproject.html)  by Thomas W. Judson.
