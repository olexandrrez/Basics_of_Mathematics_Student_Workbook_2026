# Problem 07: A Line Relative to a Plane

## 1. Original Problem
For
$$L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,$$
determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

## 2. What We Are Trying to Find
We must determine the geometric relationship between line $L$ and plane $\Pi$ (unique intersection point, parallel and disjoint, or completely contained), and explain the theoretical diagnostic role of the dot product $v \cdot n$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Dot Product Test ($v \cdot n$)**:
  - Let $v$ be the direction vector of the line and $n$ the normal vector of the plane.
  - If $v \cdot n \neq 0$, the line is not parallel to the plane and **intersects it at exactly one point**.
  - If $v \cdot n = 0$, the line's direction is perpendicular to the normal, meaning the line is **parallel to the plane**.
- **Disjoint vs Contained**:
  - When $v \cdot n = 0$, test any single point $P_0$ of the line in the plane equation:
    - If $P_0 \in \Pi$, the line **lies entirely in the plane**.
    - If $P_0 \notin \Pi$, the line is **parallel and disjoint** (no common points).

## 4. Step-by-Step Solution

### Step 1: Identify Vectors
- For line $L: (x, y, z) = (1, 1, 0) + t(1, -1, 0)$:
  - Base point: $P_0 = (1, 1, 0)$.
  - Direction vector: $v = (1, -1, 0)$.
- For plane $\Pi: x + y + z = 2$:
  - Normal vector: $n = (1, 1, 1)$.

### Step 2: Compute the Dot Product $v \cdot n$
$$v \cdot n = (1)(1) + (-1)(1) + (0)(1) = 1 - 1 + 0 = 0.$$
Because $v \cdot n = 0$, the direction of the line is perpendicular to the normal vector $n$.
Since $n$ is perpendicular to the plane, a direction perpendicular to $n$ must run parallel to the plane.
Therefore, the line is **parallel to the plane** (it does not pierce the plane at a single point).

### Step 3: Test Whether Base Point $P_0$ Lies in the Plane
Substitute $P_0 = (1, 1, 0)$ into the plane equation $x + y + z = 2$:
$$\text{LHS} = 1 + 1 + 0 = 2.$$
$$\text{RHS} = 2.$$
Since $\text{LHS} = \text{RHS}$, point $P_0$ satisfies the equation and lies on plane $\Pi$.

### Step 4: Conclude the Relationship
Because the line is parallel to the plane ($v \cdot n = 0$) and shares at least one point $P_0$ with the plane, the line **lies entirely in the plane** ($L \subset \Pi$).

### Step 5: General Verification for Any $t$
Substitute the general point $(x(t), y(t), z(t)) = (1+t, 1-t, 0)$ into the plane:
$$(1 + t) + (1 - t) + 0 = 1 + 1 + t - t = 2.$$
The equation $2 = 2$ is satisfied for **every real number $t$**, confirming that every point on the line lies in the plane.

## 5. Why Each Step Is Valid
- The dot product $v \cdot n$ measures the rate at which moving along the line increases the value of the linear expression $n \cdot x$. When $v \cdot n = 0$, the value $n \cdot x$ is constant along the line.
- Since that constant equals the plane's target constant $2$, all points on the line lie in the plane.

## 6. Final Answer in Words
The line $L$ lies entirely in the plane $\Pi$. The dot product $v \cdot n = 0$ shows that the direction of the line is perpendicular to the normal vector, meaning the line is parallel to the plane. Testing the line's point $(1, 1, 0)$ into the plane equation gives $1 + 1 + 0 = 2$, proving that the line is contained inside the plane.

## 7. Quick Verification
- Let $t = 5$: point is $(6, -4, 0)$. Substitute: $6 + (-4) + 0 = 2$.
- Let $t = -3$: point is $(-2, 4, 0)$. Substitute: $-2 + 4 + 0 = 2$.
Every point of $L$ satisfies the plane equation.

## 8. Common Mistakes
- Concluding the line is disjointly parallel simply because $v \cdot n = 0$, forgetting to check if the line's point lies on the plane.
- Confusing $v \cdot n = 0$ with perpendicularity of the line to the plane (a line is perpendicular to a plane when $v$ is parallel to $n$, i.e. $v = c n$).

## 9. Short In-Class Explanation (3 Sentences)
We compute the dot product of the line's direction vector $(1, -1, 0)$ and the plane's normal $(1, 1, 1)$, which yields $1 - 1 + 0 = 0$. Because this dot product is zero, the line is parallel to the plane and cannot cross it at a single point. Testing the line's base point $(1, 1, 0)$ in the plane equation gives $1 + 1 + 0 = 2$, which proves that the line lies entirely inside the plane.
