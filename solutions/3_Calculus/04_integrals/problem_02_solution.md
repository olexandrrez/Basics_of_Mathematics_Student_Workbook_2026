# Problem 2: Powers, Roots, and the Domain

## 1. Original Problem
Compute $\int(2\sqrt{x}+3/x^2-x^{1/3})dx$, first rewriting powers, giving the domain, and checking the result.

## 2. What We Are Trying to Find
We apply the power rule to each term while preserving restrictions imposed by the original integrand.

## 3. Key Idea or Theorem Needed Before the Calculation
Write roots as fractional powers and reciprocals as negative powers. Use the power rule except at exponent $-1$. The original expression requires $x>0$ because of $\sqrt{x}$ and $1/x^2$ together.

## 4. Step-by-Step Solution
Rewrite as $2x^{1/2}+3x^{-2}-x^{1/3}$. The root allows $x\ge0$, but the reciprocal term excludes zero; therefore the domain is $(0,\infty)$. Integrate:
$$2\frac{x^{3/2}}{3/2}+3\frac{x^{-1}}{-1}-\frac{x^{4/3}}{4/3}+C.$$
Thus
$$F(x)=\frac43x^{3/2}-3x^{-1}-\frac34x^{4/3}+C.$$

## 5. Why Each Step Is Valid
Each exponent differs from $-1$, so the power rule applies. The result is valid on the original domain; no endpoint at zero is added.

## 6. Final Answer in Words
$F(x)=\frac43x^{3/2}-3/x-\frac34x^{4/3}+C$ for $x>0$.

## 7. Quick Verification
Differentiating gives $2x^{1/2}+3x^{-2}-x^{1/3}$.

## 8. Common Mistakes
- Integrating $x^{-2}$ as $x^{-1}$ instead of $-x^{-1}$.
- Including zero in the domain of the integrand.
- Forgetting the constant of integration.

## 9. Short In-Class Explanation
Rewrite each term as a power, integrate with the power rule, and keep $x>0$ because the original contains $1/x^2$. Differentiate the answer to check all coefficients and signs.
