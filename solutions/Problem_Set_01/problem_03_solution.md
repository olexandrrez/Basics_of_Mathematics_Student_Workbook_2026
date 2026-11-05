# Problem 3: Products in Both Orders

## Problem

For
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}3&0\\2&1\end{pmatrix},$$
find $AB$ and $BA$. Does multiplication commute for this pair?

## Worked Solution

Each entry of a product is the dot product of a row of the first matrix and a column of the second. First,
$$AB=\begin{pmatrix}1\cdot3+1\cdot2&1\cdot0+1\cdot1\\0\cdot3+1\cdot2&0\cdot0+1\cdot1\end{pmatrix}=\begin{pmatrix}5&1\\2&1\end{pmatrix}.$$
Reversing the order gives
$$BA=\begin{pmatrix}3\cdot1+0\cdot0&3\cdot1+0\cdot1\\2\cdot1+1\cdot0&2\cdot1+1\cdot1\end{pmatrix}=\begin{pmatrix}3&3\\2&3\end{pmatrix}.$$
The products differ, so multiplication does **not** commute for this pair: $AB\ne BA$.

**Check.** Both results are $2\times2$, as required. Their $(1,1)$ entries, $5$ and $3$, already establish that the products are unequal.
