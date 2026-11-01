# Unit 9 · Topic 05 — Game Theory (Two-Person Zero-Sum Games)
> Syllabus coverage: Game theory
> Cheatsheet: [../Cheatsheets/05-Game-Theory.md](../Cheatsheets/05-Game-Theory.md)

*Convention: the payoff matrix gives the gains of the row player $A$ (the maximiser). The column player $B$ is the minimiser.*

**Q1.** `[Concept]` ★ A two-person zero-sum game has a saddle point (in pure strategies) if and only if

(A) maximin value $=$ minimax value

(B) maximin value $<$ minimax value

(C) the payoff matrix is square

(D) the value of the game is zero

**Q2.** `[Numerical]` ★ The value of the game with payoff matrix
$$\begin{pmatrix} -5 & 3 & 1 & 20\\ 5 & 5 & 4 & 6\\ -4 & -2 & 0 & -5\end{pmatrix}$$
is

(A) 5

(B) 4

(C) 0

(D) $-2$

**Q3.** `[Numerical]` ★★ The value of the game with payoff matrix $\begin{pmatrix} 3 & -1\\ -2 & 4\end{pmatrix}$ is

(A) $-1$

(B) $3$

(C) $1$

(D) $\tfrac{1}{2}$

**Q4.** `[Application]` ★★★ For the game with payoff matrix
$$\begin{pmatrix} \lambda & 6 & 2\\ -1 & \lambda & -7\\ -2 & 4 & \lambda\end{pmatrix},$$
the entry $(1,1)$ is a saddle point if and only if

(A) $\lambda \ge 2$

(B) $-2\le\lambda\le 6$

(C) $-1 \le \lambda \le 2$

(D) $\lambda\le -1$

**Q5.** `[Multi-Statement]` ★★ For a finite two-person zero-sum game:

I. The value of the game is unique, even if the optimal strategies are not.

II. If a constant $k$ is added to every entry of the payoff matrix, the value increases by $k$ and the optimal strategies do not change.

III. If the game has a saddle point, then the optimal strategies are necessarily mixed (not pure).

Which is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q6.** `[Assertion-Reason]` ★★
**Assertion (A):** Every finite two-person zero-sum game has a value when mixed strategies are allowed.
**Reason (R):** For any payoff matrix, $\max_i\min_j a_{ij} \le \min_j\max_i a_{ij}$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ Match the type of game in List-I with the most appropriate method of solution in List-II.

| List-I | List-II |
|---|---|
| A. Game with a saddle point | 1. Linear programming (simplex) |
| B. $2\times2$ game without a saddle point | 2. Graphical method |
| C. $2\times n$ or $m\times 2$ game without a saddle point | 3. Pure strategies via maximin–minimax |
| D. General $m\times n$ game, no saddle point, no dominance | 4. Algebraic formula $p = \dfrac{a_{22}-a_{21}}{a_{11}+a_{22}-a_{12}-a_{21}}$ |

(A) A-3, B-4, C-1, D-2

(B) A-4, B-3, C-2, D-1

(C) A-3, B-2, C-4, D-1

(D) A-3, B-4, C-2, D-1

**Q8.** `[Application]` ★★★ Using dominance, the value of the game with payoff matrix
$$\begin{pmatrix} 1 & 7 & 2\\ 6 & 2 & 7\\ 5 & 1 & 6\end{pmatrix}$$
is

(A) 2

(B) 5

(C) 4

(D) $\tfrac{9}{2}$

**Q9.** `[Numerical]` ★★★ Using the graphical method, the value of the $2\times3$ game
$$\begin{pmatrix} 1 & -3 & 7\\ 2 & 4 & -6\end{pmatrix}$$
is

(A) $\tfrac{1}{2}$

(B) $1$

(C) $-3$

(D) $\tfrac{3}{2}$

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) A strictly dominated pure strategy is played with probability zero in every optimal strategy.

(B) If $\max\min < \min\max$ for a payoff matrix, the game has no value.

(C) In a $2\times2$ game with no saddle point, each player uses both pure strategies with positive probability.

(D) The value $v$ of the game always satisfies $\max_i\min_j a_{ij}\le v\le\min_j\max_i a_{ij}$.

**Q11.** `[Concept]` ★ If the payoff matrix of a two-person zero-sum game is skew-symmetric ($A^T = -A$), then the value of the game is

(A) 0

(B) 1

(C) the largest entry of $A$

(D) undefined

**Q12.** `[Application]` ★★ To solve a game with a positive payoff matrix by LP, player $A$'s problem is written as: minimise $x_1 + x_2 + \dots + x_m$ subject to $\sum_i a_{ij}x_i\ge 1$ for all $j$, $x_i\ge0$, where $x_i = p_i/v$. If the optimal value of this LP is $\tfrac14$, then the value of the game is

(A) $\tfrac14$

(B) $2$

(C) $\tfrac12$

(D) $4$

**Q13.** `[Numerical]` ★★ In the game with payoff matrix $\begin{pmatrix} 5 & 1\\ 3 & 4\end{pmatrix}$, the optimal mixed strategy of the column player $B$ is

(A) $\left(\tfrac15, \tfrac45\right)$

(B) $\left(\tfrac45, \tfrac15\right)$

(C) $\left(\tfrac25, \tfrac35\right)$

(D) $\left(\tfrac35, \tfrac25\right)$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | B | Numerical |
| 3 | C | Numerical |
| 4 | C | Application |
| 5 | B | Multi-Statement |
| 6 | B | Assertion-Reason |
| 7 | D | Match |
| 8 | C | Application |
| 9 | A | Numerical |
| 10 | B | NOT-true / Counterexample |
| 11 | A | Concept |
| 12 | D | Application |
| 13 | D | Numerical |

## Solutions
**Q1 — (A).** There is a saddle point exactly when the largest row-minimum equals the smallest column-maximum. In general maximin $\le$ minimax, and strict inequality means no saddle point. (D) describes a fair game.

**Q2 — (B).** The row minima are $-5, 4, -5$, so the maximin is $4$. The column maxima are $5,5,4,20$, so the minimax is $4$. The saddle point is $(2,3)$ and $v=4$. (A) is the largest entry of row 2, not its minimum.

**Q3 — (C).** Maximin $=-1$ and minimax $=3$, so there is no saddle point. Then $v = \dfrac{a_{11}a_{22}-a_{12}a_{21}}{a_{11}+a_{22}-a_{12}-a_{21}} = \dfrac{12-2}{3+4+1+2}=1$, with $p = (0.6, 0.4)$. (A) and (B) are the maximin and minimax, which only bound $v$.

**Q4 — (C).** $(1,1)$ is a saddle point iff $\lambda$ is the minimum of row 1 and the maximum of column 1. That means $\lambda\le\min(6,2) = 2$ and $\lambda\ge\max(-1,-2) = -1$. So $-1\le\lambda\le2$.

**Q5 — (B).** I: the value is unique (minimax theorem), although several optimal strategies can exist. II: $E(p,q)$ shifts by exactly $k$ for every $(p,q)$. III is false: a saddle point means **pure** optimal strategies.

**Q6 — (B).** A is von Neumann's minimax theorem. R is the elementary inequality, which holds for every matrix but gives only $\le$. Equality in mixed strategies needs a separating-hyperplane or LP-duality argument, so R does not explain A.

**Q7 — (D).** A saddle point gives pure strategies (3). A $2\times2$ game uses the formula (4). A $2\times n$ or $m\times2$ game uses the graphical method (2). A general game uses LP (1).

**Q8 — (C).** Row 3 $(5,1,6)$ is dominated by row 2 $(6,2,7)$, so delete it. For the minimiser $B$, column 3 $(2,7)$ is dominated by column 1 $(1,6)$ (B prefers smaller payoffs), so delete it. The remaining game is $\begin{pmatrix}1&7\\6&2\end{pmatrix}$ with no saddle point, so $v = \dfrac{2-42}{1+2-7-6} = 4$, with $p=(0.4,0.6,0)$. (D) $=\tfrac92$ comes from wrongly deleting column 1 instead, which leaves $\begin{pmatrix}7&2\\2&7\end{pmatrix}$ with value $45/10$.

**Q9 — (A).** The maximin is $-3$ and the minimax is $2$, so there is no saddle point. If $A$ plays row 1 with probability $p$, the expected payoffs against the columns are $2-p$, $4-7p$ and $13p-6$. The highest point of the lower envelope is where $4-7p = 13p-6$, i.e. $p=\tfrac12$, giving $v = \tfrac12$ (the line $2-p = 1.5$ lies above it there). B mixes columns 2 and 3 in the ratio $13:7$. (C) is just the maximin.

**Q10 — (B).** If maximin < minimax, there is no saddle point, but the game still has a value in **mixed** strategies (minimax theorem). (A), (C) and (D) are standard.

**Q11 — (A).** A skew-symmetric game is a symmetric game: both players face the same situation, so $v = -v$, which gives $v=0$ (a fair game).

**Q12 — (D).** $\sum x_i = \sum p_i/v = 1/v$. Minimising $\sum x_i$ maximises $v$, so $1/v = 1/4$ and $v = 4$.

**Q13 — (D).** There is no saddle point (maximin $3$, minimax $4$). The denominator is $5+4-1-3 = 5$. Then $q_1 = \dfrac{a_{22}-a_{12}}{5} = \dfrac{4-1}{5} = \dfrac35$, so $q=(\tfrac35, \tfrac25)$. Check: against row 1, $5\cdot\tfrac35 + 1\cdot\tfrac25 = \tfrac{17}{5}$; against row 2, $3\cdot\tfrac35+4\cdot\tfrac25 = \tfrac{17}{5}$ ✓. (A) is player $A$'s strategy $p = (\tfrac15,\tfrac45)$.
