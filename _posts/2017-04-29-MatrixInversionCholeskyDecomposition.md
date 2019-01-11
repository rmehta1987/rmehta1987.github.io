---
layout: post
title: Cholesky decomposition for Matrix Inversion

---


Matrix inversion is a classical problem, and can be very complicated for large matrices. There are many ways to simplify this for special types of matrices. Among them, one is to transform the matrix into a set of upper or lower triangular matrices. Consider our target matrix $\mathbf{A}$ which is Hermitian and positive-definite. Such matrices are quite famous and an example is the covariance matrix in statistics. It’s inverse is seen in the Gaussian probability density function for vectors. Then, Cholesky decomposition breaks
\mathbf{A} = \mathbf{L}\mathbf{L}^T = \mathbf{U}^T\mathbf{U}

where \mathbf{L} is a lower triangular matrix, while \mathbf{U} is an upper triangular matrix.

It is much easier to compute the inverse of a triangular matrix and there exist numerical solutions. Then the original matrix inverse is computed simply by multiplying the two inverses as

\mathbf{A}^{-1} = (\mathbf{L}^{-1})^T(\mathbf{L}^{-1}) = (\mathbf{U}^{-1})(\mathbf{U}^{-1})^T 

As bonus, the determinant is also much easier to compute.

det(\mathbf{A}) = det(\mathbf{L})^2 

$$a^2 + b^2 = c^2$$


One can also use complex matrices, and just use a conjugate-transpose instead of transpose alone.

