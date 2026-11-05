# Problem 9: Laplace Expansion of a Determinant

## Problem

Calculate
$$\det\begin{pmatrix}0&2&0\\1&-1&3\\4&0&2\end{pmatrix}$$
by Laplace expansion along the first row. Check the result by expanding down the first column.

## Worked Solution

Expanding along row 1 uses the alternating cofactor signs $+,-,+$. The first and third entries in that row are zero, so only the middle term contributes:
$$\det A=0-2\det\begin{pmatrix}1&3\\4&2\end{pmatrix}+0=-2(1\cdot2-3\cdot4)=-2(-10)=20.$$

Now expand down column 1. Its entries are $0,1,4$, with signs $+,-,+$:
$$\det A=0-1\det\begin{pmatrix}2&0\\0&2\end{pmatrix}+4\det\begin{pmatrix}2&0\\-1&3\end{pmatrix}=-4+4(6)=20.$$

**Answer:** $\boxed{20}$. Both expansions give the same determinant.
