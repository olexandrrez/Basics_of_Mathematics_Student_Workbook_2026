# Problem 03: Swapping Two Rows

## 1. Original Problem
For
$$A=\begin{pmatrix}1&2&0\\0&3&1\\2&1&1\end{pmatrix}$$
compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.
First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

## 2. What We Are Trying to Find
We must compute $\det A$, predict the value of $\det B$ when rows 1 and 2 are interchanged using the row-swap property of determinants, and verify the prediction by calculating $\det B$ explicitly.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Row Swap Property (Antisymmetry)**: Interchanging any two rows (or columns) of a square matrix multiplies its determinant by $-1$:
  $$\det(\text{swap}(R_i, R_j)) = -\det(A).$$
- **Verification**: Calculating $\det B$ directly must yield the negated value $-\det A$.

## 4. Step-by-Step Solution

### Step 1: Compute $\det A$
Expand along the first row of $A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{pmatrix}$:
$$\det A = 1 \cdot \det\begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} - 2 \cdot \det\begin{pmatrix} 0 & 1 \\ 2 & 1 \end{pmatrix} + 0 \cdot \det\begin{pmatrix} 0 & 3 \\ 2 & 1 \end{pmatrix}.$$
Compute the $2 \times 2$ determinants:
- $\det\begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} = 3(1) - 1(1) = 3 - 1 = 2$.
- $\det\begin{pmatrix} 0 & 1 \\ 2 & 1 \end{pmatrix} = 0(1) - 1(2) = 0 - 2 = -2$.
Thus:
$$\det A = 1(2) - 2(-2) + 0 = 2 + 4 = 6.$$

### Step 2: Predict $\det B$
Matrix $B$ is obtained by swapping Row 1 and Row 2 of $A$:
$$B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}.$$
By the antisymmetry property of determinants, swapping one pair of rows multiplies the determinant by $-1$.
**Prediction**:
$$\det B = -\det A = -6.$$

### Step 3: Verify Prediction by Computing $\det B$
Expand along the first column of $B$ (which has a zero in entry $b_{11}$):
$$\det B = 0 \cdot M_{11} - 1 \cdot \det\begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} + 2 \cdot \det\begin{pmatrix} 3 & 1 \\ 2 & 0 \end{pmatrix}.$$
Compute the minors:
- $\det\begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} = 3(1) - 1(1) = 2$.
- $\det\begin{pmatrix} 3 & 1 \\ 2 & 0 \end{pmatrix} = 3(0) - 1(2) = -2$.
Substitute:
$$\det B = -1(2) + 2(-2) = -2 - 4 = -6.$$
The direct computation matches our prediction of $-6$ exactly.

## 5. Why Each Step Is Valid
- Laplace expansion along any row or column is valid and yields the identical determinant value.
- The determinant is an alternating multilinear form; swapping two vectors in an alternating form reverses the sign of the evaluated volume.

## 6. Final Answer in Words
The determinant of matrix $A$ is $6$. By the row-swap property, swapping the first two rows predicts $\det B = -6$. Calculating $\det B$ directly yields $-6$, verifying the theoretical prediction.

## 7. Quick Verification
- Checking by Sarrus' rule on $A$:
  Main diagonals: $1(3)(1) + 2(1)(2) + 0(0)(1) = 3 + 4 + 0 = 7$.
  Anti-diagonals: $0(3)(2) + 1(1)(1) + 2(0)(1) = 0 + 1 + 0 = 1$.
  $\det A = 7 - 1 = 6$.
- For $B$, swapping one row transposes two rows in the permutation sign $\text{sgn}(\sigma)$, flipping the sign of every permutation term, confirming $\det B = -6$.

## 8. Common Mistakes
- Believing that swapping rows leaves the determinant unchanged (confusing row swaps with row additions $R_i \leftarrow R_i + cR_j$).
- Forgetting the alternating signs in Laplace expansion ($+ - +$).

## 9. Short In-Class Explanation (3 Sentences)
Expanding matrix $A$ along its first row gives a determinant of $6$. According to determinant theory, interchanging any two rows reverses the sign of the determinant, so we predict $\det B = -6$. Direct calculation of $\det B$ confirms the value $-6$, verifying that a row swap flips the sign.
