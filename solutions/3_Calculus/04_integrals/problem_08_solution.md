# Problem 8: Choosing the Factors in Integration by Parts

## 1. Original Problem
Compute $\int x\cos xdx$ and justify differentiating $x$ and integrating cosine.

## 2. What We Are Trying to Find
We want a factor choice that makes the remaining integral simpler after applying integration by parts.

## 3. Key Idea or Theorem Needed Before the Calculation
Choose $u$ to become simpler when differentiated and $dv$ to have an easy antiderivative. Then use $\int u,dv=uv-\int v,du$.

## 4. Step-by-Step Solution
Set $u=x$, $dv=\cos xdx$. Then $du=dx$ and $v=\sin x$. Therefore
$$\int x\cos xdx=x\sin x-\int\sin xdx=x\sin x+\cos x+C.$$
Differentiating cosine repeatedly would not simplify the algebraic factor; differentiating $x$ reduces it to 1, which is why this choice is convenient.

## 5. Why Each Step Is Valid
The formula follows from the product rule and our choices satisfy $dv=d(\sin x)$ and $du=dx$.

## 6. Final Answer in Words
$\int x\cos xdx=x\sin x+\cos x+C$.

## 7. Quick Verification
The derivative is $\sin x+x\cos x-\sin x=x\cos x$.

## 8. Common Mistakes
- Forgetting the negative sign before the remaining integral.
- Integrating $\cos x$ as $-\sin x$; its antiderivative is $\sin x$.

## 9. Short In-Class Explanation
Differentiate $x$ and integrate cosine because those choices simplify the remaining integral. Applying parts gives $x\sin x+\cos x+C$, whose derivative is the original product.
