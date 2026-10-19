# Problem 1: Antiderivative and Verification

## 1. Original Problem
For $f(x)=3x^2-4x+5$, find one antiderivative, write the full family, verify it, and explain the constant $C$.

## 2. What We Are Trying to Find
An antiderivative is a function whose derivative is the given integrand. We find one and then account for every possible antiderivative.

## 3. Key Idea or Theorem Needed Before the Calculation
Reverse the power rule: for $n\ne-1$, $\int x^n dx=x^{n+1}/(n+1)+C$. Integrals are linear over sums and constant multiples.

## 4. Step-by-Step Solution
Integrate term by term:
$$\int3x^2dx=x^3,\qquad\int-4xdx=-2x^2,\qquad\int5dx=5x.$$
Therefore the full family is
$$F(x)=x^3-2x^2+5x+C.$$

## 5. Why Each Step Is Valid
Differentiating each antiderivative term reverses the corresponding power-rule step. Adding a constant does not change the derivative, so all real values of $C$ work.

## 6. Final Answer in Words
All antiderivatives are $x^3-2x^2+5x+C$, where $C$ is arbitrary.

## 7. Quick Verification
$$F'(x)=3x^2-4x+5,$$ exactly the original function.

## 8. Common Mistakes
- Forgetting $+C$ for an indefinite integral.
- Dividing by the old exponent instead of the new exponent.

## 9. Short In-Class Explanation
Integrate each polynomial term by reversing the power rule. The result is $x^3-2x^2+5x+C$. Differentiation recovers the integrand, and the constant remains arbitrary because it differentiates to zero.
