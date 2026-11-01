# Unit 9 · Topic 03 — Dual Problem and Duality Theorems
> Syllabus coverage: Dual problem and duality theorem
> Cheatsheet: [../Cheatsheets/03-Duality.md](../Cheatsheets/03-Duality.md)

**Q1.** `[Concept]` ★ The dual of the dual of a linear programming problem is

(A) the dual itself

(B) the primal

(C) an unbounded problem

(D) not defined in general

**Q2.** `[Numerical]` ★ The dual of Max $Z = 2x_1 + 3x_2$ subject to $x_1 + 2x_2 \le 4,\; 3x_1 + x_2 \le 6,\; x_1,x_2\ge0$ is

(A) Min $W = 4y_1 + 6y_2$ s.t. $y_1 + 3y_2 \ge 2,\; 2y_1 + y_2 \ge 3,\; y_1,y_2\ge0$

(B) Min $W = 4y_1 + 6y_2$ s.t. $y_1 + 2y_2 \ge 2,\; 3y_1 + y_2 \ge 3,\; y_1,y_2\ge0$

(C) Min $W = 2y_1 + 3y_2$ s.t. $y_1 + 3y_2 \ge 4,\; 2y_1 + y_2 \ge 6,\; y_1,y_2\ge0$

(D) Min $W = 4y_1 + 6y_2$ s.t. $y_1 + 3y_2 \le 2,\; 2y_1 + y_2 \le 3,\; y_1,y_2\ge0$

**Q3.** `[Concept]` ★ If the $i$-th constraint of the primal is an **equation**, then the $i$-th dual variable is

(A) non-negative

(B) non-positive

(C) unrestricted in sign

(D) zero

**Q4.** `[Numerical]` ★★ For a maximisation LPP, a feasible solution with $Z = 10$ is known, and a feasible solution of its dual with $W = 12$ is known. Which of the following could be the common optimal value of the two problems?

(A) 9

(B) 11

(C) 12.5

(D) 14

**Q5.** `[Multi-Statement]` ★★ For a primal–dual pair of LPPs:

I. If the primal has an unbounded objective, then the dual is infeasible.

II. If the primal is infeasible, then the dual must have an unbounded objective.

III. It is possible for both the primal and the dual to be infeasible.

Which is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q6.** `[Assertion-Reason]` ★★
**Assertion (A):** If the primal (max) LPP has a finite optimal solution, then the dual also has a finite optimal solution and $\max Z = \min W$.
**Reason (R):** For any feasible $x$ of the primal and any feasible $y$ of the dual, $c^Tx \le b^Ty$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Numerical]` ★★★ The LPP Max $Z = 3x_1 + 5x_2$ s.t. $x_1 \le 4,\; 2x_2\le12,\; 3x_1 + 2x_2 \le 18,\; x_1,x_2\ge0$ has the optimal solution $x_1 = 2,\; x_2 = 6$. Using complementary slackness, the optimal dual solution $(y_1, y_2, y_3)$ is

(A) $(0, \tfrac32, 1)$

(B) $(1, \tfrac32, 0)$

(C) $(0, 1, \tfrac32)$

(D) $(3, \tfrac52, 0)$

**Q8.** `[Match]` ★★ For a primal in the form Max $c^Tx$, match List-I (primal feature) with List-II (corresponding dual feature).

| List-I (Primal, Max) | List-II (Dual, Min) |
|---|---|
| A. $i$-th constraint is "$\le$" | 1. $j$-th dual constraint is an equation |
| B. $i$-th constraint is "$=$" | 2. $i$-th dual variable $y_i\ge0$ |
| C. $j$-th variable $x_j$ unrestricted | 3. Number of dual variables |
| D. Number of primal constraints | 4. $i$-th dual variable unrestricted |

(A) A-2, B-1, C-4, D-3

(B) A-4, B-2, C-1, D-3

(C) A-2, B-4, C-1, D-3

(D) A-2, B-4, C-3, D-1

**Q9.** `[Application]` ★★★ The optimal simplex tableau of Max $Z = 5x_1 + 4x_2$ s.t. $6x_1+4x_2\le24$ (resource 1), $x_1+2x_2\le6$ (resource 2), $x_1,x_2\ge0$ is

| Basic | $x_1$ | $x_2$ | $s_1$ | $s_2$ | $x_B$ |
|---|---|---|---|---|---|
| $x_1$ | 1 | 0 | $1/4$ | $-1/2$ | 3 |
| $x_2$ | 0 | 1 | $-1/8$ | $3/4$ | $3/2$ |
| $\Delta_j = Z_j-C_j$ | 0 | 0 | $3/4$ | $1/2$ | 21 |

If the availability of resource 2 is increased from 6 to 7, the new optimal value of $Z$ is

(A) 21.5

(B) 21.75

(C) 22

(D) 25

**Q10.** `[NOT-true / Counterexample]` ★★ At a pair of optimal solutions $x^*$ (primal, max) and $y^*$ (dual), which of the following is NOT necessarily true?

(A) If the primal has $m$ constraints and $n$ variables, the dual has $n$ constraints and $m$ variables.

(B) If the $i$-th primal constraint is satisfied with strict inequality, then $y_i^* = 0$.

(C) If $y_i^*>0$, then the $i$-th primal constraint holds with equality.

(D) If $x_j^* = 0$, then the $j$-th dual constraint holds with strict inequality.

**Q11.** `[Application]` ★★ The dual of: Min $Z = 2x_1 + 3x_2$ s.t. $x_1 + x_2 \ge 5,\; x_1 - x_2 = 1,\; x_1\ge0,\; x_2$ unrestricted, is

(A) Min $W = 5y_1 + y_2$ s.t. $y_1 + y_2 \ge 2,\; y_1 - y_2 = 3,\; y_1\ge0,\; y_2$ unrestricted

(B) Max $W = 5y_1 + y_2$ s.t. $y_1 + y_2 \le 2,\; y_1 - y_2 \le 3,\; y_1\ge0,\; y_2$ unrestricted

(C) Max $W = 5y_1 + y_2$ s.t. $y_1 + y_2 \le 2,\; y_1 - y_2 = 3,\; y_1,y_2\ge0$

(D) Max $W = 5y_1 + y_2$ s.t. $y_1 + y_2 \le 2,\; y_1 - y_2 = 3,\; y_1\ge0,\; y_2$ unrestricted

**Q12.** `[Numerical]` ★★ The optimal value of
$$\text{Min } W = 2y_1 + 3y_2 + 4y_3 \ \text{ s.t. }\ y_1 + y_3 \ge 1,\;\; y_2 + y_3\ge1,\;\; y_1,y_2,y_3\ge0$$
is

(A) 2

(B) 9

(C) 5

(D) 4

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | A | Numerical |
| 3 | C | Concept |
| 4 | B | Numerical |
| 5 | C | Multi-Statement |
| 6 | B | Assertion-Reason |
| 7 | A | Numerical |
| 8 | C | Match |
| 9 | A | Application |
| 10 | D | NOT-true / Counterexample |
| 11 | D | Application |
| 12 | D | Numerical |

## Solutions
**Q1 — (B).** Duality is involutive: $(P^*)^* = P$.

**Q2 — (A).** The dual variables match the constraints, and the RHS $(4,6)$ becomes the cost vector. The constraint matrix is transposed: column of $x_1$ is $(1,3)$, giving $y_1+3y_2\ge2$; column of $x_2$ is $(2,1)$, giving $2y_1+y_2\ge3$. (B) forgets to transpose. (C) swaps $b$ and $c$ without transposing. (D) has the wrong inequality direction.

**Q3 — (C).** An equality constraint corresponds to an unrestricted dual variable, and an unrestricted primal variable corresponds to an equality dual constraint.

**Q4 — (B).** By weak duality every primal value is $\le$ every dual value, so $10\le Z^* = W^*\le12$. Only $11$ lies in $[10,12]$.

**Q5 — (C).** I follows from weak duality: a feasible $y$ would bound $Z$. II is false: if the primal is infeasible, the dual is either unbounded **or** infeasible. III is true, e.g. Max $x_1 + x_2$ s.t. $x_1 - x_2\le -1,\ -x_1 + x_2 \le -1$ (adding them gives $0\le-2$), and its dual has the same (infeasible) structure.

**Q6 — (B).** A is the strong duality theorem and R is weak duality; both are true. Weak duality alone gives only $\max Z\le\min W$. It does not show that the dual has an optimum or that the gap is zero; that needs, e.g., the simplex argument $y^T = c_B^TB^{-1}$ or Farkas' lemma.

**Q7 — (A).** Constraint 1: $x_1 = 2 < 4$ is slack, so $y_1 = 0$. Since $x_1,x_2>0$, both dual constraints are tight: $y_1 + 3y_3 = 3 \Rightarrow y_3 = 1$, and $2y_2 + 2y_3 = 5 \Rightarrow y_2 = \tfrac32$. Check: $W = 4(0) + 12(\tfrac32) + 18(1) = 36 = Z^*$ ✓. (C) swaps $y_2,y_3$; (B) and (D) violate $y_1=0$.

**Q8 — (C).** For a max primal: $\le$ gives $y_i\ge0$; $=$ gives $y_i$ unrestricted; $x_j$ unrestricted gives the $j$-th dual constraint as an equation; and #primal constraints = #dual variables.

**Q9 — (A).** The $\Delta$ entry under $s_2$, $\tfrac12$, is the shadow price $y_2^*$. The new basic solution is $x_B = B^{-1}b' = (3,\,\tfrac32) + 1\cdot(-\tfrac12,\ \tfrac34) = (2.5, 2.25)\ge0$, so the basis stays optimal and $Z = 21 + \tfrac12(1) = 21.5$. Check: $5(2.5)+4(2.25) = 21.5$ ✓. (B) uses $3/4$, the price of resource 1.

**Q10 — (D).** Complementary slackness gives $x_j^*\,(\text{surplus of dual constraint } j) = 0$. It does **not** force strict inequality when $x_j^* = 0$, because both can be zero (degeneracy, or alternative optima). (B) and (C) are complementary slackness, and (A) is the definition.

**Q11 — (D).** For a min primal: a "$\ge$" constraint gives $y_1\ge0$, and an "$=$" constraint gives $y_2$ unrestricted. $x_1\ge0$ gives the dual constraint $y_1 + y_2 \le 2$, and $x_2$ unrestricted gives the **equation** $y_1 - y_2 = 3$. Both optima equal $12$ (primal $(3,2)$, dual $(2.5,-0.5)$). Note that $y_2^* < 0$, so (C) would even change the answer.

**Q12 — (D).** This is the dual of Max $x_1 + x_2$ s.t. $x_1\le2,\ x_2\le3,\ x_1+x_2\le4$, whose optimum is clearly $4$. By strong duality $W^* = 4$, attained at $y = (0,0,1)$. (C) $=2+3$ comes from $y=(1,1,0)$, which is feasible but not optimal.
