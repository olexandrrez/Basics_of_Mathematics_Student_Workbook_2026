# Problem 15: Associativity of Multiplication and Different Calculation Paths

## 1. Original Problem
Given
$$A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\quad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix},\quad C=\begin{pmatrix}2&1\\0&-1\end{pmatrix}.$$
Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

## 2. What We Are Trying to Find
We need to evaluate the three-matrix product $ABC$ along two different parenthesization paths: first calculating $(AB)$ then multiplying by $C$, and first calculating $(BC)$ then multiplying by $A$. We compare the numerical results, count the arithmetic operations involved in each path, and interpret associativity.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Associativity of Matrix Multiplication**: For any matrices $A, B, C$ of compatible dimensions, $(AB)C = A(BC)$. The grouping of operations does not affect the final result.
- **Computational Cost**: Multiplying an $m \times k$ matrix by a $k \times p$ matrix requires $m \cdot p \cdot k$ multiplications and $m \cdot p \cdot (k - 1)$ additions. The order of parenthesization can significantly affect the total number of operations (matrix chain multiplication problem).

## 4. Step-by-Step Solution

### Step 1: Compute via Path 1: $(AB)C$
- First compute $AB$:
  $A$ is $2 \times 3$, $B$ is $3 \times 2$, so $AB$ is $2 \times 2$:
  $$AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}$$
  - Entry $(1,1)$: $1(1) + 2(2) + 0(-1) = 1 + 4 + 0 = 5$.
  - Entry $(1,2)$: $1(0) + 2(1) + 0(3) = 0 + 2 + 0 = 2$.
  - Entry $(2,1)$: $0(1) + 1(2) + 1(-1) = 0 + 2 - 1 = 1$.
  - Entry $(2,2)$: $0(0) + 1(1) + 1(3) = 0 + 1 + 3 = 4$.
  $$AB = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix}.$$
  Operation count for $AB$: $2 \times 2 \times 3 = 12$ multiplications.

- Next compute $(AB)C$:
  Multiply $(AB)$ ($2 \times 2$) by $C$ ($2 \times 2$):
  $$(AB)C = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}$$
  - Entry $(1,1)$: $5(2) + 2(0) = 10$.
  - Entry $(1,2)$: $5(1) + 2(-1) = 5 - 2 = 3$.
  - Entry $(2,1)$: $1(2) + 4(0) = 2$.
  - Entry $(2,2)$: $1(1) + 4(-1) = 1 - 4 = -3$.
  $$(AB)C = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}.$$
  Operation count for $(AB)C$: $2 \times 2 \times 2 = 8$ multiplications.
  Total multiplications for Path 1: $12 + 8 = 20$.

### Step 2: Compute via Path 2: $A(BC)$
- First compute $BC$:
  $B$ is $3 \times 2$, $C$ is $2 \times 2$, so $BC$ is $3 \times 2$:
  $$BC = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}$$
  - Row 1: $(1(2)+0(0), 1(1)+0(-1)) = (2, 1)$.
  - Row 2: $(2(2)+1(0), 2(1)+1(-1)) = (4, 2-1) = (4, 1)$.
  - Row 3: $(-1(2)+3(0), -1(1)+3(-1)) = (-2, -1-3) = (-2, -4)$.
  $$BC = \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}.$$
  Operation count for $BC$: $3 \times 2 \times 2 = 12$ multiplications.

- Next compute $A(BC)$:
  Multiply $A$ ($2 \times 3$) by $(BC)$ ($3 \times 2$):
  $$A(BC) = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}$$
  - Entry $(1,1)$: $1(2) + 2(4) + 0(-2) = 2 + 8 + 0 = 10$.
  - Entry $(1,2)$: $1(1) + 2(1) + 0(-4) = 1 + 2 + 0 = 3$.
  - Entry $(2,1)$: $0(2) + 1(4) + 1(-2) = 0 + 4 - 2 = 2$.
  - Entry $(2,2)$: $0(1) + 1(1) + 1(-4) = 0 + 1 - 4 = -3$.
  $$A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}.$$
  Operation count for $A(BC)$: $2 \times 2 \times 3 = 12$ multiplications.
  Total multiplications for Path 2: $12 + 12 = 24$.

### Step 3: Comparison and Explanation
Both calculations yield the identical matrix $\begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$. This proves associativity in this example: $(AB)C = A(BC)$.
However, Path 1 required $20$ multiplications while Path 2 required $24$ multiplications. Even though both paths are mathematically equivalent, parenthesization impacts computational efficiency.

## 5. Why Each Step Is Valid
- Matrix multiplication satisfies associativity because function composition is inherently associative: $(f \circ g) \circ h = f \circ (g \circ h)$.
- Both paths respect valid inner-dimension matching at each stage.

## 6. Final Answer in Words
Both paths yield $(AB)C = A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$. Associativity means that grouping adjacent matrix products does not alter the final result. Path 1 required 20 scalar multiplications, whereas Path 2 required 24 scalar multiplications, illustrating that different grouping choices can have different computational efficiency.

## 7. Quick Verification
- Both intermediate matrices $AB = \begin{pmatrix}5&2\\1&4\end{pmatrix}$ and $BC = \begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}$ were independently multiplied to yield the exact same entries: $(10, 3)$ in Row 1 and $(2, -3)$ in Row 2.

## 8. Common Mistakes
- Permuting the matrices (e.g., swapping $B$ and $A$) rather than just moving parentheses. Associativity changes grouping, NOT order of factors.
- Assuming all paths have equal computational effort.

## 9. Short In-Class Explanation (3 Sentences)
We compute the product using both groupings $(AB)C$ and $A(BC)$ and obtain the exact same matrix $\begin{pmatrix}10&3\\2&-3\end{pmatrix}$, confirming that matrix multiplication is associative. Associativity allows us to group factors however we like without changing the outcome, although the order of matrices cannot be swapped. In this example, computing $(AB)C$ first was computationally faster, requiring fewer scalar multiplications than $A(BC)$.
