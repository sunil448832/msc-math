# Unit 9 · Topic 02 — Simplex Method, Big-M Technique and Two-Phase Method
> Syllabus coverage: Solution of linear programming problem by simplex method; Big M-technique; Two-phase method
> Cheatsheet: [../Cheatsheets/02-Simplex-BigM-Two-Phase.md](../Cheatsheets/02-Simplex-BigM-Two-Phase.md)

*Convention used throughout: $\Delta_j = Z_j - C_j$ is the net-evaluation (index) row, where $Z_j = C_B^T B^{-1}a_j$.*

**Q1.** `[Concept]` ★ In the simplex method for a **maximisation** problem (using $\Delta_j = Z_j - C_j$), the entering variable is the one with

(A) the most positive $\Delta_j$

(B) the largest cost coefficient $C_j$, regardless of $\Delta_j$

(C) the smallest positive ratio $x_{B_i}/a_{ij}$

(D) the most negative $\Delta_j$

**Q2.** `[Concept]` ★ A basic feasible solution is called **degenerate** if

(A) some non-basic variable is positive

(B) the objective function is zero

(C) at least one basic variable is zero

(D) two variables have the same $\Delta_j$

**Q3.** `[Numerical]` ★★ Solving Max $Z = 3x_1 + 5x_2$ subject to $x_1 \le 4,\; 2x_2 \le 12,\; 3x_1 + 2x_2 \le 18,\; x_1,x_2\ge0$ by the simplex method gives the optimal value

(A) 27

(B) 30

(C) 36

(D) 42

**Q4.** `[Numerical]` ★★ In a simplex tableau (max problem), $x_1$ has been selected to enter. Its column and the current solution are:

| Basic | $x_B$ | $x_1$ column |
|---|---|---|
| $s_1$ | 24 | 4 |
| $s_2$ | 12 | 3 |
| $s_3$ | 2 | $-2$ |

The leaving variable and the pivot element are

(A) $s_1$, pivot 4

(B) $s_2$, pivot 3

(C) $s_3$, pivot $-2$

(D) $s_1$, pivot 3

**Q5.** `[Multi-Statement]` ★★ Regarding the two-phase method:

I. Phase I minimises the sum of the artificial variables subject to the original constraints.

II. If the optimal value of the Phase I objective is positive, the original LPP has no feasible solution.

III. Artificial variables are needed for every constraint of the type "$\le$" with a non-negative right-hand side.

Which is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q6.** `[Assertion-Reason]` ★★
**Assertion (A):** If, in an optimal simplex tableau of a maximisation problem, $\Delta_j = 0$ for some non-basic variable $x_j$, then the problem may have alternative optimal solutions.
**Reason (R):** Bringing such an $x_j$ into the basis at level $\theta$ changes the value of $Z$ by $-\theta\,\Delta_j$, which is $0$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ (Max problem, $\Delta_j = Z_j - C_j$.) Match the tableau indication in List-I with its conclusion in List-II.

| List-I | List-II |
|---|---|
| A. All $\Delta_j \ge 0$, no artificial variable positive | 1. No feasible solution |
| B. $\Delta_k < 0$ and every entry of column $k$ is $\le 0$ | 2. Unbounded solution |
| C. Tie in the minimum ratio test | 3. Optimal solution reached |
| D. All $\Delta_j\ge0$ but an artificial variable is basic at a positive level | 4. Next BFS will be degenerate |

(A) A-3, B-2, C-1, D-4

(B) A-3, B-2, C-4, D-1

(C) A-2, B-3, C-4, D-1

(D) A-3, B-4, C-2, D-1

**Q8.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) In the Big-M method for a minimisation problem, the artificial variables get cost $+M$ in the objective.

(B) Every simplex tableau of an $m$-constraint problem has exactly $m$ basic variables.

(C) Degeneracy in an LPP always leads to cycling in the simplex method.

(D) Slack variables have zero coefficient in the objective function.

**Q9.** `[Numerical]` ★★★ Using the Big-M method, the optimal value of
$$\text{Min } Z = 4x_1 + x_2 \ \text{ s.t. } \ 3x_1 + x_2 = 3,\;\; 4x_1 + 3x_2 \ge 6,\;\; x_1 + 2x_2 \le 4,\;\; x_1,x_2\ge0$$
is

(A) $3$

(B) $4$

(C) $\dfrac{18}{5}$

(D) $\dfrac{17}{5}$

**Q10.** `[Application]` ★★ The constraints of an LPP are
$$x_1 + x_2 \le 4,\quad 2x_1 + x_2 \ge 3,\quad x_1 - x_2 = 1,\quad -x_1 + x_2 \ge -2,\quad x_1, x_2 \ge 0.$$
The minimum number of artificial variables needed to get an initial basic feasible solution for the simplex method is

(A) 1

(B) 2

(C) 3

(D) 4

**Q11.** `[Application]` ★★★ Phase I of the two-phase method is applied to: Max $Z = x_1 + x_2$ subject to $x_1 + x_2 \le 2,\; x_1 + x_2 \ge 4,\; x_1,x_2\ge 0$. The optimal value of the Phase I objective (sum of the artificial variables) and the conclusion are

(A) 0; the problem has an optimal solution

(B) 2; the problem is unbounded

(C) 4; the problem is unbounded

(D) 2; the problem is infeasible

**Q12.** `[Multi-Statement]` ★★★ Consider the following about the (primal) simplex method:

I. In a non-degenerate iteration of a maximisation problem, the value of $Z$ strictly increases.

II. Each iteration moves from an extreme point of the feasible region to an adjacent extreme point (or stays at the same point in a degenerate pivot).

III. A variable that leaves the basis can never re-enter it in a later iteration.

Which is/are correct?

(A) I and II only

(B) II only

(C) I and III only

(D) I, II and III

**Q13.** `[Concept]` ★ In a simplex tableau of a maximisation problem, $x_k$ has $\Delta_k<0$ and every entry $a_{ik}$ of its column is $\le 0$. Then the LPP has

(A) an unbounded solution

(B) no feasible solution

(C) a degenerate optimal solution

(D) alternative optimal solutions

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | C | Concept |
| 3 | C | Numerical |
| 4 | B | Numerical |
| 5 | B | Multi-Statement |
| 6 | A | Assertion-Reason |
| 7 | B | Match |
| 8 | C | NOT-true / Counterexample |
| 9 | D | Numerical |
| 10 | B | Application |
| 11 | D | Application |
| 12 | A | Multi-Statement |
| 13 | A | Concept |

## Solutions
**Q1 — (D).** $\Delta_j<0$ means that increasing $x_j$ increases $Z$ at the rate $-\Delta_j$, so we pick the most negative $\Delta_j$ (Dantzig's rule). (C) is the rule for the **leaving** variable, and (A) is the entering rule for a min problem.

**Q2 — (C).** Degenerate means a basic variable has value zero. Non-basic variables are always $0$, so (A) is impossible.

**Q3 — (C).** The simplex method enters $x_2$ (ratio $12/2=6$), then $x_1$ (ratio $6/3 = 2$), reaching $(x_1,x_2)=(2,6)$ with $Z=6+30=36$. The final $\Delta$'s for the slacks are $(0, 3/2, 1)\ge0$. (A) is the value at $(4,3)$ and (B) at $(0,6)$, both earlier corner points. (D) comes from $(4,6)$, which is infeasible.

**Q4 — (B).** The ratio test uses only **positive** entries: $24/4 = 6$, $12/3 = 4$, and $s_3$ is excluded since $-2<0$. The minimum is $4$, so $s_2$ leaves and the pivot is $3$. (A) picks the largest coefficient. (C) wrongly takes the "ratio" $2/(-2)=-1$ as the smallest.

**Q5 — (B).** I and II describe Phase I correctly. III is false: a "$\le$" constraint with $b\ge0$ has its slack as a ready basic variable. Artificials are needed for "$\ge$" and "$=$" constraints.

**Q6 — (A).** The new objective value is $Z' = Z - \theta\Delta_j$. With $\Delta_j=0$ the new BFS (if $\theta>0$) is also optimal, so there are alternative optima, and so infinitely many by convexity. R is exactly why A holds. ("May" covers the degenerate case $\theta = 0$.)

**Q7 — (B).** The optimality test passes (3). An improving direction that no constraint stops gives an unbounded solution (2). A tie in the ratio test makes the other tied basic variable $0$ next time, which is degeneracy (4). An artificial variable stuck at a positive level means infeasible (1).

**Q8 — (C).** Degeneracy **can** cause cycling, but this is rare; most degenerate problems do not cycle, and Bland's rule or lexicographic rules prevent it. (A), (B) and (D) are standard facts. (In a max problem the penalty is $-M$.)

**Q9 — (D).** Big-M: introduce $R_1$ (in the equation), the surplus $s_2$ with $R_2$, and the slack $s_3$. Iterating gives $x_1 = \tfrac25,\ x_2 = \tfrac95$ with $Z = \tfrac85 + \tfrac95 = \tfrac{17}{5}$. Check: $3(2/5)+9/5 = 3$ ✓, $8/5+27/5 = 7\ge 6$ ✓, $2/5+18/5=4\le4$ ✓. (C) is the value at the intermediate point $(3/5, 6/5)$, where $Z = 12/5+6/5 = 18/5$, which is feasible but not optimal.

**Q10 — (B).** Row 1 is "$\le$" and gets a slack. Row 2 is "$\ge$" and needs an artificial. Row 3 is "$=$" and needs an artificial. Row 4 has a negative RHS, so multiply by $-1$: $x_1 - x_2 \le 2$, which gets a slack. Total: **2**. (C) forgets to make the right-hand side non-negative first.

**Q11 — (D).** Phase I: Min $R$ with $x_1+x_2+s_1 = 2$ and $x_1+x_2 - s_2 + R = 4$. Since $R = 4 - (x_1+x_2) + s_2$ and $x_1+x_2 \le 2$, the minimum is $R = 2 > 0$. So the original problem is infeasible. Unboundedness is never detected in Phase I.

**Q12 — (A).** I: $Z$ changes by $\theta\,|\Delta_k|>0$ when $\theta>0$. II: adjacent BFS differ in one basic variable, which is an edge move. III is false: a variable that leaves can re-enter later (and does so routinely). What cannot repeat, without cycling, is an entire **basis**.

**Q13 — (A).** If no $a_{ik}>0$, the ratio test has no candidate. $x_k$ can then increase indefinitely while every basic variable stays $\ge0$, and $Z\to\infty$. So the solution is unbounded (the region is unbounded too).
