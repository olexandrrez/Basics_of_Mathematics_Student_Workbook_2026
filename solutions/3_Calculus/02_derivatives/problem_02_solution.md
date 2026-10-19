# Problem 2: Powers, Roots, and the Domain

## 1. Original Problem
For $f(x)=2\sqrt{x}-3/x^2+x^{3/2}$, rewrite using powers, determine its domain, differentiate, and compare the domains of $f$ and $f'$.

## 2. What We Are Trying to Find
We will express radicals and reciprocal powers in exponent notation, identify real inputs for which every term is defined, then differentiate and check where the resulting formula exists.

## 3. Key Idea or Rule Needed Before the Calculation
Use $\sqrt{x}=x^{1/2}$, $1/x^2=x^{-2}$ and $(x^p)'=px^{p-1}$. Domain restrictions must be carried through: an even root requires a nonnegative radicand, while a denominator cannot be zero.

## 4. Step-by-Step Solution
Rewrite:
$$f(x)=2x^{1/2}-3x^{-2}+x^{3/2}.$$
The root requires $x\ge0$, and $x^{-2}$ excludes $x=0$, so $D_f=(0,\infty)$. Differentiate term by term:
$$f'(x)=2\cdot\tfrac12x^{-1/2}-3(-2)x^{-3}+\tfrac32x^{1/2}=x^{-1/2}+6x^{-3}+\tfrac32x^{1/2}.$$
For all three terms of $f'$ to be real and finite, $x$ must be positive; hence $D_{f'}=(0,\infty)$.

## 5. Why Each Step Is Valid
The exponent rule applies to each power on its domain. The negative exponents in the derivative still place powers of $x$ in denominators, so zero remains excluded. No positive input is excluded.

## 6. Final Answer in Words
The original function is $2x^{1/2}-3x^{-2}+x^{3/2}$ on $(0,\infty)$. Its derivative is $x^{-1/2}+6x^{-3}+\frac32x^{1/2}$, with the same domain.

## 7. Quick Verification
Integrating the derivative terms reverses the calculation: $x^{-1/2}$ integrates to $2x^{1/2}$, $6x^{-3}$ to $-3x^{-2}$, and $\frac32x^{1/2}$ to $x^{3/2}$, up to a constant.

## 8. Common Mistakes
- Including $x=0$ because the square root alone permits it; the reciprocal term does not.
- Differentiating $x^{-2}$ as $-2x^{-2}$ instead of $-2x^{-3}$.
- Assuming the derivative's domain must always be smaller; here it happens to match.

## 9. Short In-Class Explanation
Convert each term to a power, then use the power rule. The square root allows zero, but the reciprocal term excludes it, so the function's domain is positive reals. The derivative also contains negative powers and has that same domain.
