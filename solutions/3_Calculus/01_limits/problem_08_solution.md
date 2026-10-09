# Problem 08: A Square Root in a Function Limit

## 1. Original Problem
Compute
$$\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}$$
by rationalizing the numerator. Compare the idea with Exercise 3 involving a sequence.

## 2. What We Are Trying to Find
We must:
1. Compute the limit of the algebraic function $f(x) = \frac{\sqrt{x}-2}{x-4}$ as $x \to 4$.
2. Rationalize the numerator by multiplying and dividing by the conjugate $\sqrt{x} + 2$.
3. Compare this technique with the conjugate method used in Exercise 3 for the sequence $\sqrt{n^2+5n} - n$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Rationalizing Conjugate Identity**:
  $$(\sqrt{u} - v)(\sqrt{u} + v) = u - v^2.$$
  Setting $u = x$ and $v = 2$, we obtain:
  $$(\sqrt{x} - 2)(\sqrt{x} + 2) = x - 2^2 = x - 4.$$
- **Resolving $\frac{0}{0}$ Indeterminacies**:
  When both numerator and denominator vanish at $x = c$, there is a hidden algebraic factor of $(x - c)$ causing the zero. Rationalization unmasks the factor $(x - 4)$ in the numerator, allowing it to be canceled against the identical factor in the denominator.

## 4. Step-by-Step Solution

### Step 1: Test direct substitution
Substitute $x = 4$ into $f(x)$:
$$\frac{\sqrt{4} - 2}{4 - 4} = \frac{2 - 2}{0} = \frac{0}{0}.$$
This is an indeterminate form of type $\frac{0}{0}$.

### Step 2: Multiply numerator and denominator by the conjugate
The conjugate of the numerator $\sqrt{x} - 2$ is $\sqrt{x} + 2$.
Multiply top and bottom by $(\sqrt{x} + 2)$:
$$\frac{\sqrt{x} - 2}{x - 4} = \frac{(\sqrt{x} - 2)(\sqrt{x} + 2)}{(x - 4)(\sqrt{x} + 2)}.$$

### Step 3: Expand the numerator
Using $(A - B)(A + B) = A^2 - B^2$:
$$(\sqrt{x} - 2)(\sqrt{x} + 2) = (\sqrt{x})^2 - 2^2 = x - 4.$$
Substitute this back into the fraction:
$$\frac{x - 4}{(x - 4)(\sqrt{x} + 2)}.$$

### Step 4: Cancel the common factor $(x - 4)$
Since the limit investigates the neighborhood $x \to 4$ where $x \neq 4$, the factor $x - 4 \neq 0$.
We cancel $(x - 4)$:
$$\frac{x - 4}{(x - 4)(\sqrt{x} + 2)} = \frac{1}{\sqrt{x} + 2}.$$

### Step 5: Evaluate the limit of the simplified expression
Since $g(x) = \frac{1}{\sqrt{x} + 2}$ is continuous at $x = 4$, substitute $x = 4$:
$$\lim_{x\to4}\frac{\sqrt{x}-2}{x-4} = \lim_{x\to4}\frac{1}{\sqrt{x} + 2} = \frac{1}{\sqrt{4} + 2} = \frac{1}{2 + 2} = \frac{1}{4}.$$

---

### Step 6: Comparison with Exercise 3
- **Shared mathematical idea**:
  Both exercises rely on the exact same algebraic identity $(A-B)(A+B) = A^2 - B^2$ to eliminate a radical that obscures algebraic simplification.
- **Different context and purpose**:
  - In Exercise 3 ($\\lim_{n \to \infty} [\sqrt{n^2+5n} - n]$), the conjugate was used on an **indeterminate difference at infinity** (form $\infty - \infty$). It converted a difference into a fraction so that the dominant $n^2$ terms canceled, leaving a manageable ratio of linear terms.
  - In Exercise 8, the conjugate is used on an **indeterminate quotient at a finite point** (form $\frac{0}{0}$). It transforms the numerator into the polynomial factor $(x - 4)$, allowing it to cancel the singular factor in the denominator that was causing division by zero.

## 5. Why Each Step Is Valid
1. **Multiplication by $1$**: For $x$ near $4$, $\sqrt{x} + 2 \approx 4 \neq 0$, so $\frac{\sqrt{x}+2}{\sqrt{x}+2} = 1$.
2. **Difference of squares**: $(\sqrt{x})^2 - 2^2 = x - 4$ is an algebraic identity for all $x \ge 0$.
3. **Cancellation**: In the limit as $x \to 4$, $x \neq 4$, so $x - 4 \neq 0$. Dividing non-zero quantities is valid.
4. **Continuity of the square root**: The function $\sqrt{x}$ is continuous on its domain, allowing direct evaluation of $\sqrt{4} = 2$.

## 6. Final Answer in Words
The limit as $x$ approaches $4$ is $\frac{1}{4}$. Multiplying numerator and denominator by the conjugate $\sqrt{x}+2$ removes the square root and produces the factor $(x-4)$, which cancels the identical factor in the denominator. This technique parallels Exercise 3: both employ the difference-of-squares identity to resolve an indeterminate form, but Exercise 3 resolved an $\infty-\infty$ difference at infinity, while here it resolves a $0/0$ ratio at a finite point.

## 7. Quick Verification
- Alternative algebraic method (factoring the denominator):
  Recall that for $x > 0$, $x - 4 = (\sqrt{x})^2 - 2^2 = (\sqrt{x} - 2)(\sqrt{x} + 2)$.
  Therefore:
  $$\frac{\sqrt{x}-2}{x-4} = \frac{\sqrt{x}-2}{(\sqrt{x}-2)(\sqrt{x}+2)} = \frac{1}{\sqrt{x}+2}.$$
  Taking $x \to 4$:
  $$\frac{1}{\sqrt{4}+2} = \frac{1}{4}.$$
  Both methods yield the exact same answer $\frac{1}{4}$.
- Numerical check: At $x = 4.001$: $\frac{\sqrt{4.001}-2}{0.001} \approx \frac{2.00024998 - 2}{0.001} = 0.24998 \approx 0.25$.

## 8. Common Mistakes
- **Flipping the sign inside the radical**: Multiplying by $\sqrt{x-2}$ or $\sqrt{-x}+2$ instead of changing the outer sign to $\sqrt{x}+2$.
- **Squaring individual terms instead of multiplying by conjugate**: Writing $\frac{(\sqrt{x}-2)^2}{(x-4)^2}$, which squares the whole fraction and alters the problem completely.
- **Denominator arithmetic error**: Writing the denominator as $(\sqrt{4}+2) = 4$ but forgetting the numerator is $1$, writing $4$ instead of $\frac{1}{4}$.

## 9. Short In-Class Explanation (3 Sentences)
Direct substitution gives $0/0$, so we multiply the numerator and denominator by the conjugate $\sqrt{x}+2$. This turns the numerator into $x-4$, which cancels the matching $x-4$ in the denominator that was creating the zero. Evaluating the remaining fraction $\frac{1}{\sqrt{x}+2}$ at $x=4$ yields the final limit of $\frac{1}{4}$.
