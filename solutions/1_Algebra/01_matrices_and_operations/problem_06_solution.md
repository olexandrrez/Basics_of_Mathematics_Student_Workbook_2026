# Problem 06: Transpose

## 1. Original Problem
For
$$A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}$$
compute $A^T$, $B^T$, and $AB$. Then verify in this example that
$$(AB)^T=B^TA^T.$$

## 2. What We Are Trying to Find
We need to transpose matrices $A$ (size $2 \times 3$) and $B$ (size $3 \times 2$), compute the product $AB$, compute the transpose $(AB)^T$, compute the product in reverse transposed order $B^T A^T$, and verify that $(AB)^T = B^T A^T$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Matrix Transpose**: The transpose of an $m \times n$ matrix $M = (m_{ij})$ is the $n \times m$ matrix $M^T = (m_{ji})$ obtained by swapping rows and columns.
- **Transpose of a Product Property**: For any two matrices that can be multiplied, $(MN)^T = N^T M^T$. The order of factors reverses because transposing exchanges rows and columns, turning left-row $\times$ right-column into right-column $\times$ left-row.

## 4. Step-by-Step Solution

### Step 1: Compute $A^T$ and $B^T$
- $A$ is $2 \times 3$: its rows become columns of $A^T$ (size $3 \times 2$):
  $$A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}.$$
- $B$ is $3 \times 2$: its rows become columns of $B^T$ (size $2 \times 3$):
  $$B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}.$$

### Step 2: Compute $AB$
$A$ is $2 \times 3$ and $B$ is $3 \times 2$, so $AB$ is $2 \times 2$:
$$AB = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}$$
- Row 1, Col 1: $1(1) + 2(2) + 3(-1) = 1 + 4 - 3 = 2$.
- Row 1, Col 2: $1(0) + 2(1) + 3(3) = 0 + 2 + 9 = 11$.
- Row 2, Col 1: $4(1) + 5(2) + 6(-1) = 4 + 10 - 6 = 8$.
- Row 2, Col 2: $4(0) + 5(1) + 6(3) = 0 + 5 + 18 = 23$.
Thus:
$$AB = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}.$$

### Step 3: Compute $(AB)^T$
Transpose the $2 \times 2$ product $AB$:
$$(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}.$$

### Step 4: Compute $B^T A^T$
Multiply $B^T$ ($2 \times 3$) by $A^T$ ($3 \times 2$):
$$B^T A^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}$$
- Row 1, Col 1: $1(1) + 2(2) + (-1)(3) = 1 + 4 - 3 = 2$.
- Row 1, Col 2: $1(4) + 2(5) + (-1)(6) = 4 + 10 - 6 = 8$.
- Row 2, Col 1: $0(1) + 1(2) + 3(3) = 0 + 2 + 9 = 11$.
- Row 2, Col 2: $0(4) + 1(5) + 3(6) = 0 + 5 + 18 = 23$.
Thus:
$$B^T A^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}.$$

Comparing the two matrices, $(AB)^T = B^T A^T$ holds identically.

## 5. Why Each Step Is Valid
- Transposition reflects matrix elements across the main diagonal, converting row vectors into column vectors.
- In $AB$, entry $(i, j)$ is the dot product of row $i$ of $A$ and column $j$ of $B$. In $(AB)^T$, this becomes entry $(j, i)$.
- In $B^T A^T$, entry $(j, i)$ is the dot product of row $j$ of $B^T$ (which is column $j$ of $B$) and column $i$ of $A^T$ (which is row $i$ of $A$), which gives the identical dot product value.

## 6. Final Answer in Words
The transposes are $A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}$ and $B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}$. The product is $AB = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}$, whose transpose is $(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$. Multiplying $B^T A^T$ gives the exact same matrix $\begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$, confirming that $(AB)^T = B^T A^T$.

## 7. Quick Verification
- Checking dimensions: $A^T$ is $3 \times 2$ and $B^T$ is $2 \times 3$. If we tried computing $A^T B^T$, the dimensions $(3 \times 2)(2 \times 3)$ would give a $3 \times 3$ matrix, which cannot equal the $2 \times 2$ matrix $(AB)^T$. This proves that the reversed order $B^T A^T$ is the only dimensionally compatible choice.

## 8. Common Mistakes
- Writing $(AB)^T = A^T B^T$ without reversing the factors, which often results in dimension mismatch or incorrect entries.
- Transposing only the diagonal elements and forgetting to swap off-diagonal elements.

## 9. Short In-Class Explanation (3 Sentences)
We compute $A^T$ and $B^T$ by swapping rows with columns, turning a $2 \times 3$ matrix into a $3 \times 2$ matrix and vice versa. Calculating $AB$ gives a $2 \times 2$ matrix whose transpose has rows and columns flipped. When we compute $B^T A^T$, the order of multiplication reverses, and we get the exact same matrix, verifying the identity $(AB)^T = B^T A^T$.
