# Problem 2: Scalar Multiplication and Subtraction

## Problem

Calculate $2A-3B$ for
$$A=\begin{pmatrix}2&-1\\3&4\end{pmatrix},\qquad B=\begin{pmatrix}1&2\\-2&0\end{pmatrix}.$$

## Worked Solution

Both matrices are $2\times2$, so we can multiply corresponding entries by the scalars and subtract the resulting matrices entry by entry:
$$2A=\begin{pmatrix}4&-2\\6&8\end{pmatrix},\qquad 3B=\begin{pmatrix}3&6\\-6&0\end{pmatrix}.$$
Therefore
$$2A-3B=\begin{pmatrix}4-3&-2-6\\6-(-6)&8-0\end{pmatrix}=\boxed{\begin{pmatrix}1&-8\\12&8\end{pmatrix}}.$$

**Check.** The result is still $2\times2$, and entrywise subtraction gives $1,-8,12,8$ in the corresponding positions.
