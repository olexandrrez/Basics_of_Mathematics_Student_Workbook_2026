# Problem 10: Columns of a Matrix Product

## 1. Original Problem
Given
$$A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&2\\-1&0\\3&1\end{pmatrix}.$$
Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## 2. What We Are Trying to Find
We need to multiply matrix $A$ individually by each column vector of $B$, compute the full matrix product $AB$, and explain the structural theorem that the columns of a matrix product are the products of the left matrix with each column of the right matrix.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Column Definition of Matrix Multiplication**: If a matrix $B$ is partitioned by its columns as $B = \begin{pmatrix} b_1 & b_2 & \dots & b_k \end{pmatrix}$, then the matrix product $AB$ is given by:
  $$AB = \begin{pmatrix} Ab_1 & Ab_2 & \dots & Ab_k \end{pmatrix}.$$
  Each column of $AB$ is formed independently by multiplying $A$ by the corresponding column of $B$.

## 4. Step-by-Step Solution

### Step 1: Compute $Ab_1$ and $Ab_2$
The columns of $B$ are:
$$b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix},\qquad b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}.$$
- Compute $Ab_1$:
  $$Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(-1) + 0(3) \\ 0(1) + 1(-1) + 1(3) \end{pmatrix} = \begin{pmatrix} 1 - 2 + 0 \\ 0 - 1 + 3 \end{pmatrix} = \begin{pmatrix} -1 \\ 2 \end{pmatrix}.$$
- Compute $Ab_2$:
  $$Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 1(2) + 2(0) + 0(1) \\ 0(2) + 1(0) + 1(1) \end{pmatrix} = \begin{pmatrix} 2 + 0 + 0 \\ 0 + 0 + 1 \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}.$$

### Step 2: Compute the Full Product $AB$
$A$ is $2 \times 3$ and $B$ is $3 \times 2$, so $AB$ is $2 \times 2$:
$$AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}$$
- Entry $(1,1)$: $1(1) + 2(-1) + 0(3) = -1$.
- Entry $(1,2)$: $1(2) + 2(0) + 0(1) = 2$.
- Entry $(2,1)$: $0(1) + 1(-1) + 1(3) = 2$.
- Entry $(2,2)$: $0(2) + 1(0) + 1(1) = 1$.
Thus:
$$AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}.$$

### Step 3: Compare and Explain
Notice that:
- Column 1 of $AB$ is $\begin{pmatrix} -1 \\ 2 \end{pmatrix}$, which is exactly $Ab_1$.
- Column 2 of $AB$ is $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$, which is exactly $Ab_2$.
Therefore:
$$AB = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}.$$
**Why this holds**: The $(i, j)$ entry of $AB$ is defined as the dot product of row $i$ of $A$ with column $j$ of $B$. But this is identically the $i$-th entry of the matrix-vector product $A b_j$. Therefore, collecting all rows for a fixed column $j$ forms the complete vector $Ab_j$.

## 5. Why Each Step Is Valid
- Matrix multiplication distributes naturally across the column partitioning of the right matrix.
- The dot product definition of matrix multiplication evaluates each column of the product independently of all other columns.

## 6. Final Answer in Words
The individual matrix-vector products are $Ab_1 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}$ and $Ab_2 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$. The product matrix is $AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}$. The columns of $AB$ are precisely $Ab_1$ and $Ab_2$ because matrix multiplication acts on each column of the right matrix separately.

## 7. Quick Verification
- Check column 1: $1 \cdot \begin{pmatrix}1\\0\end{pmatrix} - 1 \cdot \begin{pmatrix}2\\1\end{pmatrix} + 3 \cdot \begin{pmatrix}0\\1\end{pmatrix} = \begin{pmatrix}1-2+0\\0-1+3\end{pmatrix} = \begin{pmatrix}-1\\2\end{pmatrix}$. Matches.
- Check column 2: $2 \cdot \begin{pmatrix}1\\0\end{pmatrix} + 0 \cdot \begin{pmatrix}2\\1\end{pmatrix} + 1 \cdot \begin{pmatrix}0\\1\end{pmatrix} = \begin{pmatrix}2+0+0\\0+0+1\end{pmatrix} = \begin{pmatrix}2\\1\end{pmatrix}$. Matches.

## 8. Common Mistakes
- Computing rows instead of columns: thinking the rows of $AB$ are $a_i B$ without transposing properly.
- Forgetting that $b_1$ and $b_2$ are vertical columns of $B$, not horizontal rows.

## 9. Short In-Class Explanation (3 Sentences)
Computing $Ab_1$ and $Ab_2$ yields the vectors $(-1, 2)^T$ and $(2, 1)^T$. When we compute the full product matrix $AB$, these two vectors form its first and second columns. This demonstrates the column perspective of matrix multiplication: multiplying $A$ by $B$ simply transforms every column of $B$ by $A$.
