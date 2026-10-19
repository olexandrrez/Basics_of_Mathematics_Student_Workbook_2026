# Problem 5: Distance from Velocity

## 1. Original Problem
For $v(t)=4t+2$ m/s during the first five seconds, calculate distance, explain why integration gives position change, and discuss negative velocity.

## 2. What We Are Trying to Find
We distinguish displacement (signed change in position) from total distance, which counts all motion as positive.

## 3. Key Idea or Theorem Needed Before the Calculation
Velocity is the derivative of position, so integrating velocity gives net displacement. Total distance is the integral of speed $|v|$.

## 4. Step-by-Step Solution
On $[0,5]$, $v(t)=4t+2\ge2>0$, so the object never reverses direction. Thus distance equals displacement:
$$\int_0^5(4t+2)dt=[2t^2+2t]_0^5=50+10=60\text{ m}.$$
If velocity could be negative, the signed integral would subtract backward motion. For total distance, split where velocity changes sign and integrate $|v(t)|$ instead.

## 5. Why Each Step Is Valid
The Fundamental Theorem relates the derivative of position to its net change. Positivity of velocity makes absolute value unnecessary in this case.

## 6. Final Answer in Words
The car travels 60 m in the first five seconds. With negative velocity, use the absolute value to compute total distance.

## 7. Quick Verification
Average velocity here is $(v(0)+v(5))/2=(2+22)/2=12$ m/s; over five seconds this gives 60 m, consistent with the integral.

## 8. Common Mistakes
- Calling the integral of velocity total distance when velocity changes sign.
- Integrating acceleration instead of velocity for displacement.

## 9. Short In-Class Explanation
Integrating velocity gives net position change. Here velocity is always positive, so that change is the full distance: 60 m. If velocity is negative at times, integrate its absolute value for total distance.
