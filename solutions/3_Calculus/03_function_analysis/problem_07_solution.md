# Problem 7: A Trigonometric Function

## 1. Original Problem
On $[0,2\pi]$, find intervals of monotonicity and extrema for $f(x)=\sin x+\cos x$, including endpoints.

## 2. What We Are Trying to Find
We find the critical points in the closed interval, use derivative signs to determine monotonicity, and compare all critical and endpoint values for absolute extrema.

## 3. Key Idea or Theorem Needed Before the Calculation
On a closed interval, absolute extrema can occur at interior critical points or endpoints. Solve $f'=0$ and compare function values at every candidate.

## 4. Step-by-Step Solution
Differentiate: $f'(x)=\cos x-\sin x$. The zeros satisfy $\tan x=1$, giving $x=\pi/4,5\pi/4$ in $[0,2\pi]$. The derivative sign is positive on $(0,\pi/4)$, negative on $(\pi/4,5\pi/4)$ and positive on $(5\pi/4,2\pi)$.

Therefore $f$ increases, decreases, then increases. Evaluate candidates:
$$f(0)=1,\quad f(2\pi)=1,\quad f(\pi/4)=\sqrt2,\quad f(5\pi/4)=-\sqrt2.$$

## 5. Why Each Step Is Valid
The derivative sign determines monotonicity between critical points. A continuous function on a closed bounded interval attains its absolute extrema; checking endpoints as well as stationary points identifies them.

## 6. Final Answer in Words
Absolute maximum is $\sqrt2$ at $\pi/4$; absolute minimum is $-\sqrt2$ at $5\pi/4$. The function increases on $[0,\pi/4]$ and $[5\pi/4,2\pi]$, and decreases on $[\pi/4,5\pi/4]$.

## 7. Quick Verification
Using $\sin x+\cos x=\sqrt2\sin(x+\pi/4)$ confirms the range is between $-\sqrt2$ and $\sqrt2$.

## 8. Common Mistakes
- Forgetting one critical point in $[0,2\pi]$.
- Omitting the endpoint values when finding absolute extrema.

## 9. Short In-Class Explanation
Set $\cos x-\sin x=0$ to find two critical points. Check the derivative signs and compare both critical values with the endpoint values. The largest and smallest are $\sqrt2$ and $-\sqrt2$.
