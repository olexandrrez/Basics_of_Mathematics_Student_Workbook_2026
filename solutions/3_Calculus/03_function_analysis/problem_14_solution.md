# Problem 14: Reconstructing Information from the Derivative

## 1. Original Problem
Given $f'(x)=(x-1)(x+2)$, determine monotonicity and extrema and sketch a possible shape. Verify the same derivative for $g(x)=x^3/3+x^2/2-2x$.

## 2. What We Are Trying to Find
We infer the shape from the derivative alone, then use the specified function as a concrete example and calculate its turning-point heights.

## 3. Key Idea or Theorem Needed Before the Calculation
The zeros of $f'$ divide the real line into intervals. Test the derivative sign on each interval; sign changes classify extrema. Any functions with the same derivative differ by a constant.

## 4. Step-by-Step Solution
The roots are $-2$ and 1. For $x<-2$, both factors are negative, so their product is positive. Between $-2$ and 1 the factors have opposite signs, so the product is negative. For $x>1$, both are positive. Thus the function increases, decreases, then increases, with local maximum at $-2$ and local minimum at 1.

For the example,
$$g'(x)=x^2+x-2=(x-1)(x+2).$$
Its values are $g(-2)=-8/3+2+4=10/3$ and $g(1)=1/3+1/2-2=-7/6$.

## 5. Why Each Step Is Valid
The derivative sign gives monotonicity independently of the function's vertical position. Integrating a derivative determines an antiderivative up to an additive constant, which shifts the graph vertically but preserves its shape.

## 6. Final Answer in Words
Every such function has a local maximum at $x=-2$ and a local minimum at $x=1$. For $g$, these points are $(-2,10/3)$ and $(1,-7/6)$.

## 7. Quick Verification
Factoring $g'=x^2+x-2$ reproduces the given derivative. The sign chart $+,-,+$ agrees with the rise-fall-rise sketch.

## 8. Common Mistakes
- Trying to determine absolute heights from $f'$ alone; a constant of integration is unknown.
- Misreading the sign between the roots.

## 9. Short In-Class Explanation
The derivative is positive before $-2$, negative until 1, then positive. So the graph has a maximum followed by a minimum. The example $g$ has the same shape, with heights found by substitution.

```text
y           • local max
↑         ／ ＼
|       ／     ＼
|     ／         ＼       ／
|   ／             ＼___／  local min
+---------−2----------1------------→ x
```
