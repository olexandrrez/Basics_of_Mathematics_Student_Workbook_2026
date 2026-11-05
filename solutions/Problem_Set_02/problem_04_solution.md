# Problem 4: Gaussian Elimination and Cramer's Rule

## Problem

Solve by Gaussian elimination
$$\begin{cases}x+y+z=4,\\2x-y+z=8,\\x+2y-z=-3.\end{cases}$$
Then independently compute $z$ using Cramer's rule on the $3\times3$ coefficient matrix.

## Worked Solution

Write the augmented matrix and eliminate entries below the first pivot:
$$\left[\begin{array}{rrr|r}1&1&1&4\\2&-1&1&8\\1&2&-1&-3\end{array}\right]\xrightarrow{R_2-2R_1,\ R_3-R_1}
\left[\begin{array}{rrr|r}1&1&1&4\\0&-3&-1&0\\0&1&-2&-7\end{array}\right].$$
Swap rows 2 and 3, then eliminate the second-column entry in row 3:
$$\left[\begin{array}{rrr|r}1&1&1&4\\0&1&-2&-7\\0&-3&-1&0\end{array}\right]\xrightarrow{R_3+3R_2}
\left[\begin{array}{rrr|r}1&1&1&4\\0&1&-2&-7\\0&0&-7&-21\end{array}\right].$$
Back-substitution gives $z=3$, then $y-2(3)=-7$, so $y=-1$, and $x-1+3=4$, so $x=2$.

For the independent Cramer's-rule calculation of $z$, the coefficient determinant and the determinant with column 3 replaced by the constants are
$$\Delta=\det\begin{pmatrix}1&1&1\\2&-1&1\\1&2&-1\end{pmatrix}=7,$$
$$\Delta_z=\det\begin{pmatrix}1&1&4\\2&-1&8\\1&2&-3\end{pmatrix}=21.$$
Since $\Delta\ne0$, Cramer's rule gives $z=\Delta_z/\Delta=21/7=3$.

**Check.** $(2,-1,3)$ gives $2-1+3=4$, $4+1+3=8$, and $2-2-3=-3$.
