# Problem 9: A Logarithm and the Chain Rule

## 1. Original Problem
Differentiate $f(x)=\ln(x^2+1)$, determine the derivative's sign for negative, zero, and positive $x$, and describe the behavior near zero.

## 2. What We Are Trying to Find
We will find the domain, derivative, sign chart, and resulting local/global behavior of the function.

## 3. Key Idea or Rule Needed Before the Calculation
For positive $u(x)$, $(\ln u)'=u'/u$. A derivative sign chart determines intervals of increase and decrease; a change from negative to positive indicates a minimum.

## 4. Step-by-Step Solution
Since $x^2+1\ge1$, the logarithm is defined for all real $x$. Let $u=x^2+1$, so $u'=2x$. Then
$$f'(x)=\frac{2x}{x^2+1}.$$
The denominator is positive. Thus $f'<0$ if $x<0$, $f'(0)=0$, and $f'>0$ if $x>0$. The function decreases up to zero and increases afterward. Since $f(0)=\ln1=0$, it has a minimum at zero.

## 5. Why Each Step Is Valid
The denominator's positivity means it does not alter the numerator's sign. The derivative changes from negative to positive at zero, which verifies a minimum. Moreover, $x^2+1\ge1$ implies $f(x)\ge0$ because logarithm is increasing.

## 6. Final Answer in Words
$f'(x)=2x/(x^2+1)$; it is negative to the left of zero, zero at zero, and positive to the right. The global minimum is $f(0)=0$.

## 7. Quick Verification
The function is even, $f(-x)=f(x)$, so the behavior on both sides is symmetric, consistent with the sign chart.

## 8. Common Mistakes
- Forgetting to divide by the inner expression $x^2+1$.
- Assuming $f'(0)=0$ means $f(0)=0$ without evaluating; here both happen to be zero.

## 9. Short In-Class Explanation
The chain rule gives $2x/(x^2+1)$. Its denominator is always positive, so the sign follows $x$: negative then positive. The function therefore reaches its minimum zero at the origin.
