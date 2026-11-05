# Problem 10: Determinant Properties

## Problem

Let $A,B$ be $3\times3$ matrices with $\det A=-2$ and $\det B=5$. Find $\det(AB)$ and $\det(2A^T)$. A matrix $C$ is formed from $A$ by swapping two rows and then multiplying one row by $3$; find $\det C$.

## Worked Solution

The product rule gives
$$\det(AB)=\det A\det B=(-2)(5)=\boxed{-10}.$$
Transposition does not change a determinant, and multiplying every row of a $3\times3$ matrix by $2$ multiplies its determinant by $2^3$:
$$\det(2A^T)=2^3\det(A^T)=8\det A=8(-2)=\boxed{-16}.$$
Swapping two rows reverses the determinant's sign, changing $-2$ to $2$. Multiplying one row by $3$ then multiplies the determinant by $3$, so
$$\det C=3(2)=\boxed{6}.$$

**Check.** Each factor reflects one determinant rule: product of matrices, scaling all three rows, invariance under transpose, and the two specified row operations.
