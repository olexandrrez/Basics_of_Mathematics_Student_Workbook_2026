# Problem 02: Determinant of a 3×3 Matrix

## 1. Original Problem
For
$$A=\begin{pmatrix}1&2&-1\\0&3&4\\2&1&5\end{pmatrix}$$
compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

## 2. What We Are Trying to Find
We need to calculate the determinant of a $3 \times 3$ matrix using Sarrus' rule (diagonal expansion) and then verify the numerical result independently using cofactor expansion along a row containing a zero.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Sarrus' Rule**: For a $3 \times 3$ matrix, copy the first two columns to the right:
  $$\det A = (a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32}) - (a_{13}a_{22}a_{31} + a_{11}a_{23}a_{32} + a_{12}a_{21}a_{33}).$$
- **Laplace (Cofactor) Expansion**: Expanding along row $i$:
  $$\det A = \sum_{j=1}^3 (-1)^{i+j} a_{ij} M_{ij},$$
  where $M_{ij}$ is the $(i, j)$ minor determinant. Choosing a row with a zero entry simplifies the calculation.

## 4. Step-by-Step Solution

### Step 1: Compute $\det A$ Using Sarrus' Rule
Write out the products of the three main diagonals:
- Diagonal 1: $1 \cdot 3 \cdot 5 = 15$.
- Diagonal 2: $2 \cdot 4 \cdot 2 = 16$.
- Diagonal 3: $(-1) \cdot 0 \cdot 1 = 0$.
Sum of main diagonal products:
$$S_1 = 15 + 16 + 0 = 31.$$

Write out the products of the three anti-diagonals:
- Anti-diagonal 1: $(-1) \cdot 3 \cdot 2 = -6$.
- Anti-diagonal 2: $1 \cdot 4 \cdot 1 = 4$.
- Anti-diagonal 3: $2 \cdot 0 \cdot 5 = 0$.
Sum of anti-diagonal products:
$$S_2 = -6 + 4 + 0 = -2.$$

Subtract the anti-diagonal sum from the main diagonal sum:
$$\det A = S_1 - S_2 = 31 - (-2) = 31 + 2 = 33.$$

### Step 2: Verification via Laplace Expansion along Row 2
Row 2 is $(0, 3, 4)$, which has a zero at entry $a_{21}$:
$$\det A = -0 \cdot M_{21} + 3 \cdot M_{22} - 4 \cdot M_{23}.$$
Compute the $2 \times 2$ minors:
- Minor $M_{22}$: delete row 2, col 2:
  $$M_{22} = \det\begin{pmatrix} 1 & -1 \\ 2 & 5 \end{pmatrix} = 1(5) - (-1)(2) = 5 + 2 = 7.$$
- Minor $M_{23}$: delete row 2, col 3:
  $$M_{23} = \det\begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix} = 1(1) - 2(2) = 1 - 4 = -3.$$
Substitute the minors:
$$\det A = 3(7) - 4(-3) = 21 + 12 = 33.$$
Both methods yield exactly $33$.

## 5. Why Each Step Is Valid
- Sarrus' rule is the algebraic realization of the permutation definition of the determinant for the symmetric group $S_3$.
- Laplace cofactor expansion is a fundamental theorem of determinants valid along any row or column; expanding along row 2 reduces the problem to two $2 \times 2$ determinants due to the zero entry.

## 6. Final Answer in Words
The determinant of matrix $A$ computed by Sarrus' rule is $33$. Verification by Laplace expansion along the second row confirms that $\det A = 3(7) - 4(-3) = 33$.

## 7. Quick Verification
- Both independent methods produced $33$.
- Row operation check: $R_3 \leftarrow R_3 - 2R_1$ gives third row $(0, -3, 7)$. Expanding along column 1 gives $1 \cdot \det\begin{pmatrix}3 & 4 \\ -3 & 7\end{pmatrix} = 1(21 - (-12)) = 33$. Perfect agreement.

## 8. Common Mistakes
- Applying Sarrus' rule to $4 \times 4$ matrices (Sarrus' rule is strictly valid only for $3 \times 3$ matrices).
- Dropping the negative sign in the anti-diagonals, computing $31 + (-2) = 29$ instead of $31 - (-2) = 33$.

## 9. Short In-Class Explanation (3 Sentences)
We calculate the determinant using Sarrus' rule by summing the products along the three downward diagonals to get $31$ and subtracting the upward diagonals which sum to $-2$, giving $33$. To verify this quickly, we expand along the second row to exploit the zero entry. The cofactor expansion gives $3(7) - 4(-3) = 33$, confirming the result.
