# Problem 04: Triangular Matrix

## 1. Original Problem
Without expanding the determinant, compute
$$\det\begin{pmatrix}2&4&1\\0&-3&5\\0&0&7\end{pmatrix}.$$
State the rule for an arbitrary triangular matrix and explain it using this example.

## 2. What We Are Trying to Find
We must evaluate the determinant of a $3 \times 3$ upper-triangular matrix without performing a standard expansion, formulate the general theorem for triangular matrices, and explain why the theorem holds.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Triangular Matrix Determinant Theorem**: If $T = (t_{ij})$ is an upper-triangular, lower-triangular, or diagonal $n \times n$ matrix, its determinant is simply the product of all entries along the main diagonal:
  $$\det T = \prod_{i=1}^n t_{ii} = t_{11} t_{22} \dots t_{nn}.$$
- **Why this holds**: In every term of the Leibniz formula except the main diagonal product, at least one factor comes from the strictly lower (or upper) triangular part where the entries are zero.

## 4. Step-by-Step Solution

### Step 1: Identify the Structure of the Matrix
The given matrix is:
$$T = \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}.$$
All entries below the main diagonal ($t_{21} = 0, t_{31} = 0, t_{32} = 0$) are zero. Therefore, $T$ is an upper-triangular matrix.

### Step 2: Apply the Diagonal Product Rule
The main diagonal entries are $t_{11} = 2$, $t_{22} = -3$, and $t_{33} = 7$.
Multiply them together:
$$\det T = 2 \cdot (-3) \cdot 7 = -6 \cdot 7 = -42.$$

### Step 3: Explain the Rule Using This Example
Consider performing Laplace expansion successively down the first column:
1. Column 1 has non-zero entry only at the top: $t_{11} = 2$.
   Expanding along Column 1:
   $$\det T = 2 \cdot \det\begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} - 0 \cdot M_{21} + 0 \cdot M_{31} = 2 \cdot \det\begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix}.$$
2. The remaining $2 \times 2$ matrix is also upper-triangular. Expanding along its first column gives:
   $$\det\begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} = -3 \cdot 7 - 5 \cdot 0 = (-3) \cdot 7.$$
3. Combining them:
   $$\det T = 2 \cdot (-3) \cdot 7 = -42.$$
At every step of cofactor expansion, the zeros eliminate all terms except the diagonal entry times the remaining submatrix, cascading directly into the product of the diagonal elements.

## 5. Why Each Step Is Valid
- The zero entries below the diagonal guarantee that in column expansion, all minors except the first are multiplied by zero.
- This recursive property applies universally to any triangular matrix of any dimension $n$.

## 6. Final Answer in Words
The determinant is $-42$. For any triangular matrix, the determinant is the product of its main diagonal entries. Here, multiplying the diagonal entries $2$, $-3$, and $7$ gives $-42$, because expanding along the columns with zeros systematically eliminates all other terms.

## 7. Quick Verification
- Compute by Sarrus' rule:
  Main diagonals: $2(-3)(7) + 4(5)(0) + 1(0)(0) = -42 + 0 + 0 = -42$.
  Anti-diagonals: $1(-3)(0) + 2(5)(0) + 4(0)(7) = 0 + 0 + 0 = 0$.
  $\det T = -42 - 0 = -42$.
  Confirms the diagonal product rule.

## 8. Common Mistakes
- Unnecessarily carrying out a full Sarrus expansion and risking arithmetic mistakes when the triangular structure provides the answer immediately.
- Forgetting negative signs when multiplying diagonal entries: $2 \cdot (-3) \cdot 7 = -42$, not $42$.

## 9. Short In-Class Explanation (3 Sentences)
Because all entries below the main diagonal are zero, this is an upper-triangular matrix. The determinant of any triangular matrix is simply the product of its diagonal entries, which gives $2 \times (-3) \times 7 = -42$. This rule works because expanding column by column eliminates every other term due to the zeros.
