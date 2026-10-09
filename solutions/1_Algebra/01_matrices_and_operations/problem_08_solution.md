# Problem 08: Row Operations and Their Reversibility

## 1. Original Problem
For
$$A=\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}$$
perform, in order:
1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## 2. What We Are Trying to Find
We must apply three elementary row operations sequentially to a $3 \times 3$ matrix, record the intermediate matrices, and state the exact inverse row operation for each step that restores the previous matrix.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Elementary Row Operations**:
  1. Row addition: $R_i \leftarrow R_i + c R_j$ (adds a multiple of row $j$ to row $i$).
  2. Row swap: $R_i \leftrightarrow R_j$ (interchanges two rows).
  3. Row scaling: $R_i \leftarrow c R_i$ ($c \neq 0$).
- **Reversibility**: Elementary row operations are completely reversible. Each operation has an elementary inverse operation that undoes its geometric and algebraic effect.

## 4. Step-by-Step Solution

### Initial Matrix
$$A = \begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}.$$

### Step 1: Operation $R_2 \leftarrow R_2 - 2R_1$
- Row 1 remains: $(1, 2, -1)$.
- New Row 2:
  $$R_2 - 2R_1 = (2, 4, 1) - 2(1, 2, -1) = (2-2, 4-4, 1-(-2)) = (0, 0, 3).$$
- Row 3 remains: $(-1, 1, 3)$.
The matrix becomes:
$$A_1 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}.$$
- **Inverse Operation**: $R_2 \leftarrow R_2 + 2R_1$.

### Step 2: Operation $R_3 \leftarrow R_3 + R_1$
- New Row 3:
  $$R_3 + R_1 = (-1, 1, 3) + (1, 2, -1) = (-1+1, 1+2, 3+(-1)) = (0, 3, 2).$$
The matrix becomes:
$$A_2 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}.$$
- **Inverse Operation**: $R_3 \leftarrow R_3 - R_1$.

### Step 3: Interchange $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$)
Swap the second and third rows of $A_2$:
$$A_3 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}.$$
- **Inverse Operation**: Interchange $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$).

## 5. Why Each Step Is Valid
- Elementary row operations correspond to multiplying the matrix on the left by invertible elementary matrices.
- Because each elementary matrix is invertible, the linear combinations of rows preserve the solution space of the underlying linear system without loss of information.

## 6. Final Answer in Words
After the first operation, the matrix is $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}$, reversed by $R_2 \leftarrow R_2 + 2R_1$. After the second operation, it is $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}$, reversed by $R_3 \leftarrow R_3 - R_1$. After swapping rows, the final upper-triangular matrix is $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}$, reversed by swapping $R_2$ and $R_3$ again.

## 7. Quick Verification
- Reverse Step 3: Swap $R_2$ and $R_3$ of $A_3$ $\to$ recovers $A_2 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}$.
- Reverse Step 2: $R_3 - R_1$ on $A_2$ gives $(0-1, 3-2, 2-(-1)) = (-1, 1, 3)$, which recovers $A_1$.
- Reverse Step 1: $R_2 + 2R_1$ on $A_1$ gives $(0+2, 0+4, 3-2) = (2, 4, 1)$, which recovers original $A$.

## 8. Common Mistakes
- Arithmetic errors with negative signs when subtracting multiples (e.g., $1 - 2(-1) = 3$, not $-1$).
- Thinking that the inverse of swapping two rows requires a different operation, rather than simply swapping them back.

## 9. Short In-Class Explanation (3 Sentences)
We sequentially apply the row operations to eliminate entries in the first column and then swap rows to reach upper triangular form $\begin{pmatrix}1&2&-1\\0&3&2\\0&0&3\end{pmatrix}$. Each row operation is completely reversible because subtracting a multiple is undone by adding that multiple, and swapping rows is undone by swapping them back. This reversibility guarantees that Gaussian elimination preserves the full information of the original matrix.
