# Problem 8: Minor and Cofactor

## Problem

For
$$A=\begin{pmatrix}2&1&0\\-1&3&2\\1&0&4\end{pmatrix},$$
find the minor $M_{23}$ and cofactor $C_{23}$. Explain their sign difference.

## Worked Solution

To find $M_{23}$, delete row 2 and column 3. The remaining $2\times2$ matrix is
$$\begin{pmatrix}2&1\\1&0\end{pmatrix},$$
so its determinant, the minor, is
$$M_{23}=2\cdot0-1\cdot1=-1.$$
The cofactor includes the position-dependent sign $(-1)^{i+j}$:
$$C_{23}=(-1)^{2+3}M_{23}=-(-1)=1.$$

**Answer:** $\boxed{M_{23}=-1,\ C_{23}=1}$. The sign changes because position $(2,3)$ has odd index sum.
