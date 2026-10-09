# Problem 09: Matrix Equation

## 1. Original Problem
Given
$$A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}3&1\\2&4\end{pmatrix}.$$
Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

## 2. What We Are Trying to Find
We must determine the unknown $2 \times 2$ matrix $X$ satisfying the matrix equation $AX = B$ by identifying which side to multiply by $A^{-1}$, computing $A^{-1}$, finding $X$, and verifying that $AX = B$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Side of Multiplication**: Because matrix multiplication is non-commutative ($MN \neq NM$), multiplying an equation by an inverse must be done on the same side for both sides of the equation.
  - To cancel $A$ on the left of $AX$, we must multiply by $A^{-1}$ on the **left**:
    $$A^{-1}(AX) = A^{-1} B \implies (A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B.$$
  - Multiplying on the right would give $(AX)A^{-1} = B A^{-1}$, which does not isolate $X$.

## 4. Step-by-Step Solution

### Step 1: Decide on the Side for $A^{-1}$
In the equation $AX = B$, matrix $A$ appears on the left of the unknown $X$. To eliminate $A$, we must multiply by $A^{-1}$ on the **left**.
Formula:
$$X = A^{-1} B.$$

### Step 2: Compute $A^{-1}$
For $A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$:
$$\det A = (1)(1) - (2)(0) = 1.$$
Using the $2 \times 2$ inverse formula:
$$A^{-1} = \frac{1}{1} \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix}.$$

### Step 3: Compute $X = A^{-1} B$
Multiply $A^{-1}$ by $B = \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix}$:
$$X = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix}$$
- Top-left entry: $1(3) + (-2)(2) = 3 - 4 = -1$.
- Top-right entry: $1(1) + (-2)(4) = 1 - 8 = -7$.
- Bottom-left entry: $0(3) + 1(2) = 0 + 2 = 2$.
- Bottom-right entry: $0(1) + 1(4) = 0 + 4 = 4$.
Thus:
$$X = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}.$$

### Step 4: Verification by Computing $AX$
Multiply $A$ by the computed matrix $X$:
$$AX = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}$$
- Top-left: $1(-1) + 2(2) = -1 + 4 = 3$.
- Top-right: $1(-7) + 2(4) = -7 + 8 = 1$.
- Bottom-left: $0(-1) + 1(2) = 0 + 2 = 2$.
- Bottom-right: $0(-7) + 1(4) = 0 + 4 = 4$.
Thus:
$$AX = \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix} = B.$$
The product reproduces $B$ perfectly.

## 5. Why Each Step Is Valid
- The existence of $A^{-1}$ is guaranteed by $\det A = 1 \neq 0$.
- Left-multiplication preserves matrix equality and utilizes associativity $(A^{-1}A)X = IX = X$.

## 6. Final Answer in Words
We must multiply on the left by $A^{-1}$, yielding $X = A^{-1}B$. The inverse is $A^{-1} = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix}$, and the solution matrix is $X = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}$. Computing $AX$ reproduces $B$, verifying the solution.

## 7. Quick Verification
- What if we mistakenly multiplied on the right ($B A^{-1}$)?
  $$B A^{-1} = \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix} \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 3 & -5 \\ 2 & 0 \end{pmatrix} \neq X.$$
  Multiplying $A(B A^{-1}) = \begin{pmatrix} 7 & -5 \\ 2 & 0 \end{pmatrix} \neq B$. This confirms that left multiplication is the only correct choice.

## 8. Common Mistakes
- Multiplying $A^{-1}$ on the right, confusing $A^{-1}B$ with $B A^{-1}$.
- Incorrect sign in the inverse: writing $\begin{pmatrix}1&2\\0&1\end{pmatrix}$ instead of $\begin{pmatrix}1&-2\\0&1\end{pmatrix}$.

## 9. Short In-Class Explanation (3 Sentences)
To isolate $X$ in the equation $AX = B$, we must multiply by $A^{-1}$ on the left because matrix multiplication is non-commutative. Computing the inverse gives $A^{-1} = \begin{pmatrix}1&-2\\0&1\end{pmatrix}$, and multiplying it by $B$ on the left yields $X = \begin{pmatrix}-1&-7\\2&4\end{pmatrix}$. Multiplying $A$ by our resulting matrix $X$ reproduces $B$, confirming the solution.
