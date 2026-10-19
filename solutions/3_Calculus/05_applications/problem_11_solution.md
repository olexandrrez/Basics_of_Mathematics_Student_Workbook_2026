# Problem 11: Volume of a Solid of Revolution

## 1. Original Problem
Rotate the region under $y=\sqrt{x}$ for $x\in[0,4]$ around the $x$-axis. Set up and calculate the volume using disks.

## 2. What We Are Trying to Find
We add the volumes of thin circular slices perpendicular to the axis of rotation.

## 3. Key Idea or Theorem Needed Before the Calculation
A disk of radius $r$ has area $\pi r^2$. A thin slice of thickness $dx$ has volume approximately this area times $dx$, and integration accumulates the slices.

## 4. Step-by-Step Solution
At each $x$, the radius is the distance from the $x$-axis to the curve, $r=y=\sqrt{x}$. Therefore cross-sectional area is $\pi(\sqrt{x})^2=\pi x$. Integrate from 0 to 4:
$$V=\pi\int_0^4x dx=\pi\left[\frac{x^2}{2}\right]_0^4=8\pi.$$

## 5. Why Each Step Is Valid
The region touches the axis, so each cross-section is a full disk rather than a washer with a hole. The radius is nonnegative on the interval.

## 6. Final Answer in Words
The solid's volume is $8\pi$ cubic units.

## 7. Quick Verification
The integrand $\pi x$ increases linearly from 0 to $4\pi$ over length 4; its triangular area is $\frac12(4)(4\pi)=8\pi$.

## 8. Common Mistakes
- Using $y$ instead of $y^2$ in the disk area.
- Forgetting the factor $\pi$.

## 9. Short In-Class Explanation
Each slice is a disk with radius $\sqrt{x}$ and area $\pi x$. Integrating those areas over 0 to 4 gives $8\pi$.
