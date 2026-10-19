# Problem 14: A Matrix That Is Its Own Inverse

## 1. Original Problem
Assume that a square matrix $A$ satisfies
$$A^2=I.$$
Show that
$$A^{-1}=A.$$
Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

## 2. What We Are Trying to Find
We must prove algebraically that any square matrix satisfying $A^2 = I$ (an involution) is its own inverse ($A^{-1} = A$), construct an explicit non-trivial $2 \times 2$ example other than $\pm I$, and verify it by computing its square.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Definition of Inversion**: For a square matrix $A$, if there exists a matrix $B$ such that $AB = I$ and $BA = I$, then $B$ is uniquely defined as $A^{-1}$.
- **Involutory Matrix**: A matrix satisfying $A^2 = I$ is called an involution. A reflection is one example of an involution: applying it twice across the same line returns every point to its original position. Not every involution is a Euclidean reflection.

## 4. Step-by-Step Solution

### Step 1: Show That $A^{-1} = A$
We are given that:
$$A^2 = I \iff A \cdot A = I.$$
1. Because $A \cdot A = I$, the product of $A$ with itself is the identity matrix.
2. By the uniqueness of the matrix inverse, if a matrix $B$ satisfies $A B = I$ and $B A = I$, then $B = A^{-1}$.
3. Here, setting $B = A$ satisfies:
   $$A(A) = I \quad \text{and} \quad (A)A = I.$$
4. Therefore:
   $$A^{-1} = A.$$

### Step 2: Construct a Non-Trivial $2 \times 2$ Example
We seek a matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \neq \pm I$ such that $A^2 = I$.
Consider a geometric reflection across the line $y = x$:
It maps $(x, y) \mapsto (y, x)$.
The matrix representing this reflection is:
$$A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}.$$
(Another valid example is reflection across the $x$-axis: $\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$).
Clearly, $A \neq I$ and $A \neq -I$.

### Step 3: Verify the Example by Multiplication
Compute $A^2 = A \cdot A$:
$$A^2 = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 0(0)+1(1) & 0(1)+1(0) \\ 1(0)+0(1) & 1(1)+0(0) \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I.$$
Since $A^2 = I$, its inverse is $A^{-1} = A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$.

## 5. Why Each Step Is Valid
- The equality $A \cdot A = I$ directly satisfies the defining axiom of the inverse matrix without requiring intermediate steps.
- The reflection matrix $\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$ swaps coordinates, and swapping coordinates twice is the identity mapping on $\mathbb{R}^2$.

## 6. Final Answer in Words
If $A^2 = I$, then $A$ multiplied by itself is $I$, which means $A$ satisfies the definition of the inverse matrix, so $A^{-1} = A$. A concrete example different from $\pm I$ is the coordinate swap matrix $A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$. Multiplying this matrix by itself yields $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$, verifying that it is its own inverse.

## 7. Quick Verification
- Check determinant: $\det A = 0(0) - 1(1) = -1$.
  Using the $2 \times 2$ formula:
  $$A^{-1} = \frac{1}{-1} \begin{pmatrix} 0 & -1 \\ -1 & 0 \end{pmatrix} = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} = A.$$
  Confirms $A^{-1} = A$.

## 8. Common Mistakes
- Giving $I$ or $-I$ as the example, ignoring the explicit instruction to provide an example different from $\pm I$.
- Concluding that $A^2 = I$ implies $A = \pm I$ (which is true for numbers, but false for matrices!).

## 9. Short In-Class Explanation (3 Sentences)
From the equation $A \cdot A = I$, the matrix $A$ directly satisfies the definition of the inverse matrix, proving immediately that $A^{-1} = A$. Unlike numbers where $x^2 = 1$ only gives $\pm 1$, matrices have many self-inverting solutions. A reflection is one example of an involution. The permutation matrix $\begin{pmatrix}0&1\\1&0\end{pmatrix}$ swaps coordinates, and squaring it produces the identity matrix, confirming it is its own inverse.
