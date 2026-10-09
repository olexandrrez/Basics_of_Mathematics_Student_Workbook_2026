# Problem 05: Matrix Times Vector

## 1. Original Problem
Let
$$A=\begin{pmatrix}2&-1\\1&3\end{pmatrix},\qquad x=\begin{pmatrix}4\\2\end{pmatrix}.$$
Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## 2. What We Are Trying to Find
We need to calculate the matrix-vector product $Ax$ by direct multiplication and then rewrite this resulting vector explicitly as a linear combination of the columns of $A$ weighted by the components of $x$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Row View of $Ax$**: The $i$-th entry of $Ax$ is the dot product of row $i$ of $A$ with vector $x$.
- **Column View of $Ax$ (Linear Combination)**: If $A = \begin{pmatrix} \mathbf{a}_1 & \mathbf{a}_2 \end{pmatrix}$ has columns $\mathbf{a}_1, \mathbf{a}_2$ and $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$, then:
  $$Ax = x_1 \mathbf{a}_1 + x_2 \mathbf{a}_2.$$
  Multiplying a matrix by a vector produces a linear combination of the columns of the matrix where the weights are the components of the vector.

## 4. Step-by-Step Solution

### Step 1: Direct Computation of $Ax$
Using the row-by-column rule:
$$Ax = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} 4 \\ 2 \end{pmatrix} = \begin{pmatrix} 2(4) + (-1)(2) \\ 1(4) + 3(2) \end{pmatrix} = \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}.$$

### Step 2: Express $Ax$ as a Linear Combination of Columns
Identify the columns of $A$:
$$\mathbf{a}_1 = \begin{pmatrix} 2 \\ 1 \end{pmatrix},\qquad \mathbf{a}_2 = \begin{pmatrix} -1 \\ 3 \end{pmatrix}.$$
The scalar coefficients are the components of $x$: $x_1 = 4$ and $x_2 = 2$.
Form the linear combination:
$$4\mathbf{a}_1 + 2\mathbf{a}_2 = 4\begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2\begin{pmatrix} -1 \\ 3 \end{pmatrix}.$$
Calculate entrywise to verify:
$$4\begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2\begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix} = \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}.$$
Both expressions produce the identical vector $\begin{pmatrix} 6 \\ 10 \end{pmatrix}$.

## 5. Why Each Step Is Valid
- The row-by-column definition and the column linear combination definition are algebraically identical; expanding $(a_{i1}x_1 + a_{i2}x_2)$ shows that the $i$-th component of the linear combination is exactly the dot product of row $i$ with $x$.
- Scalar multiplication of vectors scales each coordinate, and vector addition combines matching coordinates.

## 6. Final Answer in Words
The product is $Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$. Expressed as a linear combination of the columns of $A$, it is $4\begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2\begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$.

## 7. Quick Verification
- Check first coordinate: $4(2) + 2(-1) = 8 - 2 = 6$.
- Check second coordinate: $4(1) + 2(3) = 4 + 6 = 10$.
Both perspectives yield the exact same result $(6, 10)^T$.

## 8. Common Mistakes
- Misaligning coefficients: weighting the first column by 2 and the second by 4 instead of using $x_1 = 4$ and $x_2 = 2$.
- Confusing columns of $A$ with rows of $A$ when constructing the linear combination.

## 9. Short In-Class Explanation (3 Sentences)
Multiplying matrix $A$ by vector $x$ directly yields the output vector $(6, 10)^T$. Crucially, this same result can be viewed as taking 4 times the first column of $A$ plus 2 times the second column of $A$. This demonstrates the fundamental idea that a matrix-vector product is simply a linear combination of the matrix's columns.
