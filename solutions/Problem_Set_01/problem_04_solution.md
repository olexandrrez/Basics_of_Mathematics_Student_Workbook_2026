# Problem 4: Transpose of a Product

## Problem

Let
$$A=\begin{pmatrix}1&0&2\\-1&3&1\end{pmatrix},\qquad B=\begin{pmatrix}2&1\\0&-1\\1&2\end{pmatrix}.$$
Calculate $(AB)^T$ and verify $(AB)^T=B^TA^T$.

## Worked Solution

Multiplying rows of $A$ by columns of $B$ gives
$$AB=\begin{pmatrix}1\cdot2+0\cdot0+2\cdot1&1\cdot1+0\cdot(-1)+2\cdot2\\(-1)\cdot2+3\cdot0+1\cdot1&(-1)\cdot1+3\cdot(-1)+1\cdot2\end{pmatrix}=\begin{pmatrix}4&5\\-1&-2\end{pmatrix}.$$
Thus
$$ (AB)^T=\begin{pmatrix}4&-1\\5&-2\end{pmatrix}. $$
For an independent verification, transpose the original matrices:
$$B^T=\begin{pmatrix}2&0&1\\1&-1&2\end{pmatrix},\qquad A^T=\begin{pmatrix}1&-1\\0&3\\2&1\end{pmatrix}.$$
Their product is
$$B^TA^T=\begin{pmatrix}2+0+2&-2+0+1\\1+0+4&-1-3+2\end{pmatrix}=\begin{pmatrix}4&-1\\5&-2\end{pmatrix}=(AB)^T.$$

**Check.** Both sides are $2\times2$ and have identical entries, verifying the transpose-of-a-product identity in this example.
