# Problem 11: Choose the Method First

## 1. Original Problem
For each integral, identify a method and compute: (1) $\int\sin(3x)dx$, (2) $\int x\ln xdx$, (3) $\int x/\sqrt{x^2+1}dx$.

## 2. What We Are Trying to Find
Each expression has a different structural cue: a composite trig function, a product involving a logarithm, and a numerator related to a radical's inner derivative.

## 3. Key Idea or Theorem Needed Before the Calculation
Use substitution for compositions whose inner derivative appears; use integration by parts when one factor simplifies by differentiation, especially logarithms.

## 4. Step-by-Step Solution
**(1) Substitution.** Let $u=3x$, so $du=3dx$. Then $\int\sin(3x)dx=\frac13\int\sin udu=-\frac13\cos(3x)+C$.

**(2) Parts.** Let $u=\ln x$, $dv=x dx$, so $du=dx/x$, $v=x^2/2$. Then
$$\int x\ln xdx=\frac{x^2}{2}\ln x-\frac12\int xdx=\frac{x^2}{2}\ln x-\frac{x^2}{4}+C,$$
for $x>0$.

**(3) Substitution.** Let $u=x^2+1$, so $du=2x dx$. Then $\int x/\sqrt{x^2+1}dx=\frac12\int u^{-1/2}du=\sqrt{x^2+1}+C$.

## 5. Why Each Step Is Valid
Each method matches the integrand's structure, and the factors from substitutions correctly account for the differential.

## 6. Final Answer in Words
The antiderivatives are $-\cos(3x)/3$, $(x^2/2)\ln x-x^2/4$, and $\sqrt{x^2+1}$, each plus $C$.

## 7. Quick Verification
Differentiation gives $\sin(3x)$, $x\ln x$, and $x/\sqrt{x^2+1}$, respectively.

## 8. Common Mistakes
- Forgetting the factor $1/3$ in the first substitution.
- Using parts without correctly calculating $v$ or the minus sign.
- Omitting the factor $1/2$ in the third substitution.

## 9. Short In-Class Explanation
The first and third integrals reverse the chain rule; the middle is a product best handled by parts. Showing the substitution differentials and the parts choices makes the method transparent.
