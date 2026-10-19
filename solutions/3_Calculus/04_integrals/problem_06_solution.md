# Problem 6: When Does a Logarithm Appear?

## 1. Original Problem
Compute $\int2x/(x^2+5)dx$, identify the substitution and explain the logarithm.

## 2. What We Are Trying to Find
We recognize the pattern “derivative of a denominator divided by that denominator,” which leads to a logarithmic antiderivative.

## 3. Key Idea or Theorem Needed Before the Calculation
Since $(\ln|u|)'=u'/u$, an integral of $u'/u$ becomes $\ln|u|+C$.

## 4. Step-by-Step Solution
Set $u=x^2+5$. Then $du=2x\,dx$, matching the numerator and differential. Therefore
$$\int\frac{2x}{x^2+5}dx=\int\frac{du}{u}=\ln|u|+C.$$
Because $x^2+5>0$ for every real $x$, remove the absolute value:
$$F(x)=\ln(x^2+5)+C.$$

## 5. Why Each Step Is Valid
The logarithm appears because its derivative is reciprocal input times the input derivative. Here the denominator derivative is exactly the numerator.

## 6. Final Answer in Words
$\ln(x^2+5)+C$.

## 7. Quick Verification
$F'(x)=2x/(x^2+5)$.

## 8. Common Mistakes
- Writing $\ln(x^2+5)$ without checking the sign; here it is safe because the argument is always positive.
- Forgetting the absolute value in cases where the substituted expression may be negative.

## 9. Short In-Class Explanation
The denominator's derivative is the numerator, so set $u=x^2+5$. The integral becomes $\int du/u$, whose antiderivative is a logarithm.
