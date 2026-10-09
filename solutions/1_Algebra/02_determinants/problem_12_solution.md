# Problem 12: A Parameter Revealed by a Row Operation

## 1. Original Problem
For
$$A(t)=\begin{pmatrix}1&2&3\\2&4&t\\0&1&1\end{pmatrix}$$
find the values of $t$ for which the matrix is not invertible.
Before computing the determinant, perform the operation
$$R_2\leftarrow R_2-2R_1$$
and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

## 2. What We Are Trying to Find
We need to apply the row operation $R_2 \leftarrow R_2 - 2R_1$ to simplify $A(t)$, compute the determinant from the simplified matrix, identify the parameter value $t$ that makes the determinant zero (rendering $A(t)$ non-invertible), and explain the geometric row dependence that occurs at that value.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Determinant Invariance Under Row Addition**: $R_2 \leftarrow R_2 - 2R_1$ leaves $\det A(t)$ unchanged.
- **Invertibility Criterion**: Matrix $A(t)$ is not invertible if and only if $\det A(t) = 0$.
- **Linear Dependence**: If $\det A(t) = 0$, the rows of $A(t)$ must be linearly dependent.

## 4. Step-by-Step Solution

### Step 1: Perform the Specified Row Operation
$$A(t) = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & t \\ 0 & 1 & 1 \end{pmatrix}.$$
Apply $R_2 \leftarrow R_2 - 2R_1$:
$$R_2 - 2R_1 = (2, 4, t) - 2(1, 2, 3) = (2-2, 4-4, t-6) = (0, 0, t-6).$$
The matrix becomes:
$$A_1(t) = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & t-6 \\ 0 & 1 & 1 \end{pmatrix}.$$
Because row addition preserves the determinant, $\det A(t) = \det A_1(t)$.

### Step 2: Compute the Determinant Using the Simplified Structure
Expand $\det A_1(t)$ along its first column (which has only one non-zero entry):
$$\det A_1(t) = 1 \cdot \det\begin{pmatrix} 0 & t-6 \\ 1 & 1 \end{pmatrix} - 0 + 0.$$
Compute the $2 \times 2$ determinant:
$$\det\begin{pmatrix} 0 & t-6 \\ 1 & 1 \end{pmatrix} = (0)(1) - (t-6)(1) = -(t-6) = 6 - t.$$
Therefore:
$$\det A(t) = 6 - t.$$

### Step 3: Find Values Where Matrix Is Not Invertible
A matrix is not invertible if and only if its determinant is zero:
$$6 - t = 0 \implies t = 6.$$

### Step 4: Explain What Happens to the Rows at $t=6$
When $t = 6$:
- Look at the first two rows of the original matrix $A(6)$:
  $$R_1 = (1, 2, 3),\qquad R_2 = (2, 4, 6).$$
- Notice that:
  $$R_2 = 2 R_1.$$
Row 2 is exactly twice Row 1.
Because one row is an exact scalar multiple of another, the rows are linearly dependent. In the simplified matrix, Row 2 becomes $(0, 0, 6-6) = (0, 0, 0)$, a row of pure zeros. A row of zeros means the matrix collapses rank, has zero determinant, and cannot be inverted.

## 5. Why Each Step Is Valid
- Row replacement $R_2 \leftarrow R_2 - 2R_1$ strictly preserves the determinant value.
- Expanding along column 1 reduces the $3 \times 3$ determinant to a single $2 \times 2$ calculation.
- The condition $\det A(t) = 0$ is the exact algebraic characterization of non-invertibility.

## 6. Final Answer in Words
The matrix $A(t)$ is not invertible when $t = 6$. At $t = 6$, the second row $(2, 4, 6)$ becomes an exact scalar multiple of the first row $(1, 2, 3)$ ($R_2 = 2R_1$). This linear dependence causes the second row of the simplified matrix to become all zeros, making the determinant zero and the matrix singular.

## 7. Quick Verification
- Compute $\det A(t)$ by Sarrus' rule on the original matrix:
  Main diagonals: $1(4)(1) + 2(t)(0) + 3(2)(1) = 4 + 0 + 6 = 10$.
  Anti-diagonals: $3(4)(0) + 1(t)(1) + 2(2)(1) = 0 + t + 4 = t + 4$.
  $\det A(t) = 10 - (t + 4) = 6 - t$.
  Setting $6 - t = 0$ gives $t = 6$. Confirmed.

## 8. Common Mistakes
- Miscalculating the $2 \times 2$ determinant: forgetting the minus sign on $(t-6)(1)$, writing $t-6$ instead of $6-t$.
- Failing to explain the geometric dependence between the rows of the original matrix.

## 9. Short In-Class Explanation (3 Sentences)
Subtracting twice the first row from the second row produces $(0, 0, t-6)$, leaving only one non-zero entry in that row. Expanding along the first column gives the determinant $6 - t$, which equals zero when $t = 6$. At $t = 6$, the second row of the original matrix is exactly twice the first row, creating linear dependence and making the matrix non-invertible.
