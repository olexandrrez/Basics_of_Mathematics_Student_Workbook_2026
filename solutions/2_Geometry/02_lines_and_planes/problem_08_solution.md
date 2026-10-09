# Problem 08: Intersection Point of a Line and a Plane

## 1. Original Problem
Find the intersection point of
$$(x,y,z)=(1,0,2)+t(1,2,-1)$$
with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

## 2. What We Are Trying to Find
We must determine the spatial coordinates of the single point where line $L$ pierces plane $\Pi$, and verify the answer by checking that the point lies both on the line and in the plane.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Parametric-to-Cartesian Substitution**: Write the line in parametric coordinate form $x(t), y(t), z(t)$.
- Substitute these expressions into the Cartesian plane equation $A x(t) + B y(t) + C z(t) = D$.
- Solve the resulting single linear equation for the parameter $t$.
- Substitute $t$ back into the line equation to obtain the coordinates of the intersection point.

## 4. Step-by-Step Solution

### Step 1: Write Parametric Equations of the Line
From $(x, y, z) = (1, 0, 2) + t(1, 2, -1)$:
$$\begin{cases} x = 1 + t, \\ y = 2t, \\ z = 2 - t. \end{cases}$$

### Step 2: Substitute into the Plane Equation
The plane is $x + y + z = 4$.
Substitute $x(t), y(t), z(t)$:
$$(1 + t) + (2t) + (2 - t) = 4.$$

### Step 3: Solve for Parameter $t$
Simplify the left-hand side:
$$(1 + 2) + (t + 2t - t) = 4 \implies 3 + 2t = 4.$$
Subtract 3 from both sides:
$$2t = 1 \implies t = \frac{1}{2}.$$

### Step 4: Compute the Intersection Point
Substitute $t = 1/2$ back into the line equations:
$$x = 1 + \frac{1}{2} = \frac{3}{2} = 1.5,$$
$$y = 2\left(\frac{1}{2}\right) = 1,$$
$$z = 2 - \frac{1}{2} = \frac{3}{2} = 1.5.$$
The intersection point is:
$$P = \left(\frac{3}{2}, 1, \frac{3}{2}\right) = (1.5, 1, 1.5).$$

### Step 5: Check by Substituting into Both Descriptions
1. **Check in Plane**:
   Substitute $(3/2, 1, 3/2)$ into $x + y + z = 4$:
   $$\frac{3}{2} + 1 + \frac{3}{2} = 3 + 1 = 4.$$
   $4 = 4$, True! The point lies on the plane.
2. **Check on Line**:
   Subtract base point $(1, 0, 2)$ from $P$:
   $$P - P_0 = \left(\frac{3}{2} - 1, 1 - 0, \frac{3}{2} - 2\right) = \left(\frac{1}{2}, 1, -\frac{1}{2}\right) = \frac{1}{2}(1, 2, -1) = \frac{1}{2}v.$$
   This matches the direction vector scaled by $t = 1/2$. The point lies on the line.

## 5. Why Each Step Is Valid
- Substituting parametric formulas translates the geometric intersection into a 1D algebraic equation.
- Since the coefficient of $t$ is $v \cdot n = 1 + 2 - 1 = 2 \neq 0$, the linear equation has a unique solution $t = 1/2$.

## 6. Final Answer in Words
The intersection point of the line and the plane is $P = (3/2, 1, 3/2) = (1.5, 1, 1.5)$. Substituting these coordinates into the plane equation yields $1.5 + 1 + 1.5 = 4$, and subtracting the base point of the line yields $0.5(1, 2, -1)$, confirming that the point lies on both objects.

## 7. Quick Verification
- Compute dot product $v \cdot n = (1)(1) + (2)(1) + (-1)(1) = 2 \neq 0$.
  By formula: $t = \frac{d - n \cdot P_0}{n \cdot v} = \frac{4 - (1+0+2)}{2} = \frac{4 - 3}{2} = \frac{1}{2}$.
  This confirms $t = 1/2$ by the projection formula.

## 8. Common Mistakes
- Miscomputing $t - t$: forgetting that $t + 2t - t = 2t$.
- Forgetting to substitute $t$ back into the line equations to find the coordinates $(x, y, z)$.

## 9. Short In-Class Explanation (3 Sentences)
We substitute the parametric coordinates $x = 1+t$, $y = 2t$, and $z = 2-t$ into the plane equation to get $3 + 2t = 4$. Solving this gives parameter value $t = 1/2$. Substituting $t = 1/2$ back into the line equation yields the intersection point $(1.5, 1, 1.5)$, which satisfies both the line and plane equations upon verification.
