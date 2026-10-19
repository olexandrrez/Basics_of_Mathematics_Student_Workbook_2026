# Problem 12: Several Rules at Once

## 1. Original Problem
Differentiate $f(x)=(x^2+1)^3e^x$. State a plan identifying the rule for the whole expression and for one factor, then factor common terms.

## 2. What We Are Trying to Find
The expression is a product, and one factor is a composite power. We must apply the product rule outside and the chain rule inside.

## 3. Key Idea or Rule Needed Before the Calculation
Use $(uv)'=u'v+uv'$ for the product and $(g^3)'=3g^2g'$ for the composite factor.

## 4. Step-by-Step Solution
Let $u=(x^2+1)^3$, $v=e^x$. The chain rule gives $u'=3(x^2+1)^2(2x)=6x(x^2+1)^2$, and $v'=e^x$. Apply the product rule:
$$f'=6x(x^2+1)^2e^x+(x^2+1)^3e^x.$$
Factor the common quantity $e^x(x^2+1)^2$:
$$f'=e^x(x^2+1)^2(6x+x^2+1).$$

## 5. Why Each Step Is Valid
The outer product rule accounts for both factors. The chain rule accounts for the inner $x^2+1$ in the first factor. Factoring does not change the value of the derivative.

## 6. Final Answer in Words
$f'(x)=e^x(x^2+1)^2(x^2+6x+1)$.

## 7. Quick Verification
Expanding the factored expression gives the two original product-rule terms, so the factorization is consistent.

## 8. Common Mistakes
- Applying only the product rule and missing the inner factor $2x$.
- Applying only the chain rule and ignoring the exponential factor's derivative.

## 9. Short In-Class Explanation
First see the whole expression as a product. Differentiate the power factor by the chain rule, differentiate $e^x$, add the two product terms, and factor their shared factors.
