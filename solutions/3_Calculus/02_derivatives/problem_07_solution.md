# Problem 7: A Trigonometric Composition

## 1. Original Problem
For $f(x)=\sin(x^2+1)$, identify outer and inner functions, find the derivative, and determine its sign at zero.

## 2. What We Are Trying to Find
The input to sine is itself a function. We will account for how that inner input changes, then evaluate the result at zero.

## 3. Key Idea or Rule Needed Before the Calculation
The chain rule gives $(\sin u(x))'=\cos(u(x))u'(x)$.

## 4. Step-by-Step Solution
The inner function is $u=x^2+1$, whose derivative is $2x$. The outer function is sine, whose derivative is cosine. Therefore
$$f'(x)=2x\cos(x^2+1).$$
At $x=0$, $f'(0)=0\cdot\cos1=0$.

## 5. Why Each Step Is Valid
The cosine term is the derivative of the outer sine, evaluated at its original input. The factor $2x$ is the derivative of that input. Since the latter is zero at zero, the product is zero regardless of $\cos1$.

## 6. Final Answer in Words
$f'(x)=2x\cos(x^2+1)$, and its value at zero is zero, neither positive nor negative.

## 7. Quick Verification
Directly substitute $x=0$ in the formula; the result is zero. The function itself has value $\sin1$ there, so the horizontal slope does not mean the function value is zero.

## 8. Common Mistakes
- Writing only $\cos(x^2+1)$ and omitting $2x$.
- Saying the derivative is positive or negative at zero even though it equals zero.

## 9. Short In-Class Explanation
Differentiate the outside sine to get cosine of the same input, then multiply by the derivative $2x$ of the inside. At zero this factor vanishes, so the derivative is zero.
