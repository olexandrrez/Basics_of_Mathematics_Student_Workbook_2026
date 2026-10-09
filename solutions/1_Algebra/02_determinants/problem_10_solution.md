# Problem 10: Detecting Dependence

## 1. Original Problem
Without carrying out a full determinant calculation, explain why
$$\det\begin{pmatrix}1&2&3\\2&4&6\\0&1&5\end{pmatrix}=0.$$
Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

## 2. What We Are Trying to Find
We must explain why the determinant is zero by inspecting the structural relationship between the rows of the matrix, formulate the linear dependence relation explicitly, and explain why linear dependence implies that the matrix is not invertible.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Linear Dependence of Rows**: If one row of a matrix is a scalar multiple of another row (or a linear combination of other rows), the rows are linearly dependent.
- **Determinant Zero Theorem**: A matrix with linearly dependent rows has determinant zero.
- **Row Elimination Property**: If $R_2 = c R_1$, performing the row operation $R_2 \leftarrow R_2 - c R_1$ produces a row of all zeros. Any matrix with a row of zeros has determinant zero.
- **Invertibility**: A matrix is invertible if and only if its rows form a linearly independent basis for $\mathbb{R}^n$.

## 4. Step-by-Step Solution

### Step 1: Inspect the Rows of the Matrix
The rows are:
$$R_1 = (1, 2, 3),$$
$$R_2 = (2, 4, 6),$$
$$R_3 = (0, 1, 5).$$

### Step 2: Identify the Specific Dependence
Comparing $R_1$ and $R_2$:
$$2 \cdot R_1 = 2 \cdot (1, 2, 3) = (2(1), 2(2), 2(3)) = (2, 4, 6) = R_2.$$
Thus, Row 2 is exactly twice Row 1:
$$R_2 - 2R_1 = (0, 0, 0).$$
The rows are linearly dependent.

### Step 3: Connect Dependence to Determinant Value
Apply the row operation $R_2 \leftarrow R_2 - 2R_1$:
- Because adding a multiple of one row to another does not change the determinant,
  $$\det\begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix} = \det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \end{pmatrix}.$$
- Expanding along the second row (which contains only zeros):
  $$\det = -0 \cdot M_{21} + 0 \cdot M_{22} - 0 \cdot M_{23} = 0.$$
Therefore, the determinant is zero without any heavy arithmetic.

### Step 4: Connect to Noninvertibility
Because $R_2$ provides no new information beyond $R_1$, the row vectors span at most a 2-dimensional plane rather than the full 3-dimensional space $\mathbb{R}^3$.
The corresponding linear transformation collapses 3-dimensional space onto a plane or line, flattening volume to zero.
Because multiple distinct input vectors are mapped to the same output vector (the kernel contains non-trivial vectors), the transformation is not injective (one-to-one) and cannot be inverted.

## 5. Why Each Step Is Valid
- The equality $R_2 = 2R_1$ is an exact entry-by-entry scalar multiplication identity.
- Invariance of determinants under row additions ensures that the matrix with a row of zeros has the exact same determinant as the original matrix.

## 6. Final Answer in Words
The determinant is $0$ because the second row is an exact scalar multiple of the first row ($R_2 = 2R_1$). This linear dependence means that subtracting $2R_1$ from $R_2$ creates an entire row of zeros. Because the rows are linearly dependent, the matrix has rank less than 3, collapses 3D volume to zero, and cannot be inverted.

## 7. Quick Verification
- Compute by Sarrus' rule to confirm:
  Main diagonals: $1(4)(5) + 2(6)(0) + 3(2)(1) = 20 + 0 + 6 = 26$.
  Anti-diagonals: $3(4)(0) + 1(6)(1) + 2(2)(5) = 0 + 6 + 20 = 26$.
  $\det = 26 - 26 = 0$.
  Confirms the zero determinant.

## 8. Common Mistakes
- Blindly launching into Sarrus' rule without noticing the obvious row proportionality.
- Confusing linear dependence with parallel columns; here the dependence is directly between the first two rows.

## 9. Short In-Class Explanation (3 Sentences)
We observe that the second row $(2, 4, 6)$ is exactly twice the first row $(1, 2, 3)$, making the rows linearly dependent. Performing the operation $R_2 - 2R_1$ creates a row of all zeros without changing the determinant, which immediately proves the determinant is zero. Because the rows do not span full three-dimensional space, the matrix compresses space and is not invertible.
