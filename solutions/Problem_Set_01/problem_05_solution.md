# Problem 5: Matrix Classifications

## Problem

Classify
$$D=\begin{pmatrix}3&0\\0&3\end{pmatrix},\quad S=\begin{pmatrix}1&-2\\-2&5\end{pmatrix},\quad K=\begin{pmatrix}0&4\\-4&0\end{pmatrix}$$
as diagonal, scalar, symmetric, and/or skew-symmetric; more than one label may apply. Also classify
$$T=\begin{pmatrix}2&1\\0&3\end{pmatrix},\qquad I_2,\qquad 0_{2\times3}$$
as triangular, identity, or zero matrices, stating their dimensions.

## Worked Solution

A diagonal matrix has zero entries off the main diagonal; a scalar matrix is a scalar multiple of the identity. A matrix is symmetric when its transpose equals itself, and skew-symmetric when its transpose is its negative.

- $D=3I_2$ is diagonal, scalar, and symmetric. It is not skew-symmetric, since its nonzero diagonal entries cannot equal their own negatives.
- $S^T=S$, because the two off-diagonal entries are both $-2$. Thus $S$ is symmetric. It is neither diagonal nor scalar, and it is not skew-symmetric (its diagonal entries are nonzero).
- $K^T=\begin{pmatrix}0&-4\\4&0\end{pmatrix}=-K$, so $K$ is skew-symmetric. It is not diagonal, scalar, or symmetric.

For the remaining matrices, $T$ is $2\times2$ and has zeros below the diagonal, so it is upper triangular. It is not lower triangular because its upper-right entry is $1$. The matrix $I_2=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ is the $2\times2$ identity; it is also diagonal and both upper and lower triangular. Finally, $0_{2\times3}$ is the $2\times3$ zero matrix; it is not an identity matrix, and the usual triangular classification applies to square matrices, so it is not called triangular.

**Check.** The transpose tests distinguish symmetric from skew-symmetric matrices, while the sizes and locations of zero entries establish the remaining classifications.
