# Problem 5: Solving a System with the Inverse Matrix

## Problem

Use the inverse-matrix method to solve
$$\begin{cases}3x+y=11,\\2x+y=8.\end{cases}$$
Compare your answer with direct subtraction.

## Worked Solution

Write $AX=b$, where
$$A=\begin{pmatrix}3&1\\2&1\end{pmatrix},\quad X=\begin{pmatrix}x\\y\end{pmatrix},\quad b=\begin{pmatrix}11\\8\end{pmatrix}.$$
The determinant is $3\cdot1-2\cdot1=1$, so
$$A^{-1}=\begin{pmatrix}1&-1\\-2&3\end{pmatrix}.$$
Then
$$X=A^{-1}b=\begin{pmatrix}1&-1\\-2&3\end{pmatrix}\begin{pmatrix}11\\8\end{pmatrix}=\begin{pmatrix}3\\2\end{pmatrix}.$$
Thus $(x,y)=(3,2)$.

Direct subtraction gives $(3x+y)-(2x+y)=11-8$, hence $x=3$; substituting into $2x+y=8$ gives $y=2$. Both methods agree.

**Check.** $3(3)+2=11$ and $2(3)+2=8$.
