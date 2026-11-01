# Cheatsheet · Unit 9 · Topic 02 — Simplex Method, Big-M and Two-Phase
> Questions: [../Questions/02-Simplex-BigM-Two-Phase.md](../Questions/02-Simplex-BigM-Two-Phase.md)

## 1. Setup
Standard form: Max $Z=c^Tx$, $Ax=b$, $x\ge0$, $b\ge0$, with $A$ of size $m\times n$.
- Basis matrix $B$ ($m$ columns). $x_B = B^{-1}b$, $Z = c_B^TB^{-1}b$.
- Updated column: $y_j = B^{-1}a_j$. $Z_j = c_B^T y_j$. Net evaluation $\Delta_j = Z_j - C_j$ (for basic variables $\Delta_j = 0$).
- Some books use $C_j - Z_j$, which reverses every sign rule below. **Always check the convention.**

## 2. Simplex algorithm (Max, $\Delta_j = Z_j-C_j$)
1. Find an initial BFS. With all constraints $\le$ and $b\ge0$, use the slacks as the basis ($B=I$).
2. **Optimality test:** if all $\Delta_j\ge0$, the current BFS is optimal.
3. **Entering variable:** the most negative $\Delta_j$ (Dantzig). Its column is the **key column** $k$.
4. **Unboundedness test:** if all $y_{ik}\le0$, the solution is unbounded. Stop.
5. **Leaving variable (minimum ratio test):** $\displaystyle\theta=\min_{i:\thinspace y_{ik}\gt 0}\frac{x_{B_i}}{y_{ik}}$. That row $r$ is the **key row**, and $y_{rk}$ is the **pivot**.
6. **Pivot:** divide the key row by the pivot, then make the other entries of column $k$ zero (Gauss–Jordan). Go to 2.

- **Change in $Z$ per iteration:** $Z_{\text{new}} = Z_{\text{old}} - \theta\thinspace \Delta_k = Z_{\text{old}}+\theta\lvert\Delta_k\rvert$.
- **Min problem:** either maximise $-Z$, or use the reversed rules (enter the most positive $\Delta_j$; optimal when all $\Delta_j\le0$).
- Each iteration moves to an **adjacent** extreme point (one basic variable is exchanged).

## 3. Reading the final tableau

| Observation (max, $\Delta = Z-C$) | Conclusion |
|---|---|
| All $\Delta_j\ge0$ | optimal |
| $\Delta_j=0$ for some **non-basic** $x_j$ at the optimum | alternative optima (if a pivot with $\theta\gt 0$ is possible) |
| $\Delta_k\lt 0$ and column $k\le0$ | unbounded solution |
| Tie in the ratio test / a basic variable $=0$ | degeneracy (possible cycling) |
| Optimal, but an artificial variable is basic at a **positive** level | infeasible |
| Optimal, artificial basic at level **zero** | feasible; possible redundant constraint (degenerate) |
| $\Delta_j$ of a slack $s_i$ at the optimum | shadow price $= y_i^\ast$ of resource $i$ (Topic 03) |

## 4. Degeneracy and cycling
- **Degenerate BFS:** some basic variable $=0$. A pivot with $\theta = 0$ changes the basis but not the point or $Z$.
- **Cycling:** the sequence of bases repeats, so the method never terminates. It is possible only under degeneracy and is very rare in practice (Beale's example).
- **Anti-cycling:** Bland's smallest-index rule, the lexicographic rule, or the perturbation (Charnes) method.
- Without cycling, simplex terminates in at most $\binom{n}{m}$ iterations. The worst case is exponential (Klee–Minty), while ellipsoid and interior-point methods are polynomial.

## 5. Artificial variables
They are needed for rows with "$`\ge`$" (after subtracting the surplus) and "$`=`$", where no identity column is available. First make every $`b_i\ge0`$ (a row with $`b_i\lt 0`$ flips $`\le \leftrightarrow \ge`$).

| Constraint (with $b\ge0$) | Add |
|---|---|
| $\le$ | $+s$ (slack), which is basic |
| $`\ge`$ | $-s$ (surplus) $+R$ (artificial) |
| $`=`$ | $+R$ |

### Big-M (penalty) method
- Max: objective $c^Tx - M\sum R_i$. Min: objective $c^Tx + M\sum R_i$, with $M\gg0$.
- First make the $\Delta_j$ of the initial artificial basis consistent: subtract $M\times$ the rows from the $\Delta$ row, so that the basic $\Delta_j = 0$.
- Once an artificial variable leaves the basis, its column can be dropped.
- **Infeasible** if the optimum has some $R_i\gt 0$ in the basis. **Unbounded** is detected as usual.
- Drawbacks: the size of $M$ is arbitrary, and a large $M$ causes round-off errors.

### Two-phase method
- **Phase I:** Min $W=\sum R_i$ (equivalently Max $-\sum R_i$) subject to the same constraints.
  - $W^\ast \gt 0$ means the LPP is **infeasible**. Stop.
  - $W^\ast =0$ with no artificial in the basis: go to Phase II.
  - $W^\ast =0$ with an artificial basic at zero: pivot it out, or keep it (a redundant constraint).
- **Phase II:** take the final Phase I tableau, delete the artificial columns, restore the original objective, recompute the $\Delta_j$, and continue the simplex method.
- Phase I never detects unboundedness of the original problem ($W\ge0$ is always bounded below).

## 6. Worked standard results
- Max $3x_1+5x_2$, $x_1\le4$, $2x_2\le12$, $3x_1+2x_2\le18$: optimum $(2,6)$, $Z=36$, shadow prices $(0, 3/2, 1)$.
- Min $4x_1+x_2$, $3x_1+x_2=3$, $4x_1+3x_2\ge6$, $x_1+2x_2\le4$: optimum $(2/5, 9/5)$, $Z=17/5$ (Big-M or two-phase).

## Exam traps
- In the ratio test, **ignore zero and negative** entries of the key column; do not take a negative ratio as the "minimum".
- Make $b_i\ge0$ **before** deciding slack/surplus/artificial; a negative RHS flips the inequality.
- The entering criterion is reversed for min problems and for the $C_j-Z_j$ convention.
- A zero $\Delta_j$ for a **basic** variable means nothing; only a non-basic zero signals alternative optima.
- Degeneracy $\ne$ cycling. Degeneracy is necessary for cycling but not sufficient.
- A left variable **can** re-enter later; only a repeated **basis** (cycling) is the problem.
- An artificial variable at a positive level at the optimum means infeasible; at level zero it does not.
- Big-M penalty: $-M$ for max and $+M$ for min (the penalty must make the objective worse).
