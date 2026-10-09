# Problem 12: Formula for a Matrix Power

## 1. Original Problem
Let
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix}.$$
Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

## 2. What We Are Trying to Find
We need to calculate the small powers $A^2, A^3, A^4$ of a shear matrix, identify the pattern for the general power $A^n$, state the conjecture, and prove it rigorously for all positive integers $n$ using mathematical induction.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Power of a Matrix**: Defined recursively by $A^1 = A$ and $A^{k+1} = A^k \cdot A$.
- **Mathematical Induction**: To prove a statement $P(n)$ for all integers $n \ge 1$:
  1. Base case: verify $P(1)$.
  2. Inductive step: assume $P(n)$ holds (induction hypothesis) and prove that $P(n+1)$ must also hold.

## 4. Step-by-Step Solution

### Step 1: Compute Small Powers
- For $A^2$:
  $$A^2 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+1(0) & 1(1)+1(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}.$$
- For $A^3$:
  $$A^3 = A^2 A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+2(0) & 1(1)+2(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}.$$
- For $A^4$:
  $$A^4 = A^3 A = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+3(0) & 1(1)+3(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}.$$

### Step 2: Formulate the Conjecture
Observing the powers:
$$A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix},\quad A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix},\quad A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix},\quad A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}.$$
The diagonal entries remain $1$, the bottom-left entry remains $0$, and the upper-right entry equals the exponent $n$.
**Conjecture**: For all positive integers $n \ge 1$,
$$A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}.$$

### Step 3: Inductive Proof for $n+1$
- **Base Case ($n=1$)**:
  $$\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = A^1.$$ True.
- **Inductive Step**:
  Assume the induction hypothesis holds for an integer $n \ge 1$:
  $$A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}.$$
  We now compute $A^{n+1} = A^n A$:
  $$A^{n+1} = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1) + n(0) & 1(1) + n(1) \\ 0(1) + 1(0) & 0(1) + 1(1) \end{pmatrix} = \begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix}.$$
  This is precisely the claimed formula with $n$ replaced by $n+1$.
By the principle of mathematical induction, the formula holds for all positive integers $n \ge 1$.

## 5. Why Each Step Is Valid
- Matrix powers are associative, so $A^{n+1} = A^n A$.
- Substituting the induction hypothesis replaces $A^n$ with the assumed matrix.
- Direct row-by-column multiplication performs the exact arithmetic $1 \cdot 1 + n \cdot 1 = n+1$, rigorously closing the induction step.

## 6. Final Answer in Words
The powers are $A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$, $A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$, and $A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$. The general formula is $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$ for all $n \ge 1$. Multiplying $A^n$ by $A$ adds $1$ to the top-right entry while leaving all other entries unchanged, proving that the formula holds for $n+1$.

## 7. Quick Verification
- Let $n = 0$: $A^0 = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$, which matches $A^0 = I$.
- Geometric interpretation: $A$ represents a horizontal shear of factor $1$. Applying this shear $n$ times in succession naturally shears the plane by a total factor of $n$.

## 8. Common Mistakes
- Stopping at checking $A^4$ or $A^5$ and claiming that constitutes a mathematical proof. Verification for specific cases does not substitute an inductive step.
- Failing to state where the induction hypothesis was used in computing $A^{n+1}$.

## 9. Short In-Class Explanation (3 Sentences)
Computing the first few powers shows that the upper-right entry increases by 1 each time, leading to the conjecture $A^n = \begin{pmatrix}1 & n \\ 0 & 1\end{pmatrix}$. To prove this for all $n$, we assume the formula holds for $n$ and multiply by $A$, which gives an upper-right entry of $n+1$ and preserves the other entries. By mathematical induction, this proves the conjecture for every positive integer.
