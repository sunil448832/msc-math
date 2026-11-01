# Cheatsheet · Unit 9 · Topic 07 — Linear Systems: Gauss Elimination, LU, Jacobi, Gauss–Seidel
> Questions: [../Questions/07-Linear-Systems-Gauss-Elimination-Gauss-Seidel.md](../Questions/07-Linear-Systems-Gauss-Elimination-Gauss-Seidel.md)

## 1. Gauss elimination (direct method)
- Reduce $[A\mid b]$ to an upper triangular $[U\mid c]$ using multipliers $m_{ik}=a_{ik}^{(k)}/a_{kk}^{(k)}$, then **back-substitute**.
- **No-pivot condition:** elimination runs to completion iff the leading principal minors $\Delta_1,\dots,\Delta_{n-1}\ne0$. The pivots are $u_{kk}=\Delta_k/\Delta_{k-1}$.
- $\det A=\prod u_{kk}$ (times $(-1)^{\sharp \text{swaps}}$ when rows are interchanged).
- **Partial pivoting:** at step $k$, swap in the row with the largest $|a_{ik}^{(k)}|$ ($i\ge k$), so that $|m_{ik}|\le1$. This controls round-off growth. **Complete pivoting** searches both rows and columns.
- Pivoting is unnecessary for strictly diagonally dominant (by columns) and for SPD matrices.
- Classic round-off example: $\varepsilon x+y=1,\ x+y=2$ with tiny $\varepsilon$. Without pivoting it gives $x\approx0$, which is wrong.

### Operation counts (multiplications/divisions, leading term)
| Process | Count |
|---|---|
| Gauss elimination (forward) | $n^3/3$ |
| Back substitution | $n^2/2$ |
| Gauss–Jordan | $n^3/2$ |
| LU factorisation | $n^3/3$; each further RHS costs $n^2$ |
| Cholesky | $n^3/6$ |
| Inverse via elimination | $n^3$ |
| One Jacobi/GS sweep (dense) | $n^2$ |
| Cramer's rule (cofactor determinants) | $\sim(n+1)!$, useless |

## 2. LU factorisations
- **Doolittle:** $L$ unit lower triangular. **Crout:** $U$ unit upper triangular. **Cholesky:** $A=LL^T$, for **SPD** matrices only.
- **Existence and uniqueness:** if all leading principal minors $\Delta_1,\dots,\Delta_{n-1}\ne0$ (and $A$ is nonsingular), the Doolittle/Crout factorisation exists and is unique.
- In general only $PA=LU$ is guaranteed. Example: $`\begin{pmatrix}0&1\cr 1&0\end{pmatrix}`$ has no LU.
- To solve $Ax=b$: solve $Ly=b$ (forward), then $Ux=y$ (back).
- Tridiagonal systems use the **Thomas algorithm**, which costs $O(n)$.

## 3. Iterative methods
Split $A=D+L+U$ (diagonal, strictly lower, strictly upper).
| Method | Componentwise | Iteration matrix |
|---|---|---|
| Jacobi | $x_i^{(k+1)}=\dfrac{1}{a_{ii}}\Big(b_i-\sum_{j\ne i}a_{ij}x_j^{(k)}\Big)$ | $B_J=-D^{-1}(L+U)$ |
| Gauss–Seidel | uses the new $x_j^{(k+1)}$ for $j\lt i$ | $B_{GS}=-(D+L)^{-1}U$ |
| SOR ($\omega$) | $x^{new}=(1-\omega)x^{old}+\omega\thinspace x^{GS}$ | $(D+\omega L)^{-1}[(1-\omega)D-\omega U]$ |

### Convergence theorems
- **Fundamental:** $x^{(k+1)}=Bx^{(k)}+c$ converges for every $x^{(0)}$ **iff $\rho(B)\lt 1$**. A sufficient condition is $\Vert B\Vert \lt 1$ in some induced norm. The asymptotic rate is $-\log_{10}\rho(B)$ digits per step.
- **Strict diagonal dominance** (by rows: $|a_{ii}|\gt \sum_{j\ne i}|a_{ij}|$) implies that **both** Jacobi and GS converge. It is sufficient, not necessary.
- **SPD** implies that GS converges. SOR converges iff $0\lt \omega\lt 2$ (Ostrowski–Reich). Jacobi on an SPD matrix converges iff $2D-A$ is also PD.
- SOR can converge only for $0\lt \omega\lt 2$ (Kahan).
- For tridiagonal / consistently ordered matrices, $\rho(B_{GS})=\rho(B_J)^2$, so GS is twice as fast.
- **Jacobi and GS are not comparable in general.**
  - $`\begin{pmatrix}1&2&-2\cr 1&1&1\cr 2&2&1\end{pmatrix}`$: $\rho_J=0$ but $\rho_{GS}=2$, so Jacobi converges and GS diverges.
  - $`\frac12\begin{pmatrix}2&-1&1\cr 2&2&2\cr -1&-1&2\end{pmatrix}`$ (standard example): GS converges and Jacobi diverges ($\rho_J=\sqrt5/2$, $\rho_{GS}=1/2$).
- **Reorder** the equations so that the largest coefficients sit on the diagonal before iterating.

### Worked mini-example
For $10x+y+z=12$ (cyclic, solution $`(1,1,1)`$), starting from 0: Jacobi gives $(1.2,1.2,1.2)$ and GS gives $(1.2,1.08,0.972)$.

## 4. Direct vs iterative
| | Direct (Gauss, LU) | Iterative (Jacobi, GS) |
|---|---|---|
| Exact in finite steps (exact arithmetic) | yes | no |
| Round-off | accumulates | self-correcting |
| Best for | small or dense systems | large, sparse, diagonally dominant systems |
| Fill-in | yes | no (preserves sparsity) |

## Exam traps
- A "nonsingular" matrix need not have an LU factorisation without pivoting.
- Jacobi convergence does not imply GS convergence, and GS convergence does not imply Jacobi convergence.
- Diagonal dominance is **sufficient only**. Many non-dominant systems still converge.
- Gauss elimination costs $n^3/3$, Gauss–Jordan costs $n^3/2$. Don't swap them.
- Jacobi uses only old values. GS uses the updated values immediately, so the order of the equations matters for GS.
- A triangular $A$ gives a nilpotent $B_{GS}$ (upper triangular case), so GS converges in at most $n$ steps.
