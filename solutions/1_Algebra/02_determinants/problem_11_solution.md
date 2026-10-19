# Problem 11: Shortening the Calculation with Row Operations

## 1. Original Problem
Compute
$$\det\begin{pmatrix}1&2&3\\1&3&4\\1&4&6\end{pmatrix}$$
by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## 2. What We Are Trying to Find
We must evaluate the determinant of a $3 \times 3$ matrix by strategically applying elementary row operations to introduce zeros into the matrix, identify which operations leave the determinant value invariant, and compute the final determinant from the resulting triangular matrix.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Invariance Under Row Replacement**: The row operation $R_i \leftarrow R_i + c R_j$ ($i \neq j$) leaves the determinant unchanged:
  $$\det(A) = \det(A').$$
- **Triangular Matrix Rule**: Once a matrix is reduced to upper-triangular form with zeros below the diagonal, its determinant is simply the product of its diagonal elements:
  $$\det T = t_{11} t_{22} t_{33}.$$

## 4. Step-by-Step Solution

### Initial Matrix
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix}.$$

### Step 1: Create Zeros in the First Column
Subtract Row 1 from Row 2 and Row 3:
- **Operation 1**: $R_2 \leftarrow R_2 - R_1$.
  $$R_2 - R_1 = (1, 3, 4) - (1, 2, 3) = (0, 1, 1).$$
  *Effect on determinant*: Does not change the determinant.
- **Operation 2**: $R_3 \leftarrow R_3 - R_1$.
  $$R_3 - R_1 = (1, 4, 6) - (1, 2, 3) = (0, 2, 3).$$
  *Effect on determinant*: Does not change the determinant.

The matrix becomes:
$$A_1 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}, \qquad \det A = \det A_1.$$

### Step 2: Create a Zero in the Second Column Below Pivot
Use Row 2 to eliminate the entry in Row 3:
- **Operation 3**: $R_3 \leftarrow R_3 - 2R_2$.
  $$R_3 - 2R_2 = (0, 2, 3) - 2(0, 1, 1) = (0, 2-2, 3-2) = (0, 0, 1).$$
  *Effect on determinant*: Does not change the determinant.

The matrix is now upper-triangular:
$$A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}, \qquad \det A = \det A_2.$$

### Step 3: Compute the Determinant
Since $A_2$ is upper-triangular, multiply its main diagonal entries:
$$\det A = 1 \cdot 1 \cdot 1 = 1.$$

## 5. Why Each Step Is Valid
- The row operations $R_2 \leftarrow R_2 - R_1$, $R_3 \leftarrow R_3 - R_1$, and $R_3 \leftarrow R_3 - 2R_2$ are all of the form $R_i \leftarrow R_i + cR_j$. None of them scale or swap rows, so each preserves the determinant value exactly.
- Computing the product of diagonal entries of an upper-triangular matrix evaluates its determinant identically.

## 6. Final Answer in Words
The determinant of the matrix is $1$. The row operations $R_2 \leftarrow R_2 - R_1$, $R_3 \leftarrow R_3 - R_1$, and $R_3 \leftarrow R_3 - 2R_2$ did not change the determinant at any step, reducing the matrix to an upper-triangular matrix with ones along the diagonal.

## 7. Quick Verification
- Compute directly using Sarrus' rule on the original matrix:
  Main diagonals: $1(3)(6) + 2(4)(1) + 3(1)(4) = 18 + 8 + 12 = 38$.
  Anti-diagonals: $3(3)(1) + 1(4)(4) + 2(1)(6) = 9 + 16 + 12 = 37$.
  $\det A = 38 - 37 = 1$.
  Both methods yield exactly $1$.

## 8. Common Mistakes
- Miscalculating the anti-diagonal sum in Sarrus' rule when large numbers are involved, which demonstrates why row operations are much safer and less error-prone.
- Forgetting that row scaling $R_i \leftarrow c R_i$ alters the determinant by $c$, whereas row replacement $R_i \leftarrow R_i + c R_j$ leaves it invariant.

## 9. Short In-Class Explanation (3 Sentences)
We simplify the matrix by subtracting the first row from the second and third rows, and then subtracting twice the second row from the third row. None of these row additions change the value of the determinant, and they reduce the matrix to upper-triangular form with ones on the main diagonal. The determinant is simply the product of the diagonal entries, which gives $1 \times 1 \times 1 = 1$.
