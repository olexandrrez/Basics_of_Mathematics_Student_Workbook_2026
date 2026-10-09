# Problem 04: Gauss–Jordan Elimination

## 1. Original Problem
Find $A^{-1}$ using the Gauss–Jordan method for
$$A=\begin{pmatrix}1&2\\3&5\end{pmatrix}.$$
Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

## 2. What We Are Trying to Find
We must compute the inverse of matrix $A$ by augmenting it with the $2 \times 2$ identity matrix $[A \mid I]$, applying elementary row operations to transform the left side into the identity matrix $I$, and explain the theoretical reason why the right side becomes $A^{-1}$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Gauss-Jordan Inversion Algorithm**: Set up the augmented block matrix $[A \mid I]$. Apply elementary row operations until the left block becomes the identity matrix $I$:
  $$[A \mid I] \xrightarrow{\text{row operations}} [I \mid A^{-1}].$$
- **Why this works**: Every elementary row operation corresponds to multiplying on the left by an elementary matrix $E_k$. The sequence of operations transforms $A$ into $I$:
  $$(E_m \dots E_2 E_1) A = I \implies E_m \dots E_2 E_1 = A^{-1}.$$
  Applying this same sequence of row operations to the right block $I$ produces:
  $$(E_m \dots E_2 E_1) I = A^{-1} I = A^{-1}.$$

## 4. Step-by-Step Solution

### Step 1: Set Up the Augmented Matrix
$$[A \mid I] = \left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 3 & 5 & 0 & 1 \end{array}\right].$$

### Step 2: Eliminate Below Pivot in Column 1
Perform $R_2 \leftarrow R_2 - 3R_1$:
- Left side: $(3, 5) - 3(1, 2) = (3-3, 5-6) = (0, -1)$.
- Right side: $(0, 1) - 3(1, 0) = (0-3, 1-0) = (-3, 1)$.
The augmented matrix becomes:
$$\left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & -1 & -3 & 1 \end{array}\right].$$

### Step 3: Make the Pivot in Row 2 Positive
Perform $R_2 \leftarrow -1 \cdot R_2$:
- Left side: $-(0, -1) = (0, 1)$.
- Right side: $-(-3, 1) = (3, -1)$.
The augmented matrix becomes:
$$\left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & 1 & 3 & -1 \end{array}\right].$$

### Step 4: Eliminate Above Pivot in Column 2
Perform $R_1 \leftarrow R_1 - 2R_2$:
- Left side: $(1, 2) - 2(0, 1) = (1-0, 2-2) = (1, 0)$.
- Right side: $(1, 0) - 2(3, -1) = (1-6, 0-(-2)) = (-5, 2)$.
The augmented matrix is now:
$$\left[\begin{array}{cc|cc} 1 & 0 & -5 & 2 \\ 0 & 1 & 3 & -1 \end{array}\right].$$

### Step 5: Read Off the Inverse
The left side has reached $I$. Therefore, the matrix on the right is $A^{-1}$:
$$A^{-1} = \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}.$$

## 5. Why Each Step Is Valid
- Elementary row operations are reversible and represent left-multiplication by invertible elementary matrices.
- Accumulating these transformations on $I$ records the exact matrix product that reduces $A$ to $I$, which is by definition $A^{-1}$.

## 6. Final Answer in Words
Using the Gauss-Jordan method, the inverse matrix is $A^{-1} = \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}$. Obtaining $I$ on the left guarantees that the sequence of elementary row operations applied equals the matrix $A^{-1}$, so applying those same operations to $I$ on the right produces $A^{-1}$.

## 7. Quick Verification
- Compute $A A^{-1}$:
  $$\begin{pmatrix} 1 & 2 \\ 3 & 5 \end{pmatrix} \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix} = \begin{pmatrix} 1(-5)+2(3) & 1(2)+2(-1) \\ 3(-5)+5(3) & 3(2)+5(-1) \end{pmatrix} = \begin{pmatrix} -5+6 & 2-2 \\ -15+15 & 6-5 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I.$$
- Verify with $2 \times 2$ formula: $\det A = 1(5) - 2(3) = -1$.
  $A^{-1} = \frac{1}{-1}\begin{pmatrix}5&-2\\-3&1\end{pmatrix} = \begin{pmatrix}-5&2\\3&-1\end{pmatrix}$. Exactly matches.

## 8. Common Mistakes
- Applying row operations only to the left half and forgetting to perform the exact same arithmetic on the right half.
- Sign errors when subtracting negative numbers in $R_1 - 2R_2$, such as $0 - 2(-1) = -2$ instead of $+2$.

## 9. Short In-Class Explanation (3 Sentences)
We set up the augmented matrix $[A \mid I]$ and use row operations to eliminate entries and turn the left block into the identity matrix $I$. Each row operation corresponds to multiplying by an elementary matrix, so the combined effect of the operations is multiplication by $A^{-1}$. Because these same operations are applied to $I$ on the right, the right block transforms into the inverse matrix $\begin{pmatrix}-5&2\\3&-1\end{pmatrix}$.
