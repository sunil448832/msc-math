# Unit 9 · Topic 01 — LPP: Formulation, Graphical Method and Convex Sets
> Syllabus coverage: Linear programming problem; solution of LPP by graphical method; convex set
> Cheatsheet: [../Cheatsheets/01-LPP-Formulation-Graphical-Convex-Sets.md](../Cheatsheets/01-LPP-Formulation-Graphical-Convex-Sets.md)

**Q1.** `[Concept]` ★ A system $AX=b$ of 3 linearly independent equations in 5 unknowns (the constraints of an LPP in standard form) has at most how many basic solutions?

(A) 8

(B) 10

(C) 15

(D) 60

**Q2.** `[Numerical]` ★ The maximum value of $Z = 3x + 2y$ subject to $x + y \le 4,\; x + 3y \le 6,\; x, y \ge 0$ is

(A) 11

(B) 10

(C) 12

(D) 14

**Q3.** `[Concept]` ★ Which of the following subsets of $\mathbb{R}^2$ is convex?

(A) $\{(x,y) : x^2 + y^2 \ge 1\}$

(B) $\{(x,y) : x^2 + y^2 = 1\}$

(C) $\{(x,y) : xy \le 1\}$

(D) $\{(x,y) : y \ge x^2\}$

**Q4.** `[Multi-Statement]` ★★ Consider the statements:

I. The intersection of any family of convex sets is convex.

II. The union of two convex sets is convex.

III. The set of feasible solutions of an LPP, if non-empty, is a convex set.

Which of these is/are correct?

(A) I only

(B) I and III only

(C) II and III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** If an LPP attains its optimal value at two distinct extreme points, then it has infinitely many optimal solutions.
**Reason (R):** The set of optimal solutions of an LPP is a convex set.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ (All variables $x, y \ge 0$.) Match List-I with List-II.

| List-I (LPP) | List-II (nature of solution) |
|---|---|
| A. Max $Z = 2x + 2y$, s.t. $x + y \le 4$ | 1. Unique optimal solution |
| B. Max $Z = x + y$, s.t. $x - y \le 1$ | 2. Alternative (infinitely many) optima |
| C. Max $Z = x + y$, s.t. $x + y \le 2,\; x + y \ge 3$ | 3. Unbounded solution |
| D. Max $Z = 3x + y$, s.t. $x + y \le 4,\; x \le 3$ | 4. No feasible solution |

(A) A-2, B-3, C-4, D-1

(B) A-1, B-3, C-4, D-2

(C) A-2, B-4, C-3, D-1

(D) A-3, B-2, C-4, D-1

**Q7.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true for an LPP in standard form?

(A) Every basic feasible solution corresponds to an extreme point of the feasible region, and conversely.

(B) The feasible region has only finitely many extreme points.

(C) If the feasible region is unbounded, the objective function has an unbounded optimal value.

(D) Every convex combination of two feasible solutions is a feasible solution.

**Q8.** `[Application]` ★★★ Which of the following closed convex subsets of $\mathbb{R}^2$ has **no** extreme point?

(A) The closed disc $\{(x,y) : x^2 + y^2 \le 1\}$

(B) The first quadrant $\{(x,y) : x \ge 0,\; y \ge 0\}$

(C) The half-plane $\{(x,y) : x + y \le 1\}$

(D) The triangle with vertices $(0,0), (1,0), (0,1)$

**Q9.** `[Numerical]` ★★ For the system
$$x_1 + 2x_2 + x_3 = 4, \qquad 2x_1 + x_2 + x_4 = 5, \qquad x_j \ge 0,$$
the number of basic **feasible** solutions is

(A) 6

(B) 5

(C) 3

(D) 4

**Q10.** `[Numerical]` ★★ The minimum value of $Z = x + y$ subject to $x + 2y \ge 4,\; 3x + y \ge 6,\; x, y \ge 0$ is

(A) $2$

(B) The problem is unbounded

(C) $4$

(D) $\dfrac{14}{5}$

**Q11.** `[Application]` ★★★ Consider: Max $Z = kx + y$ subject to $x + y \le 4,\; x + 2y \le 6,\; x, y \ge 0$, where $k > 0$. For which of the following values of $k$ does the problem have alternative optimal solutions?

(A) $k = 2$

(B) $k = \tfrac{1}{2}$

(C) $k = 3$

(D) $k = \tfrac{1}{3}$

**Q12.** `[Concept]` ★ To convert the constraint $2x_1 + 3x_2 \ge 6$ into an equation, one

(A) subtracts a surplus variable

(B) adds a slack variable

(C) adds an unrestricted variable

(D) multiplies by $-1$ and adds an artificial variable only

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | C | Numerical |
| 3 | D | Concept |
| 4 | B | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | A | Match |
| 7 | C | NOT-true / Counterexample |
| 8 | C | Application |
| 9 | D | Numerical |
| 10 | D | Numerical |
| 11 | B | Application |
| 12 | A | Concept |

## Solutions
**Q1 — (B).** A basic solution is obtained by choosing $m$ of the $n$ variables as basic and setting the other $n-m$ to zero, so there are at most $\binom{n}{m} = \binom{5}{3} = 10$. (C) $=\binom{6}{2}$ and (D) $=5\cdot4\cdot3$ (ordered choice) are miscounts.

**Q2 — (C).** The corner points are $(0,0), (4,0), (3,1), (0,2)$, where $Z = 0, 12, 11, 4$. So $Z_{\max} = 12$ at $(4,0)$. (A) is the value at the intersection point $(3,1)$; it is tempting to assume the optimum is always where the two constraint lines cross.

**Q3 — (D).** The epigraph of the convex function $x^2$ is convex. (A) is the outside of a disc, (B) is a circle (its chord midpoints are not on it), and (C) contains $(4, 0)$ and $(0,4)$ but not their midpoint $(2,2)$ has $xy = 4 > 1$.

**Q4 — (B).** I is true. II is false: two points of $\mathbb{R}$, or two disjoint discs, form a non-convex union. III is true because the feasible region is an intersection of half-spaces (and hyperplanes).

**Q5 — (A).** If $x^{(1)}, x^{(2)}$ are both optimal with value $Z^*$, then by linearity $\lambda x^{(1)} + (1-\lambda)x^{(2)}$ is feasible with the same value $Z^*$ for every $\lambda\in[0,1]$. This is exactly the convexity of the optimal set, so R explains A.

**Q6 — (A).** A: the objective is parallel to the binding constraint $x+y=4$, so the whole edge from $(4,0)$ to $(0,4)$ is optimal (2). B: along $x = y \to \infty$ the point stays feasible and $Z \to\infty$ (3). C: the constraints contradict each other (4). D: the corners $(0,0),(3,0),(3,1),(0,4)$ give $0, 9, 10, 4$, so $(3,1)$ is the unique optimum (1).

**Q7 — (C).** An unbounded feasible region does not imply an unbounded objective. For example, min $Z = x + y$ over $x, y \ge 0$ has optimum $0$. (A) is the fundamental theorem linking BFS and extreme points. (B) holds because there are at most $\binom{n}{m}$ BFS. (D) is convexity.

**Q8 — (C).** A half-plane contains a whole line through each of its points (a line parallel to $x+y=1$), so no point is an extreme point. The disc has infinitely many extreme points (its boundary circle), the quadrant has one ($(0,0)$), and the triangle has three. Note that "unbounded" alone does not mean "no extreme points" (see B).

**Q9 — (D).** There are $\binom42 = 6$ basic solutions:
$(x_1,x_2)=(2,1)$ ✓; $(x_1,x_3)=(2.5,1.5)$ ✓; $(x_1,x_4)=(4,-3)$ ✗; $(x_2,x_3)=(5,-6)$ ✗; $(x_2,x_4)=(2,3)$ ✓; $(x_3,x_4)=(4,5)$ ✓.
Four of them are feasible. (A) counts all basic solutions, ignoring the sign check.

**Q10 — (D).** The region is unbounded upward, with corners $(0,6), (8/5, 6/5), (4,0)$, where $Z = 6, 14/5, 4$. Since this is a minimisation with positive costs, the unbounded region does not matter, and $Z_{\min} = 14/5$. (A) ignores the constraints, and (B) confuses an unbounded region with an unbounded objective.

**Q11 — (B).** The corners are $(0,0),(4,0),(2,2),(0,3)$. Alternative optima occur when the objective is parallel to a binding edge: $kx+y$ is parallel to $x+2y=6$ when $k = \tfrac12$, which gives $Z = 2$ at $(4,0)$ and $Z = 3$ at both $(2,2)$ and $(0,3)$. So the edge between them is optimal. ($k=1$, parallel to $x+y=4$, would also work but is not offered.) For $k = 2, 3$ the unique optimum is $(4,0)$; for $k=\tfrac13$ it is $(0,3)$.

**Q12 — (A).** For "$\ge$" we write $2x_1+3x_2 - s = 6$ with surplus $s\ge0$. (An artificial variable is then added for the simplex starting basis, but it is not what turns the inequality into an equation.) Slack variables are for "$\le$".
