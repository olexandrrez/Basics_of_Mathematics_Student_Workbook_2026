# Problem 1: A Cubic Polynomial

## 1. Original Problem
Analyze monotonicity and extrema of $f(x)=x^3-3x^2+2$. Sketch the graph and mark the critical points.

## 2. What We Are Trying to Find
We use the first derivative to find where the function can change direction, classify each critical point, and collect end behavior for a qualitative graph.

## 3. Key Idea or Theorem Needed Before the Calculation
A differentiable function increases where $f'>0$ and decreases where $f'<0$. A sign change $+\to-$ gives a local maximum; $-\to+$ gives a local minimum.

## 4. Step-by-Step Solution
Differentiate and factor:
$$f'(x)=3x^2-6x=3x(x-2).$$
Critical values are $x=0,2$. Testing intervals gives $f'>0$ for $x<0$, $f'<0$ for $0<x<2$, and $f'>0$ for $x>2$. Thus $f$ increases, decreases, then increases. Function values are $f(0)=2$ and $f(2)=-2$. The leading cubic term gives $f\to-\infty$ as $x\to-\infty$ and $f\to+\infty$ as $x\to+\infty$.

## 5. Why Each Step Is Valid
The derivative sign determines local change. Since its sign reverses at both critical values, they are extrema: a maximum at $(0,2)$ and minimum at $(2,-2)$.

## 6. Final Answer in Words
Increasing on $(-\infty,0)$ and $(2,\infty)$; decreasing on $(0,2)$. Local maximum $(0,2)$, local minimum $(2,-2)$.

## 7. Quick Verification
$ f'(x)$ has roots exactly at 0 and 2. Substitution into the original polynomial confirms the two marked heights.

## 8. Common Mistakes
- Giving critical $x$-values without evaluating the function there.
- Assuming every critical point is a maximum or minimum without checking signs.

## 9. Short In-Class Explanation
The derivative factors as $3x(x-2)$, giving critical values 0 and 2. Its signs are positive, negative, positive, so the curve rises, falls, rises. The turning points are $(0,2)$ and $(2,-2)$.

```text
y                  • (0,2)
↑              ／￣     ￣＼
|           ／             ＼
|         ／                 ＼
|       ／                     • (2,−2) ／
+------------------------------------------→ x
```
