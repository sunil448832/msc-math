# Cheatsheet · Unit 9 · Topic 01 — LPP: Formulation, Graphical Method and Convex Sets
> Questions: [../Questions/01-LPP-Formulation-Graphical-Convex-Sets.md](../Questions/01-LPP-Formulation-Graphical-Convex-Sets.md)

## 1. Forms of an LPP
- **General:** optimise $Z = c^T x$ subject to $\le, =, \ge$ constraints, with some variables $\ge 0$ and some unrestricted.
- **Canonical (max):** Max $c^Tx$, $Ax \le b$, $x \ge 0$.
- **Standard:** Max/Min $c^Tx$, $Ax = b$, $x \ge 0$, $b \ge 0$ (multiply a row by $-1$ if $b_i\lt 0$).
- **Conversions**

| Situation | Action |
|---|---|
| $a^Tx \le b$ | add a **slack** $s\ge0$: $a^Tx + s = b$ |
| $a^Tx \ge b$ | subtract a **surplus** $s\ge0$: $a^Tx - s = b$ |
| $x_j$ unrestricted | $x_j = x_j' - x_j''$ with $x_j', x_j''\ge0$ |
| $x_j \le 0$ | $x_j = -x_j'$ |
| Min $Z$ | Max $(-Z)$; then $Z_{\min} = -(\max(-Z))$ |
| $b_i\lt 0$ | multiply the row by $-1$ (the inequality flips) |

- **Formulation steps:** (1) decision variables, (2) objective, (3) constraints, (4) non-negativity. Classic examples: product mix, diet problem, blending, transportation.

## 2. Convex sets
- $S\subseteq\mathbb R^n$ is **convex** if $x,y\in S,\ \lambda\in[0,1] \Rightarrow \lambda x+(1-\lambda)y\in S$.
- **Convex combination:** $\sum \lambda_i x_i$ with $\lambda_i\ge0$, $\sum\lambda_i=1$. The **convex hull** is the set of all convex combinations, i.e. the smallest convex set containing the points.
- **Extreme point:** $x\in S$ is extreme if it cannot be written as $\lambda y+(1-\lambda)z$ with $y\ne z \in S$ and $0\lt \lambda\lt 1$.
- **Hyperplane** $\lbrace a^Tx=b\rbrace$, **closed/open half-spaces** $\lbrace a^Tx\le b\rbrace$ / $\lbrace a^Tx\lt b\rbrace$: all are convex.
- **Convex polyhedron** = intersection of finitely many closed half-spaces. A **polytope** is a bounded polyhedron = convex hull of finitely many points (its extreme points).

**Standard facts**
- An intersection of convex sets is convex. A **union** need **not** be convex.
- Sum $S+T$ and scalar multiple $\alpha S$ of convex sets are convex.
- Convex: a disc, a ball, $\lbrace y\ge x^2\rbrace$ (epigraph of a convex function), any affine subspace, a hyperplane, a half-space, $\mathbb R^n$, $\emptyset$, a single point.
- Not convex: a circle $x^2+y^2=1$, the region $x^2+y^2\ge1$, $\lbrace xy\le1\rbrace$, $\lbrace xy\ge1\rbrace$ (two branches; but $\lbrace xy\ge1, x\gt 0\rbrace$ **is** convex), a union of two disjoint sets, $\mathbb{Z}$.

| Set | Number of extreme points |
|---|---|
| Closed disc / ball | infinitely many (the whole boundary sphere) |
| Polygon with $k$ vertices | $k$ |
| $\lbrace x\ge0,y\ge0\rbrace$ | 1 (origin) |
| Half-plane, line, $\mathbb R^n$, open disc | **0** |
| $\lbrace \lvert x\rvert+\lvert y\rvert\le1\rbrace$ | 4: $(\pm1,0),(0,\pm1)$ |
| Closed square $[0,1]^2$ | 4 |

- **Krein–Milman (finite-dim):** a compact convex set is the convex hull of its extreme points.
- A non-empty closed convex set has an extreme point $\iff$ it contains no line.

## 3. Basic solutions
- $Ax=b$ with $A$ of size $m\times n$, $\mathop{\mathrm{rank}}\nolimits A = m \lt  n$.
- **Basic solution:** choose $m$ columns forming a non-singular $B$; set the other $n-m$ (**non-basic**) variables to $0$; then $x_B = B^{-1}b$.
- **Maximum number of basic solutions** $= \binom{n}{m}$. This is also an upper bound on the number of BFS and of extreme points.
- **Basic feasible solution (BFS):** a basic solution with $x_B\ge0$. **Degenerate BFS:** at least one basic variable $=0$.
- A basic solution has at most $m$ non-zero variables.

**Fundamental theorems**
1. The feasible set $\lbrace Ax=b,\ x\ge0\rbrace$ is convex (a polyhedron).
2. $x$ is a BFS $\iff$ $x$ is an extreme point of the feasible region.
3. If an LPP has an optimal solution, then at least one optimal solution is a BFS (extreme point), provided the feasible region has an extreme point. This is why the graphical and simplex methods check only the corners.
4. The set of optimal solutions is convex. Two distinct optimal points imply infinitely many (the whole segment between them).
5. A local optimum of an LPP is global (a linear function on a convex set).

## 4. Graphical method (2 variables)
1. Draw each constraint line, shade the feasible side, and find the feasible region (a convex polygon, possibly unbounded).
2. List the corner points: solve pairs of boundary lines and keep the feasible solutions.
3. Evaluate $Z$ at each corner (or slide an iso-profit line $c_1x+c_2y=k$).
4. **Unbounded region:** for **max** with a direction $d$ in the region and $c^Td\gt 0$ the objective is unbounded. Otherwise the best corner is optimal. A min problem with positive costs over an unbounded region is usually fine.

| Situation | Graphical symptom |
|---|---|
| Unique optimum | the iso-profit line touches a single vertex |
| Alternative optima | the objective is **parallel to a binding edge** ($c_1/c_2 = a_1/a_2$) |
| Unbounded solution | the region is unbounded **in an improving direction** |
| Infeasible | the half-planes have an empty intersection (e.g. $x+y\le2,\ x+y\ge3$) |
| Redundant constraint | removing it does not change the region |

**Alternative-optima trick:** for Max $kx+y$ over a polygon, find the slopes of the edges adjacent to the optimal vertex. Alternative optima occur exactly when $-k$ equals the slope of an edge where the optimum sits (and that edge is on the "improving" side).

## Exam traps
- An **unbounded feasible region does not imply an unbounded solution**. That depends on the objective (and on max vs min).
- Count the basic solutions using $\binom{n}{m}$ with $n$ = **total** variables, including slacks. Then check the **feasibility** of each one to count the BFS; also discard the singular choices of $B$.
- A degenerate BFS can correspond to several bases, so #bases $\ge$ #BFS.
- The union of convex sets is not convex. A circle (the boundary) is not convex, but a disc is.
- A half-plane is convex but has **no** extreme points; an open set has no extreme points.
- The optimum is attained at a vertex **if it exists**, but it may also be attained at non-vertex points (alternative optima).
- "Surplus" belongs to $\ge$ and "slack" to $\le$. Artificial variables are only a simplex device (Topic 02).
