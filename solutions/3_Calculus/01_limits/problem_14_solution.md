# Problem 14: A 0/0 Limit with Trigonometry

## 1. Original Problem
Compute
$$\lim_{x\to0}\frac{1-\cos x}{x^2}.$$
Justify the result without using l'Hôpital's rule, using a trigonometric identity and the fundamental limit.

## 2. What We Are Trying to Find
We must evaluate the trigonometric limit:
$$L = \lim_{x \to 0} \frac{1 - \cos x}{x^2}.$$
Direct evaluation yields $\frac{1 - 1}{0^2} = \frac{0}{0}$. The exercise explicitly forbids l'Hôpital's rule; we must resolve this indeterminate form purely through trigonometric identities and reduction to the fundamental limit $\lim_{u \to 0} \frac{\sin u}{u} = 1$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Trigonometric Conjugate Identity (Difference of Squares)**:
  $$(1 - \cos x)(1 + \cos x) = 1 - \cos^2 x = \sin^2 x.$$
  This converts the expression $1 - \cos x$ directly into a squared sine term $\sin^2 x$.
- **Alternative Half-Angle Identity**:
  $$1 - \cos x = 2 \sin^2\left(\frac{x}{2}\right).$$
- **Fundamental Trigonometric Limit**:
  $$\lim_{u \to 0} \frac{\sin u}{u} = 1 \implies \lim_{u \to 0} \left(\frac{\sin u}{u}\right)^2 = 1^2 = 1.$$

## 4. Step-by-Step Solution

### Method 1: Using the Trigonometric Conjugate

#### Step 1: Multiply numerator and denominator by the conjugate $(1 + \cos x)$
The conjugate of $1 - \cos x$ is $1 + \cos x$.
Multiply numerator and denominator:
$$\frac{1 - \cos x}{x^2} = \frac{(1 - \cos x)(1 + \cos x)}{x^2 (1 + \cos x)}.$$

#### Step 2: Simplify the numerator using the Pythagorean identity
Using $(1 - \cos x)(1 + \cos x) = 1 - \cos^2 x$:
$$1 - \cos^2 x = \sin^2 x.$$
The expression becomes:
$$\frac{\sin^2 x}{x^2 (1 + \cos x)}.$$

#### Step 3: Regroup into known limits
Split the fraction into the product of two distinct factors:
$$\frac{\sin^2 x}{x^2 (1 + \cos x)} = \left( \frac{\sin x}{x} \right)^2 \cdot \frac{1}{1 + \cos x}.$$

#### Step 4: Evaluate the limit of each factor as $x \to 0$
1. For the first factor:
   $$\lim_{x \to 0} \left( \frac{\sin x}{x} \right)^2 = \left( \lim_{x \to 0} \frac{\sin x}{x} \right)^2 = 1^2 = 1.$$
2. For the second factor, since $\cos x$ is continuous at $x = 0$ and $\cos(0) = 1$:
   $$\lim_{x \to 0} \frac{1}{1 + \cos x} = \frac{1}{1 + \cos 0} = \frac{1}{1 + 1} = \frac{1}{2}.$$

#### Step 5: Multiply the limits
By the product rule for limits:
$$\lim_{x \to 0} \frac{1 - \cos x}{x^2} = 1 \cdot \frac{1}{2} = \frac{1}{2}.$$

---

### Method 2: Using the Half-Angle Identity (Verification)
Using $1 - \cos x = 2 \sin^2\left(\frac{x}{2}\right)$:
$$\frac{1 - \cos x}{x^2} = \frac{2 \sin^2(x/2)}{x^2} = 2 \cdot \left( \frac{\sin(x/2)}{x} \right)^2.$$
Multiply and divide inside the square by $2$:
$$2 \cdot \left( \frac{1}{2} \cdot \frac{\sin(x/2)}{x/2} \right)^2 = 2 \cdot \frac{1}{4} \cdot \left( \frac{\sin(x/2)}{x/2} \right)^2 = \frac{1}{2} \left( \frac{\sin(x/2)}{x/2} \right)^2.$$
As $x \to 0$, $\frac{x}{2} \to 0$, so $\frac{\sin(x/2)}{x/2} \to 1$:
$$L = \frac{1}{2} \cdot 1^2 = \frac{1}{2}.$$
Both standard methods arrive at the identical value $\frac{1}{2}$.

## 5. Why Each Step Is Valid
1. **Conjugate multiplication**: Since $\cos x \approx 1$ near $x = 0$, $1 + \cos x \approx 2 \neq 0$. Multiplying top and bottom by $1 + \cos x$ does not divide by zero and preserves equivalence.
2. **Pythagorean identity**: $\sin^2 x + \cos^2 x = 1$ is an absolute trigonometric identity for all real $x$.
3. **Product limit law**: The limits of both factors exist independently, allowing their product limit to be computed as the product of individual limits.

## 6. Final Answer in Words
The limit as $x$ approaches $0$ is $\frac{1}{2}$. Multiplying top and bottom by the conjugate $1+\cos x$ converts the numerator into $\sin^2 x$. Factoring the expression into $(\sin x / x)^2 \times \frac{1}{1+\cos x}$ allows us to evaluate the limit as $1^2 \times \frac{1}{2} = \frac{1}{2}$ without using l'Hôpital's rule.

## 7. Quick Verification
- Check via Taylor series approximation:
  $$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$$
  $$1 - \cos x = \frac{x^2}{2} - \frac{x^4}{24} + \dots$$
  Dividing by $x^2$:
  $$\frac{1 - \cos x}{x^2} = \frac{1}{2} - \frac{x^2}{24} + \dots \xrightarrow{x \to 0} \frac{1}{2}.$$
- Numerical calculation at $x = 0.01$ radians:
  $$\cos(0.01) \approx 0.9999500004$$
  $$\frac{1 - 0.9999500004}{0.0001} = \frac{0.0000499996}{0.0001} = 0.499996 \approx 0.5.$$

## 8. Common Mistakes
- **Forgetting the denominator in the conjugate**: Writing $(1-\cos x)(1+\cos x) = \sin^2 x$ in the numerator, but forgetting to include $(1+\cos x)$ in the denominator.
- **Squaring errors**: Writing $\frac{\sin^2 x}{x^2} = \frac{\sin x}{x} = 1$ without realizing it is squared ($1^2 = 1$, which happens to have the same value, but algebraically incorrect if another constant was present).
- **Evaluating $\frac{1}{1+\cos 0} = \frac{1}{1+0} = 1$**: Mistakenly recalling that $\cos(0) = 0$ instead of $\cos(0) = 1$.

## 9. Short In-Class Explanation (3 Sentences)
We multiply the numerator and denominator by the conjugate $1+\cos x$, which turns the numerator into $1-\cos^2 x = \sin^2 x$. This lets us factor the expression into $(\frac{\sin x}{x})^2$ multiplied by $\frac{1}{1+\cos x}$. Since $\frac{\sin x}{x} \to 1$ and $\frac{1}{1+\cos 0} = \frac{1}{2}$, the entire limit evaluates cleanly to $\frac{1}{2}$.
