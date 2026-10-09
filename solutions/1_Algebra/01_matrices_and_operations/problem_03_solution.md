# Problem 03: When Can Matrices Be Multiplied?

## 1. Original Problem
The matrix sizes are:
$$A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.$$
For the products:
$$AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA$$
determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## 2. What We Are Trying to Find
We must test eight ordered pairs of matrices against the dimension compatibility rule for matrix multiplication to determine which products exist and what the dimensions of each valid product matrix are.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Matrix Multiplication Compatibility Condition**: The matrix product $M \cdot N$ is defined if and only if the number of columns in the left matrix $M$ equals the number of rows in the right matrix $N$.
- **Resulting Dimension Rule**: If $M$ is of size $m \times k$ and $N$ is of size $k \times p$, then their product $MN$ is defined and has size $m \times p$. The inner dimensions must match ($k = k$), and the outer dimensions determine the result ($m \times p$).

## 4. Step-by-Step Solution

1. **Product $AB$**:
   - Sizes: $A_{2\times3}$ and $B_{3\times4}$.
   - Inner dimensions: columns of $A = 3$, rows of $B = 3$. They match ($3 = 3$).
   - **Defined**: Yes, size is $2 \times 4$.

2. **Product $BA$**:
   - Sizes: $B_{3\times4}$ and $A_{2\times3}$.
   - Inner dimensions: columns of $B = 4$, rows of $A = 2$. $4 \neq 2$.
   - **Defined**: No, undefined.

3. **Product $BC$**:
   - Sizes: $B_{3\times4}$ and $C_{4\times2}$.
   - Inner dimensions: columns of $B = 4$, rows of $C = 4$. They match ($4 = 4$).
   - **Defined**: Yes, size is $3 \times 2$.

4. **Product $CB$**:
   - Sizes: $C_{4\times2}$ and $B_{3\times4}$.
   - Inner dimensions: columns of $C = 2$, rows of $B = 3$. $2 \neq 3$.
   - **Defined**: No, undefined.

5. **Product $AC$**:
   - Sizes: $A_{2\times3}$ and $C_{4\times2}$.
   - Inner dimensions: columns of $A = 3$, rows of $C = 4$. $3 \neq 4$.
   - **Defined**: No, undefined.

6. **Product $CA$**:
   - Sizes: $C_{4\times2}$ and $A_{2\times3}$.
   - Inner dimensions: columns of $C = 2$, rows of $A = 2$. They match ($2 = 2$).
   - **Defined**: Yes, size is $4 \times 3$.

7. **Product $AD$**:
   - Sizes: $A_{2\times3}$ and $D_{2\times2}$.
   - Inner dimensions: columns of $A = 3$, rows of $D = 2$. $3 \neq 2$.
   - **Defined**: No, undefined.

8. **Product $DA$**:
   - Sizes: $D_{2\times2}$ and $A_{2\times3}$.
   - Inner dimensions: columns of $D = 2$, rows of $A = 2$. They match ($2 = 2$).
   - **Defined**: Yes, size is $2 \times 3$.

## 5. Why Each Step Is Valid
- Matrix multiplication computes dot products of rows of the left matrix with columns of the right matrix; a dot product of two vectors is valid if and only if both vectors have the exact same number of entries.
- The number of entries in a row of the left matrix is its column count, and the number of entries in a column of the right matrix is its row count; equality of these counts is strictly required.

## 6. Final Answer in Words
The defined products are:
- $AB$ (size $2 \times 4$),
- $BC$ (size $3 \times 2$),
- $CA$ (size $4 \times 3$),
- $DA$ (size $2 \times 3$).
The products $BA$, $CB$, $AC$, and $AD$ are undefined because the number of columns of the first matrix does not match the number of rows of the second.

## 7. Quick Verification
- Check outer and inner dimensions:
  - $(2\times3)(3\times4) \to 2\times4$ (inner 3 matches).
  - $(3\times4)(4\times2) \to 3\times2$ (inner 4 matches).
  - $(4\times2)(2\times3) \to 4\times3$ (inner 2 matches).
  - $(2\times2)(2\times3) \to 2\times3$ (inner 2 matches).
- Any attempt to pair rows and columns in the undefined products leaves leftover entries with no pair.

## 8. Common Mistakes
- Assuming that if $AB$ is defined, then $BA$ must also be defined (matrix multiplication is not commutative, nor symmetric in existence).
- Checking whether outer dimensions match instead of inner dimensions.

## 9. Short In-Class Explanation (3 Sentences)
Two matrices can be multiplied only when the number of columns in the first equals the number of rows in the second, because each row must dot-product with each column. The resulting matrix inherits its row count from the first matrix and its column count from the second. Out of the eight combinations, only $AB$, $BC$, $CA$, and $DA$ satisfy this inner dimension condition.
