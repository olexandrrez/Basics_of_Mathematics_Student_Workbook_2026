# Problem 5: The Chain Rule

## 1. Original Problem
For $f(x)=(3x^2-2x+1)^5$, identify the inner and outer functions, differentiate, and explain the extra factor.

## 2. What We Are Trying to Find
The fifth power acts on a polynomial expression rather than directly on $x$. We must differentiate both the outer power and the changing inner expression.

## 3. Key Idea or Rule Needed Before the Calculation
For $F(u(x))$, the chain rule states $(F(u(x)))'=F'(u(x))u'(x)$. The derivative of $u^5$ with respect to $u$ is $5u^4$.

## 4. Step-by-Step Solution
Let $u(x)=3x^2-2x+1$. Then $u'(x)=6x-2$. With outer function $F(u)=u^5$, we have $F'(u)=5u^4$. Therefore
$$f'(x)=5(3x^2-2x+1)^4(6x-2).$$

## 5. Why Each Step Is Valid
The outer derivative describes change with respect to $u$; multiplying by $u'(x)$ converts that to change with respect to $x$. This is why the factor $6x-2$ cannot be omitted.

## 6. Final Answer in Words
$f'(x)=5(3x^2-2x+1)^4(6x-2)$.

## 7. Quick Verification
The outer exponent drops from 5 to 4, and the inner derivative is $6x-2$. These are the two expected components of the chain rule.

## 8. Common Mistakes
- Forgetting to differentiate the inside.
- Replacing the inner derivative by the original polynomial.
- Applying the product rule even though the expression is a composition, not a product.

## 9. Short In-Class Explanation
Treat the polynomial as one inner function. Differentiate the fifth power to get five times the fourth power, then multiply by the derivative $6x-2$ of the inside.
