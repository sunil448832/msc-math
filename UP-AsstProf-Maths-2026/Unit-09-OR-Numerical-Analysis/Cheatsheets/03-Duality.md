# Cheatsheet · Unit 9 · Topic 03 — Duality
> Questions: [../Questions/03-Duality.md](../Questions/03-Duality.md)

## 1. Symmetric (canonical) pair
$$\textbf{(P)}\ \max\ c^Tx,\ Ax\le b,\ x\ge0 \qquad\Longleftrightarrow\qquad \textbf{(D)}\ \min\ b^Ty,\ A^Ty\ge c,\ y\ge0$$
- $A$ is $m\times n$, so (P) has $m$ constraints and $n$ variables, and (D) has $n$ constraints and $m$ variables.
- RHS of P = cost vector of D, and cost of P = RHS of D. The constraint matrix is **transposed**.
- The dual of the dual is the primal.

## 2. Construction table (primal = Max)

| Primal (Max) | Dual (Min) |
|---|---|
| $`i`$-th constraint $`\le`$ | $`y_i\ge0`$ |
| $i$-th constraint $\ge$ | $y_i\le0$ |
| $`i`$-th constraint $`=`$ | $`y_i`$ unrestricted |
| $x_j\ge0$ | $j$-th constraint $\ge$ |
| $`x_j\le0`$ | $`j`$-th constraint $`\le`$ |
| $`x_j`$ unrestricted | $`j`$-th constraint $`=`$ |

Read the table right to left for a Min primal: for Min P, $`\ge`$ gives $`y_i\ge0`$, $`=`$ gives $`y_i`$ free, $`x_j\ge0`$ gives a "$`\le`$" dual constraint, and $`x_j`$ free gives "$`=`$".
Shortcut: first bring the problem to the "natural" form (Max with $`\le`$, or Min with $`\ge`$), then write the symmetric dual.

**Standard form pair:** $\max c^Tx,\ Ax=b,\ x\ge0$ $\leftrightarrow$ $\min b^Ty,\ A^Ty\ge c$, $y$ unrestricted.

## 3. Duality theorems
- **Weak duality:** $x$ feasible for P and $y$ feasible for D imply $c^Tx\le b^Ty$.
  - If $c^Tx = b^Ty$ for feasible $x,y$, then both are optimal.
  - P unbounded implies D infeasible, and D unbounded implies P infeasible.
- **Strong duality (fundamental duality theorem):** if either problem has a finite optimum, so does the other, and $\max Z = \min W$.
- **Existence theorem (four cases):**

| | D feasible | D infeasible |
|---|---|---|
| **P feasible** | both have optima, equal values | P unbounded |
| **P infeasible** | D unbounded | possible (both infeasible) |

  So "P infeasible implies D unbounded" is **false** in general: D may be infeasible too.
- **Complementary slackness:** feasible $x^\ast , y^\ast$ are optimal **iff**
  $$y_i^\ast \thinspace (b_i - a_i^Tx^\ast ) = 0\ \ \forall i, \qquad x_j^\ast \thinspace \big((A^Ty^\ast )_j - c_j\big) = 0\ \ \forall j.$$
  - Strict primal constraint ($i$ slack) gives $y_i^\ast =0$. $y_i^\ast \gt 0$ gives a tight constraint $i$.
  - $x_j^\ast \gt 0$ gives a tight $j$-th dual constraint.
  - The converses are **not** forced: both factors can be $0$.
- **Farkas' lemma** (the theorem of alternatives behind strong duality): exactly one of $\lbrace Ax=b,\ x\ge0\rbrace$ and $\lbrace A^Ty\ge0,\ b^Ty\lt 0\rbrace$ has a solution.

## 4. Reading the dual from the optimal simplex tableau (Max, $`\le`$ constraints, slacks $s_i$)
- $y^{\ast T} = c_B^TB^{-1}$ (the **simplex multipliers**).
- $y_i^\ast  = \Delta$ of slack $s_i$ in the final $Z_j-C_j$ row.
- If constraint $i$ had a surplus/artificial instead: $y_i^\ast  = -(\Delta \text{ of the surplus})$, or $\Delta$ of the artificial with its $\pm M$ removed. Use signs consistently.
- $\Delta_j$ for an original $x_j$ = surplus of the $j$-th dual constraint.
- Conversely, the primal optimum can be read from the dual's final tableau.

**Shadow price / economic meaning.** $y_i^\ast$ is the marginal value of resource $i$: $\partial Z^\ast /\partial b_i = y_i^\ast$, valid while $B^{-1}b'\ge0$ (the basis stays optimal).
New $Z^\ast  = Z^\ast  + y_i^\ast \thinspace \Delta b_i$ inside that range. A resource with slack has shadow price $0$.

**Example.** Max $5x_1+4x_2$, $6x_1+4x_2\le24$, $x_1+2x_2\le6$: $x^\ast =(3,1.5)$, $Z^\ast =21$, $y^\ast =(3/4,1/2)$, and $W^\ast =24\cdot\tfrac34+6\cdot\tfrac12=21$.
Wyndor: Max $3x_1+5x_2$ ($x_1\le4$, $2x_2\le12$, $3x_1+2x_2\le18$): $x^\ast =(2,6)$, $y^\ast =(0,3/2,1)$, value 36.

## 5. Dual simplex method (related)
- Starts from a tableau that is optimal ($\Delta\ge0$) but infeasible (some $x_B\lt 0$).
- Leaving variable: the most negative $x_{B_r}$. Entering variable: $\min\lbrace \lvert\Delta_j/y_{rj}\rvert : y_{rj}\lt 0\rbrace$.
- If no $y_{rj}\lt 0$, the primal is infeasible.
- Used after adding a constraint, or for Min problems with $\ge$ constraints and positive costs.

## Exam traps
- **Transpose** $A$. Rows of P become columns of D, so the coefficients of $x_1$ form the first dual constraint.
- Equality in P gives an **unrestricted** dual variable (not $\ge0$). An unrestricted primal variable gives an **equality** dual constraint.
- "$`\ge`$" in a **Max** primal gives $y_i\le0$; it is easier to multiply by $-1$ first.
- Weak duality gives a bracket $Z(x)\le Z^\ast \le W(y)$, which you can use to eliminate options.
- Both P and D can be infeasible.
- Complementary slackness is one-directional: $x_j^\ast =0$ does **not** imply a strictly slack dual constraint.
- Shadow prices are valid only within the RHS ranging interval.
