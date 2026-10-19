# Problem 11: Derivative from the Definition

## 1. Original Problem
Use only $f'(x)=\lim_{h\to0}[f(x+h)-f(x)]/h$ to find the derivative of $f(x)=x^2$, compare with the power rule, and identify where the limit is used.

## 2. What We Are Trying to Find
We calculate the limiting slope of secant lines through $(x,x^2)$ and a nearby point, then compare it to the derivative rule learned earlier.

## 3. Key Idea or Rule Needed Before the Calculation
The derivative definition is a limit of difference quotients. We simplify for nonzero $h$ before taking $h\to0$; direct substitution earlier would give an indeterminate $0/0$.

## 4. Step-by-Step Solution
Substitute $f(x)=x^2$:
$$f'(x)=\lim_{h\to0}\frac{(x+h)^2-x^2}{h}.$$
Expand the square and cancel $x^2$:
$$=\lim_{h\to0}\frac{x^2+2xh+h^2-x^2}{h}=\lim_{h\to0}(2x+h)=2x.$$
The limit is taken only after canceling $h$ from the numerator and denominator.

## 5. Why Each Step Is Valid
The quotient is defined for $h\ne0$, which is exactly the punctured neighborhood used in a limit. The simplified expression has limit $2x$ as $h$ tends to zero.

## 6. Final Answer in Words
The definition gives $f'(x)=2x$, agreeing with the power rule.

## 7. Quick Verification
At, for example, $x=3$, the tangent slope is 6. The power rule also gives $(x^2)'=2x=6$ there.

## 8. Common Mistakes
- Substituting $h=0$ before simplifying.
- Failing to divide every term in $2xh+h^2$ by $h$.

## 9. Short In-Class Explanation
Insert $(x+h)^2$ and $x^2$ into the definition, expand, cancel the common terms and then cancel $h$. The remaining expression $2x+h$ tends to $2x$ as $h$ goes to zero.
