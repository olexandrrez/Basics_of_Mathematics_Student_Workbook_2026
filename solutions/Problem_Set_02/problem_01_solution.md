# Problem 1: Inverse of a 2×2 Matrix

## Problem

Find $A^{-1}$ for
$$A=\begin{pmatrix}3&1\\2&1\end{pmatrix}$$
and verify $AA^{-1}=I$.

## Worked Solution

For $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, if $ad-bc\ne0$, then
$$A^{-1}=\frac1{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}.$$
Here $\det A=3\cdot1-1\cdot2=1$, so the inverse exists and
$$A^{-1}=\begin{pmatrix}1&-1\\-2&3\end{pmatrix}.$$
Verify by multiplication:
$$AA^{-1}=\begin{pmatrix}3&1\\2&1\end{pmatrix}\begin{pmatrix}1&-1\\-2&3\end{pmatrix}=\begin{pmatrix}3-2&-3+3\\2-2&-2+3\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}=I_2.$$

**Answer:** $\boxed{A^{-1}=\begin{pmatrix}1&-1\\-2&3\end{pmatrix}}$.
