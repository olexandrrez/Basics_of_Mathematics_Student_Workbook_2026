# Problem 13: Determinant by Elimination

## 1. Original Problem
Compute the determinant
$$A=\begin{pmatrix}1&2&3\\2&5&7\\1&0&2\end{pmatrix}$$
using elimination. Record the effect of every row operation used on the value of the determinant.

## 2. What We Are Trying to Find
We must compute the determinant of matrix $A$ by using Gaussian elimination to reduce it to upper-triangular form, explicitly recording how each elementary row operation influences the determinant.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Elementary Row Operations and Determinants**:
  - $R_i \leftarrow R_i + c R_j$ ($i \neq j$): Determinant is **unchanged** (factor $1$).
  - $R_i \leftrightarrow R_j$: Determinant is **negated** (factor $-1$).
  - $R_i \leftarrow c R_i$ ($c \neq 0$): Determinant is **scaled by $c$**.
- **Determinant of Upper-Triangular Matrix**: Once reduced, the determinant is the product of the diagonal pivots.

## 4. Step-by-Step Solution

### Initial Matrix
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \end{pmatrix}.$$
Let $D_0 = \det A$.

### Step 1: Eliminate Entries in Column 1
- **Operation 1**: $R_2 \leftarrow R_2 - 2R_1$.
  Computation: $(2, 5, 7) - 2(1, 2, 3) = (2-2, 5-4, 7-6) = (0, 1, 1)$.
  *Effect on determinant*: Adding a multiple of row 1 to row 2 **does not change the determinant**.
- **Operation 2**: $R_3 \leftarrow R_3 - R_1$.
  Computation: $(1, 0, 2) - (1, 2, 3) = (1-1, 0-2, 2-3) = (0, -2, -1)$.
  *Effect on determinant*: Adding a multiple of row 1 to row 3 **does not change the determinant**.

The matrix is now:
$$A_1 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & -2 & -1 \end{pmatrix}, \qquad \det A = \det A_1.$$

### Step 2: Eliminate Entry in Column 2 Below Pivot
- **Operation 3**: $R_3 \leftarrow R_3 + 2R_2$.
  Computation: $(0, -2, -1) + 2(0, 1, 1) = (0, -2+2, -1+2) = (0, 0, 1)$.
  *Effect on determinant*: Adding a multiple of row 2 to row 3 **does not change the determinant**.

The matrix is now in upper-triangular form:
$$U = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}, \qquad \det A = \det U.$$

### Step 3: Compute the Determinant of the Triangular Matrix
The matrix $U$ is upper-triangular with diagonal entries $u_{11} = 1$, $u_{22} = 1$, and $u_{33} = 1$.
$$\det U = 1 \cdot 1 \cdot 1 = 1.$$
Since all row operations preserved the determinant:
$$\det A = \det U = 1.$$

## 5. Why Each Step Is Valid
- All three row operations performed are row replacements of the form $R_i \leftarrow R_i + c R_j$.
- In the geometric interpretation, each operation is a shear transformation, which preserves orientation and $n$-dimensional volume exactly.
- The determinant of an upper-triangular matrix is the product of its diagonal entries.

## 6. Final Answer in Words
The determinant of matrix $A$ is $1$. The three row operations $R_2 \leftarrow R_2 - 2R_1$, $R_3 \leftarrow R_3 - R_1$, and $R_3 \leftarrow R_3 + 2R_2$ each preserved the determinant value without change, reducing $A$ to an upper-triangular matrix with ones on the main diagonal, whose product is $1$.

## 7. Quick Verification
- Verify using Sarrus' rule:
  Main diagonals: $1(5)(2) + 2(7)(1) + 3(2)(0) = 10 + 14 + 0 = 24$.
  Anti-diagonals: $3(5)(1) + 1(7)(0) + 2(2)(2) = 15 + 0 + 8 = 23$.
  $\det A = 24 - 23 = 1$.
  Both methods produce exactly $1$.

## 8. Common Mistakes
- Arithmetic errors in row operations (such as computing $-1 + 2(1) = 1$ incorrectly).
- Unnecessarily dividing rows by constants to get leading ones, which would scale the determinant and introduce fraction arithmetic.

## 9. Short In-Class Explanation (3 Sentences)
We use Gaussian elimination to reduce the matrix to upper-triangular form by clearing the entries below the diagonal. Each step is a row replacement of the type $R_i \leftarrow R_i + cR_j$, which leaves the determinant completely unchanged. The resulting matrix has diagonal entries $1, 1, 1$, so multiplying them gives a final determinant of $1$.
