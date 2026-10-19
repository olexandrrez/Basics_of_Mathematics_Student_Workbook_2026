# Problem 1: Motion — from Position to Velocity

## 1. Original Problem
A point has position $s(t)=t^3-6t^2+9t+2$ for $t\ge0$. Find velocity, acceleration, stopping times, and direction of motion.

## 2. What We Are Trying to Find
Position is given, and derivatives convert it into velocity and acceleration. The sign of velocity determines direction; its zeros identify moments at rest.

## 3. Key Idea or Theorem Needed Before the Calculation
Velocity is $s'(t)$ and acceleration is $v'(t)=s''(t)$. Positive velocity means motion in the positive axis direction; negative velocity means motion in the negative direction.

## 4. Step-by-Step Solution
Differentiate position:
$$v(t)=s'(t)=3t^2-12t+9=3(t-1)(t-3).$$
Differentiate again:
$$a(t)=v'(t)=6t-12.$$
Set velocity to zero: $3(t-1)(t-3)=0$ gives $t=1$ and $t=3$. On $[0,1)$ both factors are negative, so $v>0$. On $(1,3)$ the factors have opposite signs, so $v<0$. For $t>3$ both are positive, so $v>0$.

## 5. Why Each Step Is Valid
The roots split the nonnegative time axis into intervals on which a continuous velocity cannot change sign without another zero. The sign directly gives direction.

## 6. Final Answer in Words
$v(t)=3(t-1)(t-3)$, $a(t)=6t-12$. The point stops at 1 and 3 seconds, moves forward on $[0,1)$ and $(3,\infty)$, and backward on $(1,3)$.

## 7. Quick Verification
At times 0, 2, and 4, velocity signs are respectively positive, negative, positive, matching the classification.

## 8. Common Mistakes
- Confusing acceleration zero ($t=2$) with stopping time.
- Saying negative velocity means negative speed; it means direction is negative.

## 9. Short In-Class Explanation
Differentiate position for velocity and velocity for acceleration. Factor velocity to find stops at 1 and 3, then inspect its sign between and outside those roots.
