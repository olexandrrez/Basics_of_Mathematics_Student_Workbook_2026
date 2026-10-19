# Problem 8: Two Exponential Functions

## 1. Original Problem
Differentiate $f(x)=e^{2x-3}+5^x$ and explain why the derivative contains 2 and $\ln5$.

## 2. What We Are Trying to Find
The two exponential terms use different differentiation rules: one has a variable exponent expression with base $e$, and one has constant base 5.

## 3. Key Idea or Rule Needed Before the Calculation
$(e^{u(x)})'=u'e^{u(x)}$ by the chain rule. For a positive constant $a$, $(a^x)'=a^x\ln a$, which follows from $a^x=e^{x\ln a}$.

## 4. Step-by-Step Solution
For $e^{2x-3}$, the exponent derivative is 2, so its derivative is $2e^{2x-3}$. For $5^x$, use the constant-base formula to get $5^x\ln5$. Adding gives
$$f'(x)=2e^{2x-3}+5^x\ln5.$$

## 5. Why Each Step Is Valid
The chain rule contributes the derivative of the exponent in the first term. The logarithmic factor in the second comes from rewriting $5^x$ as $e^{x\ln5}$.

## 6. Final Answer in Words
$f'(x)=2e^{2x-3}+5^x\ln5$.

## 7. Quick Verification
Both terms of the derivative are positive for every real $x$; therefore the original function is increasing everywhere, consistent with each summand increasing.

## 8. Common Mistakes
- Forgetting the factor 2 from the inner exponent.
- Differentiating $5^x$ as $x5^{x-1}$; that is a power rule for $x^5$, not an exponential rule.

## 9. Short In-Class Explanation
The first exponential needs the chain-rule factor 2. The second uses $(a^x)'=a^x\ln a$. Add the two derivatives.
