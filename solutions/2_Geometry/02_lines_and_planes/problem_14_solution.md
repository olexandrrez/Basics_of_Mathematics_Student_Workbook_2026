# Problem 14: Contrast: Intersection and Parallelism

## 1. Original Problem
From the point $P=(0,0,1)$, two lines are drawn with direction vectors
$$v_1=(2,1,-1),\qquad v_2=(2,1,0).$$
For each line, analyze its position relative to the plane $z=0$.
For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

## 2. What We Are Trying to Find
We must determine the position of two lines drawn from $P = (0, 0, 1)$ with direction vectors $v_1 = (2, 1, -1)$ and $v_2 = (2, 1, 0)$ relative to the coordinate plane $z = 0$, compute the intersection point for the intersecting line, and explain how to recognize parallelism for the other line by inspecting its direction vector.

## 3. Key Idea or Theorem Needed Before the Calculation
- **The Plane $z = 0$ ($xy$-plane)**: Has normal vector $n = (0, 0, 1)$.
- **Dot Product Condition**:
  - $v \cdot n = v_3$ (the $z$-component of the direction vector).
  - If $v_3 \neq 0$, the line has vertical displacement and must pierce $z = 0$ at a single point.
  - If $v_3 = 0$, the line has zero vertical displacement; its $z$-coordinate is constant, meaning it is strictly parallel to the $xy$-plane.

## 4. Step-by-Step Solution

### Step 1: Analyze Line 1 with Direction $v_1 = (2, 1, -1)$
- Parametric equation of Line 1 through $P = (0, 0, 1)$:
  $$\begin{cases} x = 0 + 2t = 2t, \\ y = 0 + 1t = t, \\ z = 1 - t. \end{cases}$$
- Test relative to $z = 0$:
  The $z$-component of the direction vector is $-1 \neq 0$.
  The dot product with normal $n = (0, 0, 1)$ is:
  $$v_1 \cdot n = -1 \neq 0.$$
  Therefore, Line 1 is **not parallel** to the plane and **intersects the plane $z = 0$ at exactly one point**.
- Find the intersection point:
  Set $z = 0$:
  $$1 - t = 0 \implies t = 1.$$
  Substitute $t = 1$ into $x$ and $y$:
  $$x = 2(1) = 2,\qquad y = 1(1) = 1.$$
  The intersection point is:
  $$Q = (2, 1, 0).$$

### Step 2: Analyze Line 2 with Direction $v_2 = (2, 1, 0)$
- Parametric equation of Line 2 through $P = (0, 0, 1)$:
  $$\begin{cases} x = 2s, \\ y = s, \\ z = 1 + 0s = 1. \end{cases}$$
- **Recognizing Parallelism Without Solving an Equation**:
  Look at the direction vector $v_2 = (2, 1, 0)$. Its $z$-component is identically $0$.
  This means that moving along Line 2 changes only the $x$ and $y$ coordinates, while the $z$-coordinate remains permanently locked at the initial value $z = 1$.
  The plane in question is $z = 0$.
  Because every point on Line 2 has $z = 1$, and every point on the plane has $z = 0$, the line stays at a constant altitude of $1$ unit above the plane.
  Since $1 \neq 0$, Line 2 can never meet the plane.
  We recognize parallelism immediately because the $z$-component of the direction vector is zero and the point's $z$-coordinate does not match the plane's $z$-level.

## 5. Why Each Step Is Valid
- The $z$-coordinate of a point is its directed height above the $xy$-plane; a zero vertical velocity ($v_z = 0$) guarantees a constant-altitude trajectory.
- Solving $1 - t = 0$ is an exact linear equation with the unique root $t = 1$.

## 6. Final Answer in Words
Line 1 intersects the plane $z = 0$ at the point $(2, 1, 0)$. Line 2 is parallel to the plane $z = 0$ with no intersection points. Parallelism for Line 2 is recognized immediately without solving an equation because its direction vector has a $z$-component of $0$, which keeps the line at a constant height of $z = 1$ for all parameter values, never reaching $z = 0$.

## 7. Quick Verification
- Check intersection point $Q(2, 1, 0)$:
  $z = 0$ (lies on plane).
  $Q - P = (2 - 0, 1 - 0, 0 - 1) = (2, 1, -1) = 1 \cdot v_1$ (lies on Line 1). Verified!
- Check Line 2 at $s = 100$: point is $(200, 100, 1)$. $z = 1 \neq 0$. Parallelism holds for all $s$.

## 8. Common Mistakes
- Performing unnecessary algebra for Line 2 instead of explaining how to recognize parallelism directly from the zero $z$-component.
- Forgetting that the plane $z = 0$ is the $xy$-plane.

## 9. Short In-Class Explanation (3 Sentences)
For the first line, the direction vector has $z$-component $-1$, so setting $z = 1 - t = 0$ gives $t = 1$ and yields the intersection point $(2, 1, 0)$. For the second line, the $z$-component of the direction vector is zero, meaning moving along the line never changes its height from $z = 1$. Because the line remains at a constant height of $z = 1$, it is strictly parallel to the plane $z = 0$ and never intersects it.
