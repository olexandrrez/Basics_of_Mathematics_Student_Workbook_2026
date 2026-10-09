# Problem 05: Row Operations

## 1. Original Problem
For
$$A=\begin{pmatrix}1&2&3\\2&1&0\\-1&4&2\end{pmatrix}$$
find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## 2. What We Are Trying to Find
We need to reduce matrix $A$ to an upper-triangular form using elementary row operations, track the effect of each operation on the value of the determinant, and compute $\det A$ from the resulting simplified matrix.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Row Operations and Determinants**:
  1. Adding a multiple of one row to another row ($R_i \leftarrow R_i + c R_j$ with $i \neq j$): **leaves the determinant completely unchanged**.
  2. Interchanging two rows ($R_i \leftrightarrow R_j$): **multiplies the determinant by $-1$**.
  3. Scaling a row by a non-zero scalar ($R_i \leftarrow c R_i$): **multiplies the determinant by $c$**.
- By using only type-1 operations (adding multiples of rows), the determinant remains strictly invariant throughout the reduction.

## 4. Step-by-Step Solution

### Initial Matrix
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}.$$
Let $D = \det A$.

### Step 1: Eliminate Below Pivot in Column 1
- **Operation 1**: $R_2 \leftarrow R_2 - 2R_1$.
  Effect on determinant: **No change** (adding a multiple of row 1 to row 2 preserves the determinant).
  $$R_2 - 2R_1 = (2, 1, 0) - 2(1, 2, 3) = (2-2, 1-4, 0-6) = (0, -3, -6).$$
- **Operation 2**: $R_3 \leftarrow R_3 + R_1$.
  Effect on determinant: **No change** (adding row 1 to row 3 preserves the determinant).
  $$R_3 + R_1 = (-1, 4, 2) + (1, 2, 3) = (-1+1, 4+2, 2+3) = (0, 6, 5).$$
The matrix is now:
$$A_1 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}, \qquad \det A = \det A_1.$$

### Step 2: Eliminate Below Pivot in Column 2
- **Operation 3**: $R_3 \leftarrow R_3 + 2R_2$.
  Effect on determinant: **No change** (adding $2$ times row 2 to row 3 preserves the determinant).
  $$R_3 + 2R_2 = (0, 6, 5) + 2(0, -3, -6) = (0, 6-6, 5-12) = (0, 0, -7).$$
The matrix is now in upper-triangular form:
$$A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{pmatrix}, \qquad \det A = \det A_2.$$

### Step 3: Compute the Determinant of the Triangular Matrix
Since $A_2$ is upper-triangular, its determinant is the product of its diagonal entries:
$$\det A_2 = 1 \cdot (-3) \cdot (-7) = 21.$$
Since none of our row operations changed the value of the determinant:
$$\det A = \det A_2 = 21.$$

## 5. Why Each Step Is Valid
- Adding a scalar multiple of row $j$ to row $i$ represents shear of the coordinate volume spanned by the rows; shear transformations preserve hyper-volume and orientation.
- The product of diagonal entries of an upper-triangular matrix evaluates its determinant identically.

## 6. Final Answer in Words
The determinant of $A$ is $21$. By applying row operations of the type $R_i \leftarrow R_i + cR_j$, the value of the determinant remained unchanged at every stage, reducing $A$ to an upper-triangular matrix with diagonal entries $1$, $-3$, and $-7$, whose product is $21$.

## 7. Quick Verification
- Compute $\det A$ directly using Sarrus' rule:
  Main diagonals: $1(1)(2) + 2(0)(-1) + 3(2)(4) = 2 + 0 + 24 = 26$.
  Anti-diagonals: $3(1)(-1) + 1(0)(4) + 2(2)(2) = -3 + 0 + 8 = 5$.
  $\det A = 26 - 5 = 21$.
  Both methods produce exactly $21$.

## 8. Common Mistakes
- Mistakenly changing the sign of the determinant during row replacement ($R_i \leftarrow R_i - cR_j$ does NOT change the sign; only row swaps $R_i \leftrightarrow R_j$ flip the sign).
- Arithmetic sign errors: $(-3) \cdot (-7) = +21$, not $-21$.

## 9. Short In-Class Explanation (3 Sentences)
We simplify the matrix using row additions to create zeros in the lower triangle: first eliminating the entries in the first column, then eliminating below the pivot in the second column. Because adding multiples of one row to another does not change the determinant, the determinant of the original matrix equals the determinant of the resulting triangular matrix. Multiplying the diagonal entries $1 \times (-3) \times (-7)$ gives the final answer $21$.
