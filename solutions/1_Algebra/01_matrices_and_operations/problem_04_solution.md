# Problem 04: Matrix Multiplication and Noncommutativity

## 1. Original Problem
For
$$A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\3&1\end{pmatrix}$$
compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## 2. What We Are Trying to Find
We need to calculate both matrix products $AB$ and $BA$, compare their numerical values, determine whether they commute, and explain the concept of noncommutativity in linear algebra.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Row-Column Product Rule**: For $2 \times 2$ matrices, the $(i,j)$ entry of the product is the dot product of row $i$ of the left matrix and column $j$ of the right matrix:
  $$(MN)_{ij} = \sum_{k=1}^2 m_{ik} n_{kj}.$$
- **Noncommutativity**: Unlike ordinary numbers where $ab = ba$, matrix multiplication is generally non-commutative ($AB \neq BA$). Changing the order changes which rows interact with which columns.

## 4. Step-by-Step Solution

### Step 1: Compute $AB$
Multiply rows of $A$ by columns of $B$:
$$AB = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}$$
- Top-left entry $(1,1)$: $1 \cdot 2 + 2 \cdot 3 = 2 + 6 = 8$.
- Top-right entry $(1,2)$: $1 \cdot 0 + 2 \cdot 1 = 0 + 2 = 2$.
- Bottom-left entry $(2,1)$: $0 \cdot 2 + 1 \cdot 3 = 0 + 3 = 3$.
- Bottom-right entry $(2,2)$: $0 \cdot 0 + 1 \cdot 1 = 0 + 1 = 1$.
Thus:
$$AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}.$$

### Step 2: Compute $BA$
Multiply rows of $B$ by columns of $A$:
$$BA = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$$
- Top-left entry $(1,1)$: $2 \cdot 1 + 0 \cdot 0 = 2 + 0 = 2$.
- Top-right entry $(1,2)$: $2 \cdot 2 + 0 \cdot 1 = 4 + 0 = 4$.
- Bottom-left entry $(2,1)$: $3 \cdot 1 + 1 \cdot 0 = 3 + 0 = 3$.
- Bottom-right entry $(2,2)$: $3 \cdot 2 + 1 \cdot 1 = 6 + 1 = 7$.
Thus:
$$BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}.$$

### Step 3: Compare $AB$ and $BA$
Clearly,
$$\begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} \neq \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}.$$
Therefore, $AB \neq BA$.

### Step 4: Explanation of Noncommutativity
Noncommutativity means that the order of factors in matrix multiplication fundamentally alters the outcome. Geometrically, matrices represent transformations applied to vectors; applying transformation $B$ first followed by $A$ generally does not produce the same geometric result as applying $A$ first followed by $B$.

## 5. Why Each Step Is Valid
- Matrix multiplication by definition pairs row $i$ of the left matrix with column $j$ of the right matrix.
- When the order is reversed, row $i$ of $B$ is paired with column $j$ of $A$, resulting in completely different arithmetic products and sums.

## 6. Final Answer in Words
The product $AB$ is $\begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}$ and $BA$ is $\begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}$. Since the two matrices are unequal, $AB \neq BA$. This demonstrates that matrix multiplication is non-commutative: the order in which operations are composed matters.

## 7. Quick Verification
- Check determinants:
  $\det(A) = 1 \cdot 1 - 2 \cdot 0 = 1$.
  $\det(B) = 2 \cdot 1 - 0 \cdot 3 = 2$.
  By product rule for determinants: $\det(AB) = \det(A)\det(B) = 1 \cdot 2 = 2$.
  Check calculated $\det(AB) = 8 \cdot 1 - 2 \cdot 3 = 8 - 6 = 2$.
  Check calculated $\det(BA) = 2 \cdot 7 - 4 \cdot 3 = 14 - 12 = 2$.
  Both determinants equal 2, confirming the arithmetic in both products.

## 8. Common Mistakes
- Multiplying entrywise like addition (e.g., mistakenly computing $AB$ as $\begin{pmatrix} 1\cdot 2 & 2\cdot 0 \\ 0\cdot 3 & 1\cdot 1 \end{pmatrix}$).
- Assuming that because both matrices are square and of the same size, they must commute.

## 9. Short In-Class Explanation (3 Sentences)
We compute $AB$ by multiplying rows of $A$ by columns of $B$ to get $\begin{pmatrix}8&2\\3&1\end{pmatrix}$, and $BA$ by reversing the factors to get $\begin{pmatrix}2&4\\3&7\end{pmatrix}$. Because these resulting matrices are completely different, $AB \neq BA$. This shows that matrix multiplication is non-commutative, meaning the order of operations cannot be swapped.
