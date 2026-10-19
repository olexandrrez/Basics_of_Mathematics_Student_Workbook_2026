# Problem 9: Minimizing the Material Used for a Can

## 1. Original Problem
A closed cylinder has fixed volume $V$. Write the surface area as a function of radius and find the minimizing relation between $h$ and $r$.

## 2. What We Are Trying to Find
The problem has two dimensions but a volume constraint. We eliminate height to obtain a one-variable surface-area function and optimize it.

## 3. Key Idea or Theorem Needed Before the Calculation
Cylinder volume is $\pi r^2h$; closed surface area is two circles plus the curved side, $2\pi r^2+2\pi rh$. Use the constraint to substitute for $h$.

## 4. Step-by-Step Solution
From $V=\pi r^2h$, get $h=V/(\pi r^2)$. Then
$$S(r)=2\pi r^2+2\pi r\frac{V}{\pi r^2}=2\pi r^2+\frac{2V}{r},\quad r>0.$$
Differentiate:
$$S'(r)=4\pi r-\frac{2V}{r^2}.$$
Set $S'=0$: $4\pi r^3=2V$, or $V=2\pi r^3$. Since $V=\pi r^2h$, divide by $\pi r^2$ to obtain $h=2r$. Also $S''=4\pi+4V/r^3>0$; and $S\to\infty$ as $r\to0^+$ or $r\to\infty$.

## 5. Why Each Step Is Valid
The constraint keeps volume fixed while radius varies. Positive second derivative and divergent endpoint behavior establish this critical point is the global minimum.

## 6. Final Answer in Words
Material usage is minimized when cylinder height equals its diameter: $h=2r$.

## 7. Quick Verification
Substituting $h=2r$ into volume gives $V=2\pi r^3$, exactly the stationary condition.

## 8. Common Mistakes
- Using only the lateral area for a closed cylinder and omitting the two lids.
- Optimizing with $r,h$ independent of the fixed-volume constraint.

## 9. Short In-Class Explanation
Use the volume constraint to replace height in the surface area. Differentiate the resulting function of radius; its minimum condition simplifies to $h=2r$.
