# Problem 03: A Square Root and Removing an Indeterminate Form

## 1. Original Problem
Compute
$$\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right).$$
Use the conjugate expression and explain why this transformation removes the difficulty.

## 2. What We Are Trying to Find
We must compute the limit of the sequence $a_n = \sqrt{n^2+5n} - n$ as $n \to \infty$. As $n$ grows, both $\sqrt{n^2+5n} \to \infty$ and $n \to \infty$, creating an indeterminate form of type $\infty - \infty$. We must eliminate this indeterminacy by multiplying and dividing by the algebraic conjugate.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Difference of Squares Identity**:
  $$(A - B)(A + B) = A^2 - B^2.$$
  Setting $A = \sqrt{n^2+5n}$ and $B = n$, we have:
  $$A^2 - B^2 = (n^2+5n) - n^2 = 5n.$$
- **Rationalizing Conjugate Technique**:
  For an expression $A - B$, multiply and divide by $A + B$:
  $$A - B = \frac{(A - B)(A + B)}{A + B} = \frac{A^2 - B^2}{A + B}.$$
  This converts the problematic difference of two competing infinite quantities into a quotient where the canceling highest-order terms annihilate each other.

## 4. Step-by-Step Solution

### Step 1: Identify the indeterminate form
As $n \to \infty$:
- $\sqrt{n^2 + 5n} \to \infty$
- $n \to \infty$
Direct subtraction yields $\infty - \infty$, which is indeterminate. We cannot simply conclude that the limit is $0$, because $\sqrt{n^2+5n} > n$ and their difference may settle at a positive constant.

### Step 2: Multiply and divide by the conjugate
The conjugate of $\sqrt{n^2+5n} - n$ is $\sqrt{n^2+5n} + n$.
Multiply and divide by this expression:
$$\sqrt{n^2+5n} - n = \frac{\left(\sqrt{n^2+5n} - n\right)\left(\sqrt{n^2+5n} + n\right)}{\sqrt{n^2+5n} + n}.$$

### Step 3: Expand the numerator using difference of squares
Applying $(A - B)(A + B) = A^2 - B^2$:
$$\left(\sqrt{n^2+5n}\right)^2 - n^2 = (n^2 + 5n) - n^2 = 5n.$$
Thus, the expression simplifies to:
$$\frac{5n}{\sqrt{n^2+5n} + n}.$$

### Step 4: Divide numerator and denominator by $n$
For $n > 0$, we have $n = \sqrt{n^2}$. Divide every term in the numerator and denominator by $n$:
$$\frac{\frac{5n}{n}}{\frac{\sqrt{n^2+5n}}{n} + \frac{n}{n}} = \frac{5}{\sqrt{\frac{n^2+5n}{n^2}} + 1} = \frac{5}{\sqrt{1 + \frac{5}{n}} + 1}.$$

### Step 5: Evaluate the limit as $n \to \infty$
As $n \to \infty$, $\frac{5}{n} \to 0$. By continuity of the square root function:
$$\lim_{n\to\infty} \sqrt{1 + \frac{5}{n}} = \sqrt{1 + 0} = 1.$$
Substitute this into the fraction:
$$\lim_{n\to\infty} \frac{5}{\sqrt{1 + \frac{5}{n}} + 1} = \frac{5}{1 + 1} = \frac{5}{2} = 2.5.$$

### Step 6: Why this transformation removes the difficulty
In the original expression $\sqrt{n^2+5n} - n$, both terms grow at the dominant linear rate $\sim n$. Subtracting them produces a catastrophic cancellation where the $n^2$ terms cancel out, but the leftover residual effect (the $+5n$ inside the radical) is hidden by the subtraction.
Multiplying by the conjugate moves the addition to the denominator $(\sqrt{n^2+5n} + n)$, which avoids cancellation (it is $\infty + \infty = \infty$, not indeterminate), while algebraically eliminating the square root from the numerator. This converts the indeterminate subtraction into a stable quotient of two linear expressions in $n$.

## 5. Why Each Step Is Valid
1. **Multiplication by $1$**: Since $\sqrt{n^2+5n} + n > 0$ for all $n \ge 1$, $\frac{\sqrt{n^2+5n} + n}{\sqrt{n^2+5n} + n} = 1$. Multiplying by $1$ does not change value.
2. **Difference of squares identity**: Valid for all real numbers $A, B$.
3. **Pulling $n$ inside square root**: For $n > 0$, $\frac{\sqrt{X}}{n} = \sqrt{\frac{X}{n^2}}$, which is valid because both quantities are positive.
4. **Continuity of $\sqrt{x}$**: The square root function is continuous on $[0, \infty)$, so $\lim \sqrt{u_n} = \sqrt{\lim u_n}$.

## 6. Final Answer in Words
The limit of the sequence $\sqrt{n^2+5n}-n$ as $n \to \infty$ is $\frac{5}{2}$. Multiplying by the conjugate removes the indeterminate form $\infty - \infty$ by converting the expression into a quotient where the dominant $n^2$ terms cancel in the numerator and the denominator adds two positive infinite terms without cancellation.

## 7. Quick Verification
Calculate values for large $n$:
- For $n = 10$: $\sqrt{100 + 50} - 10 = \sqrt{150} - 10 \approx 12.2474 - 10 = 2.2474$.
- For $n = 100$: $\sqrt{10000 + 500} - 100 = \sqrt{10500} - 100 \approx 102.4695 - 100 = 2.4695$.
- For $n = 1000$: $\sqrt{1000000 + 5000} - 1000 = \sqrt{1005000} - 1000 \approx 1002.4969 - 1000 = 2.4969$.
The values rapidly converge toward $2.5 = \frac{5}{2}$.

## 8. Common Mistakes
- **Assuming $\sqrt{n^2+5n} \approx \sqrt{n^2} = n$, concluding $n - n = 0$**: This naive approximation ignores the lower-order term $+5n$, which actually creates the finite offset of $2.5$.
- **Dividing by $n$ inside the root as $n$ instead of $n^2$**: Writing $\frac{\sqrt{n^2+5n}}{n} = \sqrt{\frac{n^2+5n}{n}}$, which mistakenly changes the order of the terms.
- **Sign error in the conjugate**: Multiplying by $\sqrt{n^2+5n} - n$ instead of $+ n$.

## 9. Short In-Class Explanation (3 Sentences)
The direct limit produces an indeterminate form of type $\infty - \infty$, because both terms grow linearly with $n$. We multiply and divide by the conjugate $\sqrt{n^2+5n}+n$, which cancels the $n^2$ terms in the numerator via the difference of squares identity. Dividing both numerator and denominator by $n$ then turns the expression into $\frac{5}{1+1}$, giving the final limit of $\frac{5}{2}$.
