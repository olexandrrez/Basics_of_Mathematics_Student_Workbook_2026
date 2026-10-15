# Problem 01: Matrix Size and Entries

## Problem

Given

$$A=\begin{pmatrix}2&-1&3\\0&4&5\end{pmatrix},\qquad
B=\begin{pmatrix}1&0\\-2&3\\4&1\end{pmatrix}.$$

1. State the sizes of matrices $A$ and $B$.
2. Find the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## Worked Solution

A matrix's size is **number of rows times number of columns**. Matrix $A$ has two rows and three columns, so it is $2\times3$. Matrix $B$ has three rows and two columns, so it is $3\times2$.

In the notation $a_{ij}$, the first index $i$ selects the row and the second index $j$ selects the column. Reading the indicated positions from the given matrices gives

$$a_{12}=-1,\qquad a_{23}=5,\qquad b_{21}=-2,\qquad b_{32}=1.$$

The second row of $A$ runs horizontally across row 2, so as a row vector it is

$$\begin{pmatrix}0&4&5\end{pmatrix}.$$

The first column of $B$ runs vertically down column 1, so as a column vector it is

$$\begin{pmatrix}1\\-2\\4\end{pmatrix}.$$

**Check.** In $A$, row 1 is $(2,-1,3)$, confirming $a_{12}=-1$, and row 2 is $(0,4,5)$, confirming $a_{23}=5$ and the requested second row. In $B$, row 2 is $(-2,3)$ and row 3 is $(4,1)$, confirming $b_{21}=-2$, $b_{32}=1$, and that its first column is $(1,-2,4)^T$. The vector orientations also match the matrices: a row is horizontal and a column is vertical.
