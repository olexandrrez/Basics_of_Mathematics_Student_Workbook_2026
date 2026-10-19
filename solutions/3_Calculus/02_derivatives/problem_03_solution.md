# Problem 3: The Product Rule

## 1. Original Problem
Differentiate $f(x)=(x^2+1)e^x$. Compare with the incomplete suggestion $(2x)e^x$ and identify its missing term.

## 2. What We Are Trying to Find
Both factors depend on $x$, so we need to account for the change in each factor and explain why differentiating only one is not enough.

## 3. Key Idea or Rule Needed Before the Calculation
For differentiable functions $u,v$, $(uv)'=u'v+uv'$. In particular, the exponential factor also changes: $(e^x)'=e^x$.

## 4. Step-by-Step Solution
Take $u=x^2+1$, $u'=2x$, $v=e^x$, and $v'=e^x$. Then
$$f'(x)=2xe^x+(x^2+1)e^x=e^x(x^2+2x+1).$$
The proposed expression keeps the original exponential but differentiates only $x^2+1$. It omits $(x^2+1)e^x$, the product-rule contribution from differentiating $e^x$.

## 5. Why Each Step Is Valid
The product rule follows by differentiating both changing factors. The final factorization is valid because both terms contain $e^x$.

## 6. Final Answer in Words
The derivative is $e^x(x^2+2x+1)$. The incomplete answer omits the derivative of the exponential factor.

## 7. Quick Verification
At $x=0$, the original derivative formula gives $0+1=1$; the proposed incomplete expression gives 0. The discrepancy confirms the missing contribution.

## 8. Common Mistakes
- Multiplying the two derivatives, $u'v'$, instead of using $u'v+uv'$.
- Differentiating one factor while treating the other as constant.

## 9. Short In-Class Explanation
This is a product of two changing functions, so apply both terms of the product rule. Differentiating the polynomial gives $2xe^x$; differentiating the exponential gives $(x^2+1)e^x$. Their sum is the full derivative.
