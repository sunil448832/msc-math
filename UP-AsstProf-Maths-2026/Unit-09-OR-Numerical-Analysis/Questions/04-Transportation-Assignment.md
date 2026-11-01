# Unit 9 · Topic 04 — Transportation and Assignment Problems
> Syllabus coverage: Balanced and unbalanced transportation problems; Hungarian method for solving assignment problems
> Cheatsheet: [../Cheatsheets/04-Transportation-Assignment.md](../Cheatsheets/04-Transportation-Assignment.md)

*Data used in Q3–Q5 (unit costs, supplies $`a_i`$, demands $`b_j`$):*

| | $D_1$ | $D_2$ | $D_3$ | $D_4$ | Supply |
|---|---|---|---|---|---|
| $O_1$ | 19 | 30 | 50 | 10 | 7 |
| $O_2$ | 70 | 30 | 40 | 60 | 9 |
| $O_3$ | 40 | 8 | 70 | 20 | 18 |
| Demand | 5 | 8 | 7 | 14 | 34 |

**Q1.** `[Concept]` ★ A non-degenerate basic feasible solution of a balanced transportation problem with 4 origins and 5 destinations has exactly how many positive allocations?

(A) 9

(B) 8

(C) 20

(D) 5

**Q2.** `[Concept]` ★ A transportation problem with total supply 500 and total demand 450 is solved by

(A) adding a dummy origin with supply 50 and zero costs

(B) reducing every supply proportionally

(C) adding a dummy destination with demand 50 and cost $M$ in every cell

(D) adding a dummy destination with demand 50 and zero costs

**Q3.** `[Numerical]` ★★ For the data table above, the total cost of the initial basic feasible solution given by the **North-West Corner Rule** is

(A) 779

(B) 814

(C) 1015

(D) 1105

**Q4.** `[Numerical]` ★★★ For the same data, the initial solution by **Vogel's Approximation Method** costs

(A) 743

(B) 779

(C) 814

(D) 1015

**Q5.** `[Numerical]` ★★★ For the same data, take the NWCR solution with basic cells
$x_{11}=5,\ x_{12}=2,\ x_{22}=6,\ x_{23}=3,\ x_{33}=4,\ x_{34}=14$. Using the MODI method with $u_1 = 0$, the opportunity cost $d_{32} = c_{32} - (u_3 + v_2)$ of the empty cell $(3,2)$ is

(A) $-22$

(B) $52$

(C) $-52$

(D) $38$

**Q6.** `[Multi-Statement]` ★★ For an $m\times n$ transportation problem:

I. A balanced transportation problem always has a feasible solution.

II. If all supplies and demands are integers, every basic feasible solution is integer-valued.

III. All $m+n$ supply and demand constraints are linearly independent.

Which is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** An $n\times n$ assignment problem, viewed as a transportation problem, is always highly degenerate.
**Reason (R):** Every feasible assignment has exactly $n$ positive allocations, whereas a non-degenerate basic solution of an $n\times n$ transportation problem needs $2n-1$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match List-I with List-II.

| List-I | List-II |
|---|---|
| A. Degeneracy in a transportation problem | 1. Assign a very large cost $M$ to that cell |
| B. Unbalanced transportation problem | 2. Number of occupied cells $\lt  m+n-1$ |
| C. Maximisation assignment problem | 3. Add a dummy row/column with zero costs |
| D. Prohibited (infeasible) assignment | 4. Subtract every entry from the largest entry |

(A) A-2, B-3, C-1, D-4

(B) A-3, B-2, C-4, D-1

(C) A-2, B-3, C-4, D-1

(D) A-2, B-4, C-3, D-1

**Q9.** `[Numerical]` ★★ The minimum total cost of the assignment problem with cost matrix (rows = jobs, columns = machines)
```math
\begin{pmatrix} 10 & 12 & 19 & 11\cr  5 & 10 & 7 & 8\cr  12 & 14 & 13 & 11\cr  8 & 15 & 11 & 9\end{pmatrix}
```
is

(A) 36

(B) 38

(C) 39

(D) 41

**Q10.** `[Application]` ★★★ Four salesmen are to be assigned to four territories, one each. The expected **profits** are
```math
\begin{pmatrix} 16 & 10 & 14 & 11\cr  14 & 11 & 15 & 15\cr  15 & 15 & 13 & 12\cr  13 & 12 & 14 & 15\end{pmatrix}.
```
The maximum total profit is

(A) 58

(B) 59

(C) 60

(D) 61

**Q11.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) In the Hungarian method, an unbalanced (non-square) assignment problem is first made square by adding dummy rows or columns with zero cost.

(B) Adding the same constant to every entry of a row of the cost matrix does not change the optimal assignment.

(C) In the Hungarian method, an optimal assignment can be made when the minimum number of lines covering all zeros equals the order $n$.

(D) Vogel's Approximation Method always gives an optimal solution of a transportation problem.

**Q12.** `[Application]` ★★ Three factories with total supply 150 units serve four markets with total demand 180 units. After balancing, the number of basic variables in any non-degenerate BFS is

(A) 7

(B) 6

(C) 8

(D) 12

**Q13.** `[Concept]` ★ In the MODI (u–v) method for a minimisation transportation problem, the current basic feasible solution is optimal when

(A) $c_{ij} - (u_i + v_j) \ge 0$ for every non-basic cell

(B) $c_{ij} - (u_i + v_j) \le 0$ for every non-basic cell

(C) $u_i + v_j = c_{ij}$ for every cell

(D) all $u_i$ and $v_j$ are non-negative

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | D | Concept |
| 3 | C | Numerical |
| 4 | B | Numerical |
| 5 | C | Numerical |
| 6 | B | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | C | Match |
| 9 | B | Numerical |
| 10 | D | Application |
| 11 | D | NOT-true / Counterexample |
| 12 | A | Application |
| 13 | A | Concept |

## Solutions
**Q1 — (B).** The number of basic cells is $m+n-1 = 4+5-1 = 8$, because one of the $m+n$ constraints is redundant. (A) forgets the redundancy.

**Q2 — (D).** Supply exceeds demand, so the excess $50$ goes to a **dummy destination** (column) with zero cost, which absorbs the unshipped stock. A dummy origin is used when demand exceeds supply.

**Q3 — (C).** NWCR: $x_{11}=5,\ x_{12}=2,\ x_{22}=6,\ x_{23}=3,\ x_{33}=4,\ x_{34}=14$. The cost is $95+60+180+120+280+280 = 1015$. (B) is the Least Cost Method value, (A) is VAM.

**Q4 — (B).** VAM penalties pick column $D_2$ (penalty 22), so $x_{32}=8$. Then $D_1$ (21) gives $x_{11}=5$. Then row $O_3$ (50) gives $x_{34}=10$. Then $D_4$ gives $x_{14}=2$, and finally $x_{23}=7,\ x_{24}=2$. The cost is $95\thinspace (x_{11})+20\thinspace (x_{14})+280\thinspace (x_{23})+120\thinspace (x_{24})+64\thinspace (x_{32})+200\thinspace (x_{34}) = 779$. The true optimum is $743$ (A), so VAM is close to it but not optimal here.

**Q5 — (C).** Using $u_i+v_j=c_{ij}$ on the basic cells: $u_1=0$ gives $v_1=19, v_2=30$; then $u_2 = 0$, $v_3=40$, $u_3 = 70-40 = 30$, $v_4 = 20-30=-10$. So $d_{32} = 8-(30+30) = -52\lt 0$, and bringing cell $(3,2)$ in reduces the cost. (A) forgets $u_3$, and (B) has the wrong sign.

**Q6 — (B).** I: $x_{ij} = a_ib_j/\sum a_i$ is feasible. II: the constraint matrix is totally unimodular, so every BFS is integral. III is false: the sum of the row constraints equals the sum of the column constraints, so the rank is $m+n-1$.

**Q7 — (A).** A BFS needs $2n-1$ basic cells, but an assignment has only $n$ ones; the remaining $n-1$ basic variables are zero. R is exactly why the problem is degenerate, which is also why the Hungarian method is used instead of MODI.

**Q8 — (C).** Degeneracy means fewer than $m+n-1$ occupied cells (2). Unbalanced means a dummy with zero cost (3). Maximisation means converting to a "regret/loss" matrix via $\max - a_{ij}$ (4). A forbidden cell gets cost $M$ (1).

**Q9 — (B).** The Hungarian method (verified by full enumeration) gives Job1→M2 (12), Job2→M3 (7), Job3→M4 (11), Job4→M1 (8), for a total of $38$. (A) is too small to be attainable, and (C), (D) are other feasible assignments.

**Q10 — (D).** Subtract every entry from $16$ and minimise the resulting loss matrix. The optimal assignment is S1→T1 (16), S2→T3 (15), S3→T2 (15), S4→T4 (15), for a total profit $=61$. Running the Hungarian method directly on the profits (minimising) would give the *worst* assignment.

**Q11 — (D).** VAM gives only a good **initial** BFS, and its optimality must be tested by MODI. In the table above VAM gives $779$ while the optimum is $743$. (B) holds because every assignment uses exactly one cell of that row, so the total changes by the same constant.

**Q12 — (A).** Demand exceeds supply, so add a dummy factory (supply 30). The problem becomes $4\times4$, with $m+n-1 = 4+4-1 = 7$ basic variables. (B) uses the unbalanced size $3+4-1$.

**Q13 — (A).** $d_{ij} = c_{ij}-(u_i+v_j)$ is the net change in cost per unit shipped through the empty cell $(i,j)$. If no $d_{ij}$ is negative, no improvement is possible. If all $d_{ij}\gt 0$ the optimum is unique; a zero $d_{ij}$ signals an alternative optimum. (C) holds only on **basic** cells.
