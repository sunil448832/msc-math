# Cheatsheet · Unit 9 · Topic 05 — Game Theory (Two-Person Zero-Sum)
> Questions: [../Questions/05-Game-Theory.md](../Questions/05-Game-Theory.md)

## 1. Basics
- **Two-person zero-sum (rectangular) game:** the payoff matrix $A=(a_{ij})_{m\times n}$ gives player A's (row, maximiser) gain, which is B's (column, minimiser) loss.
- **Pure strategy:** a single row or column. **Mixed strategy:** a probability vector $p\in\Delta_m$ for A, $q\in\Delta_n$ for B.
- **Expected payoff:** $E(p,q) = p^TAq$.
- **Maximin (lower value):** $\underline v = \max_i\min_j a_{ij}$. **Minimax (upper value):** $\overline v = \min_j\max_i a_{ij}$. Always $\underline v\le\overline v$.
- **Saddle point** $(r,s)$: $a_{rs}$ is the minimum of its row **and** the maximum of its column. Equivalently $\underline v=\overline v = a_{rs}$. Then the optimal strategies are **pure** and $v = a_{rs}$.
  - Several saddle points may exist, and all have the same value.
- **Value $v$:** $\underline v\le v\le\overline v$. **Fair game:** $v=0$. **Strictly determined:** $\underline v=\overline v$.
- **Minimax theorem (von Neumann):** for every finite matrix game, $\max_p\min_q p^TAq = \min_q\max_p p^TAq = v$. So a value always exists in mixed strategies. Proof: LP duality or separating hyperplanes.

## 2. Properties
- Adding $k$ to every entry gives value $v+k$, with the same optimal strategies.
- Multiplying every entry by $c\gt 0$ gives value $cv$, with the same strategies.
- **Skew-symmetric** $A$ ($A^T=-A$), a symmetric game, has $v = 0$.
- $p^\ast$ is optimal for A iff $\sum_i p_i^\ast a_{ij}\ge v$ for all $j$. $q^\ast$ is optimal for B iff $\sum_j a_{ij}q_j^\ast \le v$ for all $i$.
- **Complementary slackness:** if $q_j^\ast \gt 0$ then $`\sum_ip^\ast _ia_{ij}=v`$; if $p_i^\ast \gt 0$ then $\sum_ja_{ij}q_j^\ast =v$.

## 3. $2\times2$ game without a saddle point
$`A=\begin{pmatrix}a_{11}&a_{12}\cr a_{21}&a_{22}\end{pmatrix}`$, with $D = a_{11}+a_{22}-a_{12}-a_{21}$.
$$p_1 = \frac{a_{22}-a_{21}}{D},\qquad q_1 = \frac{a_{22}-a_{12}}{D},\qquad v = \frac{a_{11}a_{22}-a_{12}a_{21}}{D}.$$
(Then $p_2=1-p_1$ and $q_2=1-q_1$.) **Check first that there is no saddle point**; otherwise the formula gives nonsense.
- **Oddments method:** A's odds for row 1 are $\lvert a_{21}-a_{22}\rvert$ and for row 2 are $\lvert a_{11}-a_{12}\rvert$ (cross-assigned).
- Examples: $`\begin{pmatrix}3&-1\cr -2&4\end{pmatrix}`$ gives $v=1$, $p=(0.6,0.4)$, $q=(0.5,0.5)$. $`\begin{pmatrix}5&1\cr 3&4\end{pmatrix}`$ gives $v=17/5$, $p=(1/5,4/5)$, $q=(3/5,2/5)$.

## 4. Dominance
- **Row $r$ dominates row $s$** (for A, the maximiser) if $a_{rj}\ge a_{sj}$ for all $j$. Delete the **smaller** row $s$.
- **Column $k$ dominates column $l$** (for B, the minimiser) if $a_{ik}\le a_{il}$ for all $i$. Delete the **larger** column $l$.
- A row or column can also be dominated by a **convex combination** (average) of other rows or columns.
- Deleting strictly dominated strategies never changes the value. Their optimal probability is $0$.
- Example: $`\begin{pmatrix}1&7&2\cr 6&2&7\cr 5&1&6\end{pmatrix}`$: delete R3 (dominated by R2), then C3 (dominated by C1), leaving $`\begin{pmatrix}1&7\cr 6&2\end{pmatrix}`$ with $v=4$.

## 5. Graphical method
- **$2\times n$:** A plays $(p, 1-p)$. Draw the lines $E_j(p) = a_{1j}p + a_{2j}(1-p)$ for $p\in[0,1]$. Take the **lower envelope** (B minimises), and its **highest point** gives $p^\ast$ and $v$. The two (or more) lines through that point give B's active columns. Then solve the $2\times2$ subgame.
- **$m\times2$:** B plays $(q,1-q)$. Draw $E_i(q)$. Take the **upper envelope** (A maximises), and its **lowest point** gives $q^\ast$ and $v$.
- Example: $`\begin{pmatrix}1&-3&7\cr 2&4&-6\end{pmatrix}`$: lines $2-p$, $4-7p$, $13p-6$; maximin of the envelope at $p=\tfrac12$, so $v=\tfrac12$ and $q=(0,\tfrac{13}{20},\tfrac{7}{20})$.

## 6. LP formulation (general $m\times n$)
Make all entries positive (add $k$ so that $v\gt 0$). Put $x_i=p_i/v$ and $y_j = q_j/v$.
$$\textbf{A:}\ \min\sum x_i\ \ \text{s.t.}\ \sum_i a_{ij}x_i\ge1\ \forall j,\ x\ge0;\qquad \textbf{B:}\ \max\sum y_j\ \ \text{s.t.}\ \sum_j a_{ij}y_j\le1\ \forall i,\ y\ge0.$$
- These two LPs are **duals** of each other; strong duality gives the minimax theorem.
- $v = 1/\sum x_i^\ast  = 1/\sum y_j^\ast$, $p_i = v\thinspace x_i^\ast$, $q_j = v\thinspace y_j^\ast$. At the end subtract the added $k$.

## 7. Solution procedure (summary)

| Situation | Method |
|---|---|
| Saddle point exists | pure strategies, $v=$ saddle entry |
| $2\times2$, no saddle point | formula / oddments |
| Reducible by dominance | reduce first |
| $2\times n$ or $m\times2$ | graphical |
| $3\times3$ and larger | LP (simplex), or the algebraic method / iterative (Brown–Robinson) approximation |

## Exam traps
- **Always test for a saddle point first.** Row minima give the maximin and column maxima give the minimax.
- Dominance directions are opposite for rows (delete the smaller) and columns (delete the **larger**), because B minimises.
- $\max\min\lt \min\max$ does **not** mean "no value"; it means no pure solution. A mixed value exists.
- In the $2\times2$ formula, $p_1$ uses $a_{22}-a_{21}$ (the **second row**), while $q_1$ uses $a_{22}-a_{12}$ (the **second column**). Do not swap them.
- For $2\times n$, take the **maximum of the lower** envelope; for $m\times2$, take the **minimum of the upper** envelope.
- In the LP method, ensure $v\gt 0$ (add a constant). The LP optimum is $1/v$, not $v$.
- A skew-symmetric matrix has value $0$. A merely symmetric ($A^T=A$) matrix need **not** have value $0$.
