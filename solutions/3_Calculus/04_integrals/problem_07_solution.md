# Problem 7: Integration by Parts

## 1. Original Problem
Compute $\int xe^x dx$. State the product rule, derive integration by parts, and verify.

## 2. What We Are Trying to Find
The integrand is a product for which direct integration does not apply termwise. We use the product rule in reverse to reduce its complexity.

## 3. Key Idea or Theorem Needed Before the Calculation
From $(uv)'=u'v+uv'$, rearrange to $uv'= (uv)'-u'v$. Integrating gives $\int u v' dx=uv-\int u'v dx$.

## 4. Step-by-Step Solution
Choose $u=x$ and $v'=e^x$. Then $u'=1$, $v=e^x$. Apply the formula:
$$\int xe^x dx=xe^x-\int e^x dx=xe^x-e^x+C=e^x(x-1)+C.$$

## 5. Why Each Step Is Valid
Differentiating the product $xe^x$ produces both terms. Rearrangement isolates the desired product integral and leaves a simpler integral $\int e^x dx$.

## 6. Final Answer in Words
$e^x(x-1)+C$.

## 7. Quick Verification
Its derivative is $e^x(x-1)+e^x=xe^x$.

## 8. Common Mistakes
- Using the wrong sign in the by-parts formula.
- Choosing $u=e^x$ and repeatedly making the integral more complicated.

## 9. Short In-Class Explanation
Integration by parts reverses the product rule. Let $u=x$ so it simplifies under differentiation, and integrate $e^x$ unchanged. This gives $xe^x-e^x+C$, which checks by differentiation.
