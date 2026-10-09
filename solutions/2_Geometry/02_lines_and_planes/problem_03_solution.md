# Problem 03: Plane Through a Point with a Given Normal Vector

## 1. Original Problem
Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

## 2. What We Are Trying to Find
We must construct the Cartesian equation of the plane passing through point $P$ orthogonal to normal vector $n$, verify that $P$ satisfies the derived equation, and explain the geometric role of the normal vector.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Point-Normal Form of a Plane**: A plane passing through point $P = (x_0, y_0, z_0)$ with normal vector $n = (a, b, c)$ consists of all points $X = (x, y, z)$ such that the displacement vector $\overrightarrow{PX}$ is perpendicular to $n$:
  $$n \cdot (X - P) = 0 \iff a(x - x_0) + b(y - y_0) + c(z - z_0) = 0.$$
- Expanding gives the standard form $ax + by + cz + d = 0$, where $d = -(a x_0 + b y_0 + c z_0)$.

## 4. Step-by-Step Solution

### Step 1: Set Up the Point-Normal Equation
Given point $P=(1, -2, 3)$ and normal vector $n=(2, 1, -1)$:
$$2(x - 1) + 1(y - (-2)) + (-1)(z - 3) = 0.$$
Simplify the signs:
$$2(x - 1) + 1(y + 2) - 1(z - 3) = 0.$$

### Step 2: Expand to General Form
Expand the products:
$$2x - 2 + y + 2 - z + 3 = 0.$$
Combine the constant terms:
$$(-2 + 2 + 3) = 3.$$
The general equation of the plane is:
$$2x + y - z + 3 = 0 \quad \text{or} \quad 2x + y - z = -3.$$

### Step 3: Check by Substituting Point $P$
Substitute $(x, y, z) = (1, -2, 3)$ into the left-hand side of $2x + y - z + 3 = 0$:
$$\text{LHS} = 2(1) + (-2) - 3 + 3 = 2 - 2 - 3 + 3 = 0.$$
Since $\text{LHS} = 0$, the equation is satisfied.

### Step 4: Explain the Role of the Normal Vector
The normal vector $n = (a, b, c)$ completely defines the **spatial tilt and orientation** of the plane:
1. The coefficients of $x, y, z$ in the Cartesian equation are precisely the components of $n$: $(2, 1, -1)$.
2. Any vector lying in the plane $\overrightarrow{v}$ must satisfy $n \cdot \overrightarrow{v} = 0$. The normal vector acts as a perpendicular mast: by forcing all displacement vectors from $P$ to be at a $90^\circ$ angle to $n$, it restricts points to a flat two-dimensional sheet in space.
The point $P$ fixes the plane's position in space, while $n$ determines its orientation.

## 5. Why Each Step Is Valid
- The dot product definition $n \cdot (X - P) = 0$ is the exact geometric condition for a plane in $\mathbb{R}^3$.
- Algebraic expansion and collection of constant terms preserves equality.

## 6. Final Answer in Words
The equation of the plane is $2x + y - z + 3 = 0$ (or $2x + y - z = -3$). Substituting $P(1, -2, 3)$ yields $2 - 2 - 3 + 3 = 0$, verifying the result. The normal vector $n = (2, 1, -1)$ supplies the coefficients of $x, y, z$ and fixes the orientation of the plane by requiring every direction within the plane to be perpendicular to $n$.

## 7. Quick Verification
- Test another vector in the plane: take $Q = (-1, 0, 1)$.
  $2(-1) + 0 - 1 + 3 = -2 - 1 + 3 = 0$ (lies on plane).
  Displacement $\overrightarrow{PQ} = Q - P = (-2, 2, -2)$.
  Dot product with $n$: $(-2)(2) + (2)(1) + (-2)(-1) = -4 + 2 + 2 = 0$.
  $\|\overrightarrow{PQ}\|$ is strictly perpendicular to $n$.

## 8. Common Mistakes
- Sign errors when subtracting negative coordinates: $y - (-2) = y + 2$, not $y - 2$.
- Forgetting the constant term and writing $2x + y - z = 0$ (which would describe a parallel plane through the origin, not through $P$).

## 9. Short In-Class Explanation (3 Sentences)
We substitute the point $P(1, -2, 3)$ and normal vector $n=(2, 1, -1)$ into the point-normal formula $2(x-1) + 1(y+2) - 1(z-3) = 0$, which simplifies to $2x + y - z + 3 = 0$. Substituting the coordinates of $P$ into this equation gives zero, confirming that $P$ lies on the plane. The normal vector determines the orientation of the plane by providing the coefficients of $x, y, z$, ensuring that every direction in the plane is perpendicular to $n$.
