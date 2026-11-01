# Cheatsheet · Unit 9 · Topic 04 — Transportation and Assignment Problems
> Questions: [../Questions/04-Transportation-Assignment.md](../Questions/04-Transportation-Assignment.md)

## 1. Transportation problem (TP)
$$\min \sum_{i=1}^m\sum_{j=1}^n c_{ij}x_{ij}\quad\text{s.t.}\quad \sum_j x_{ij} = a_i\ (\text{supply}),\ \ \sum_i x_{ij} = b_j\ (\text{demand}),\ \ x_{ij}\ge0.$$
- **Balanced:** $\sum a_i = \sum b_j$. A balanced TP **always** has a feasible solution, e.g. $x_{ij} = a_ib_j/\sum a_i$, and an optimal one (the region is bounded).
- **Unbalanced:**
  - $\sum a_i > \sum b_j$: add a **dummy destination** (column) with demand $\sum a_i-\sum b_j$ and zero cost (or the storage cost).
  - $\sum a_i < \sum b_j$: add a **dummy origin** (row) with zero cost (or the shortage penalty).
- There are $mn$ variables and $m+n$ constraints, of rank $m+n-1$ (one constraint is redundant).
- **Number of basic variables = $m+n-1$.** A BFS with fewer positive cells is **degenerate**.
- Basic cells never form a **closed loop**. For each non-basic cell there is a unique loop through it and basic cells.
- **Integrality:** the constraint matrix is totally unimodular, so with integer $a_i,b_j$ every BFS (hence some optimum) is integral.
- The TP is a special LPP. Its dual is: max $\sum a_iu_i+\sum b_jv_j$ s.t. $u_i+v_j\le c_{ij}$, with $u,v$ unrestricted (equality constraints).

## 2. Initial BFS methods

| Method | Rule | Quality |
|---|---|---|
| North-West Corner (NWCR) | start at cell (1,1), allocate $\min(a_i,b_j)$, move right/down | ignores cost, usually worst |
| Least Cost (Matrix Minima, LCM) | allocate to the cheapest remaining cell | better |
| Vogel's Approximation (VAM) | penalty = difference of the two smallest costs in each row/column; take the row/column with the largest penalty and allocate to its cheapest cell | usually best, often optimal or near-optimal, but **not guaranteed** |

When an allocation satisfies a row and a column simultaneously, cross out only one (keep the other with a zero allocation) to preserve $m+n-1$ cells.

**Standard example** (costs $[[19,30,50,10],[70,30,40,60],[40,8,70,20]]$, supply $(7,9,18)$, demand $(5,8,7,14)$): NWCR $=1015$, LCM $=814$, VAM $=779$, optimum $=743$.

## 3. Optimality test: MODI (u–v) method
1. Take a BFS with $m+n-1$ independent occupied cells.
2. Solve $u_i+v_j = c_{ij}$ for the **occupied** cells. Set one variable (usually the $u$ of the row with the most allocations) to $0$.
3. For each empty cell compute $d_{ij} = c_{ij}-(u_i+v_j)$, the opportunity cost or reduced cost.
4. If **all $d_{ij}\ge0$**, the solution is optimal. All $d_{ij}>0$ means a unique optimum; some $d_{ij}=0$ means alternative optima.
5. Otherwise, enter the cell with the most negative $d_{ij}$. Form its closed loop (alternate $+,-$), set $\theta = $ the minimum allocation on the "$-$" corners, adjust, and repeat.
- **Stepping-stone method:** computes the same $d_{ij}$ directly by evaluating loops.
- The cost decreases by $\theta\lvert d_{ij}\rvert$.

## 4. Degeneracy in a TP
- It occurs when the number of occupied cells is $< m+n-1$, either initially or when two cells hit zero simultaneously during a loop adjustment.
- **Resolution:** put $\varepsilon$ (a tiny positive amount) in an independent empty cell (one that creates no loop), preferably a least-cost one. Let $\varepsilon\to0$ at the end.

## 5. Assignment problem (AP)
$n$ jobs and $n$ machines; $x_{ij}\in\{0,1\}$; each row and each column has exactly one $1$; minimise $\sum c_{ij}x_{ij}$.
- It is a special TP with all $a_i = b_j = 1$, and it is **always degenerate**: there are $n$ positive cells versus the $2n-1$ needed, so MODI is inefficient and the **Hungarian method** is used.
- The LP relaxation has integral optimal vertices (Birkhoff–von Neumann: doubly stochastic matrices are convex combinations of permutation matrices).
- The number of feasible assignments is $n!$.

### Hungarian method (Kuhn, from König–Egerváry)
1. **Row reduction:** subtract each row's minimum. **Column reduction:** subtract each column's minimum.
2. Cover all zeros with the **minimum number of lines** $L$ (König's theorem: $L$ = the maximum number of independent zeros).
3. If $L = n$, an optimal assignment exists among the zeros. Assign row by row or column by column using single zeros.
4. If $L<n$, let $k$ = the smallest uncovered entry. Subtract $k$ from every uncovered entry and add $k$ at each **intersection** of two lines. Go to 2.

**Key facts**
- Adding or subtracting a constant from a whole row or column does not change the optimal assignment (the total changes by that constant).
- **Unbalanced** (non-square) problem: add dummy rows or columns with zero cost.
- **Maximisation:** replace $a_{ij}$ by $(\max a_{ij}) - a_{ij}$ (or by $-a_{ij}$) and minimise.
- **Prohibited assignment:** put cost $M$ (very large; $\infty$) in that cell.
- **Travelling salesman problem:** an AP with the extra "no subtours" condition, with $c_{ii} = \infty$.

## Exam traps
- The basic count is $m+n-1$ for the **balanced** (augmented) matrix. Add the dummy first.
- A dummy row means demand > supply; a dummy column means supply > demand.
- In MODI, $u_i+v_j=c_{ij}$ only on **occupied** cells. The $d_{ij}$ sign convention matters: for a min problem, $d_{ij}\ge 0$ for all cells means optimal.
- VAM and LCM give **initial** solutions, not guaranteed optimal ones. Always test with MODI.
- A maximisation AP must be converted before the Hungarian method; otherwise you minimise the profit.
- An assignment problem is a degenerate TP. Degeneracy in a TP is resolved with $\varepsilon$, not by changing the costs.
- In the Hungarian step, add $k$ at the **intersections** and leave the singly-covered entries unchanged.
