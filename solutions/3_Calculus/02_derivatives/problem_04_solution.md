# Problem 4: A Quotient and Domain Control

## 1. Original Problem
For $f(x)=(x^2+1)/(x-1)$, determine the domain, differentiate and simplify, and explain why $x\ne1$ remains important.

## 2. What We Are Trying to Find
We need both the derivative formula and its valid inputs. Algebraic simplification must not erase a restriction inherited from the original function.

## 3. Key Idea or Rule Needed Before the Calculation
The quotient rule is $(u/v)'=(u'v-uv')/v^2$, provided $v\ne0$. The domain of a rational function excludes zeros of its original denominator.

## 4. Step-by-Step Solution
Since $x-1\ne0$, the domain is $\mathbb R\setminus\{1\}$. Set $u=x^2+1$, $u'=2x$, $v=x-1$, $v'=1$. Then
$$f'(x)=\frac{2x(x-1)-(x^2+1)}{(x-1)^2}=\frac{x^2-2x-1}{(x-1)^2}.$$
Polynomial division also gives $f=x+1+2/(x-1)$, still only for $x\ne1$.

## 5. Why Each Step Is Valid
The quotient rule applies wherever the denominator is nonzero. Combining the numerator terms gives $2x^2-2x-x^2-1=x^2-2x-1$. Rewriting the function by division does not define it at its pole.

## 6. Final Answer in Words
$D_f=\mathbb R\setminus\{1\}$ and $f'(x)=(x^2-2x-1)/(x-1)^2$ on that domain.

## 7. Quick Verification
Differentiate the divided form: $(x+1+2/(x-1))'=1-2/(x-1)^2$. Combining over a common denominator gives $(x^2-2x-1)/(x-1)^2$.

## 8. Common Mistakes
- Reversing the subtraction in the quotient-rule numerator.
- Squaring only part of the denominator.
- Treating a rewritten formula as permission to include $x=1$.

## 9. Short In-Class Explanation
The denominator excludes $x=1$. Apply the quotient rule and simplify the numerator to $x^2-2x-1$. Keep the original restriction: neither the function nor its derivative exists at the pole.
