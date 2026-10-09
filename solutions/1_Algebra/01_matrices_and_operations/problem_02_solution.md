# Problem 02: Addition and Scalar Multiplication

## 1. Original Problem
For
$$A=\begin{pmatrix}1&2\\-1&3\end{pmatrix},\qquad B=\begin{pmatrix}4&-2\\0&5\end{pmatrix}$$
compute
$$A+B,\qquad A-B,\qquad 3A-2B.$$
Explain why matrix addition is possible only for matrices of the same size.

## 2. What We Are Trying to Find
We need to perform entry-by-entry addition, subtraction, and a linear combination of two $2 \times 2$ matrices, and explain the theoretical requirement for dimension matching.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Entrywise Operations**: Matrix addition and scalar multiplication are defined entrywise. For matrices $A = (a_{ij})$ and $B = (b_{ij})$ of the same size $m \times n$, the sum is $(A+B)_{ij} = a_{ij} + b_{ij}$, and scalar multiplication by $c \in \mathbb{R}$ is $(cA)_{ij} = c \cdot a_{ij}$.
- **Dimension Compatibility**: For the sum $a_{ij} + b_{ij}$ to exist for all pairs $(i, j)$, every entry in $A$ must correspond to exactly one entry in $B$ at the same position.

## 4. Step-by-Step Solution

### Step 1: Compute $A + B$
Add corresponding entries:
$$A+B = \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}.$$

### Step 2: Compute $A - B$
Subtract corresponding entries:
$$A-B = \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}.$$

### Step 3: Compute $3A - 2B$
First scale each matrix:
$$3A = 3\begin{pmatrix}1&2\\-1&3\end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix},$$
$$2B = 2\begin{pmatrix}4&-2\\0&5\end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}.$$
Now subtract the scaled matrices:
$$3A - 2B = \begin{pmatrix} 3-8 & 6-(-4) \\ -3-0 & 9-10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}.$$

### Step 4: Explain Why Matrices Must Have the Same Size
Matrix addition is defined componentwise: each position $(i,j)$ in the resulting matrix requires adding the entry $a_{ij}$ from $A$ to the entry $b_{ij}$ from $B$. If the matrices had different dimensions, at least one entry would have no corresponding partner to add to, leaving the operation undefined.

## 5. Why Each Step Is Valid
- Entrywise addition and scalar scaling are valid because matrices of identical dimensions form a real vector space under these operations.
- Distributing scalars to every entry obeys the distributive property of scalar-matrix multiplication.

## 6. Final Answer in Words
The sum is $A+B = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$, the difference is $A-B = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}$, and the linear combination is $3A-2B = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}$. Addition requires identical dimensions because every entry $a_{ij}$ must have a uniquely positioned counterpart $b_{ij}$.

## 7. Quick Verification
- Check $(A+B) + (A-B) = 2A$:
  $$\begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix} + \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ -2 & 6 \end{pmatrix} = 2\begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = 2A.$$
  This perfectly confirms both calculations.

## 8. Common Mistakes
- Sign errors when subtracting negative numbers, like writing $2 - (-2) = 0$ instead of $4$.
- Scaling only the first row or column by a scalar instead of multiplying all entries.
- Attempting to add matrices of different shapes by padding with zeros without explicit mathematical justification.

## 9. Short In-Class Explanation (3 Sentences)
Matrix addition and scalar multiplication work strictly entry by entry on matching positions. Both matrices must have the same size so that every entry has a well-defined partner to add or subtract. By combining entrywise scaling and subtraction, we find $3A - 2B = \begin{pmatrix}-5 & 10 \\ -3 & -1\end{pmatrix}$.
