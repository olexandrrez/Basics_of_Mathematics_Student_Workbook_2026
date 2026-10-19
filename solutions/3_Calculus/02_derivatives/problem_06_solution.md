# Problem 6: Product Rule and Trigonometry

## 1. Original Problem
Differentiate $f(x)=x\sin x+\cos x$, simplify, find $f'(0)$, and interpret the tangent direction.

## 2. What We Are Trying to Find
We need the derivative of a product plus a trigonometric term. The evaluation at zero gives the slope of the tangent at $(0,f(0))$.

## 3. Key Idea or Rule Needed Before the Calculation
Use $(uv)'=u'v+uv'$, $(\sin x)'=\cos x$, and $(\cos x)'=-\sin x$.

## 4. Step-by-Step Solution
For $x\sin x$, the product rule gives $\sin x+x\cos x$. The remaining term differentiates to $-\sin x$. Adding and cancelling,
$$f'(x)=\sin x+x\cos x-\sin x=x\cos x.$$
At zero, $f'(0)=0$. Also $f(0)=1$, so the point is $(0,1)$ and its tangent is horizontal.

## 5. Why Each Step Is Valid
Each derivative follows from the standard product and trigonometric rules. The cancellation is exact. A zero derivative means zero tangent slope at that point.

## 6. Final Answer in Words
$f'(x)=x\cos x$ and $f'(0)=0$; the tangent at $(0,1)$ is horizontal.

## 7. Quick Verification
Substitute zero in the unsimplified expression: $\sin0+0\cos0-\sin0=0$.

## 8. Common Mistakes
- Using $(x\sin x)'=\cos x$ and omitting the product-rule term.
- Forgetting that derivative of cosine is negative sine.

## 9. Short In-Class Explanation
Apply the product rule to $x\sin x$, then differentiate cosine. The sine terms cancel, leaving $x\cos x$. At zero the slope is zero, so the tangent is horizontal.
