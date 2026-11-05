# Problem 6: Singular Values of a Parameter

## Problem

For which real values of $t$ is
$$A(t)=\begin{pmatrix}t&2\\3&t-1\end{pmatrix}$$
singular?

## Worked Solution

A square matrix is singular exactly when its determinant is zero. For a $2\times2$ matrix, the determinant is the product of the main diagonal entries minus the product of the other diagonal entries:
$$\det A(t)=t(t-1)-2\cdot3=t^2-t-6=(t-3)(t+2).$$
Setting this equal to zero gives $t=3$ or $t=-2$.

**Answer:** $\boxed{t\in\{-2,3\}}$.

**Check.** Substitution into $(t-3)(t+2)$ gives zero for both values, so the determinant vanishes in each case.
