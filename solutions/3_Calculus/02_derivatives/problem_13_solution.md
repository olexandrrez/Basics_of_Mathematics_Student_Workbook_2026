# Problem 13: A Multi-Layer Composition

## 1. Original Problem
Differentiate $f(x)=e^{\sin(x^2)}$. Write the nested layers and explain why the chain rule follows them in reverse order.

## 2. What We Are Trying to Find
We need to account for three nested operations: squaring, taking sine, and exponentiating with base $e$.

## 3. Key Idea or Rule Needed Before the Calculation
For a composition, multiply derivatives of successive layers. Starting with the outside operation makes the chain of dependencies explicit.

## 4. Step-by-Step Solution
The layers are $x\to x^2\to\sin(x^2)\to e^{\sin(x^2)}$. The outer exponential differentiates to itself. The sine layer contributes $\cos(x^2)$, and the innermost square contributes $2x$. Therefore
$$f'(x)=e^{\sin(x^2)}\cos(x^2)\,2x.$$

## 5. Why Each Step Is Valid
The output of each inner layer is the input of the next outer layer. A change in $x$ affects the final output through each layer, so the rates multiply. The chain rule's order is the reverse of the written nesting because we differentiate the outside operation first.

## 6. Final Answer in Words
$f'(x)=2xe^{\sin(x^2)}\cos(x^2)$.

## 7. Quick Verification
At $x=0$, the inner derivative $2x$ is zero, so the entire derivative is zero, consistent with the formula.

## 8. Common Mistakes
- Omitting $\cos(x^2)$ or $2x$.
- Differentiating only the outer exponential and treating its exponent as constant.

## 9. Short In-Class Explanation
Differentiate from the outside inward: exponential contributes itself, sine contributes cosine, and the square contributes $2x$. Multiplying these factors gives the derivative.
