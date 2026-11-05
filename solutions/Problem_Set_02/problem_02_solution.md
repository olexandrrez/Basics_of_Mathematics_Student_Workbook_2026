# Problem 2: Inverse of an Upper-Triangular Matrix

## Problem

Find the inverse of
$$A=\begin{pmatrix}1&1&0\\0&1&1\\0&0&1\end{pmatrix}.$$
Show the row operations or solve $AX=I$.

## Worked Solution

Let the columns of $X$ be solutions to $Ax=e_1$, $Ax=e_2$, and $Ax=e_3$. Since $A$ is upper triangular, back-substitution finds each column.

For $Ax=e_1$, the equations give $x_3=0$, $x_2+x_3=0$, and $x_1+x_2=1$, hence the first column is $(1,0,0)^T$. For $Ax=e_2$, they give $x_3=0$, $x_2+x_3=1$, and $x_1+x_2=0$, hence the second column is $(-1,1,0)^T$. For $Ax=e_3$, they give $x_3=1$, $x_2+x_3=0$, and $x_1+x_2=0$, hence the third column is $(1,-1,1)^T$. Therefore
$$A^{-1}=X=\begin{pmatrix}1&-1&1\\0&1&-1\\0&0&1\end{pmatrix}.$$

**Verification.** Multiplying $A$ by this matrix gives diagonal entries $1$ and all off-diagonal entries $0$, so $AA^{-1}=I_3$.
