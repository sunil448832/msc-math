# Unit 5 · Topic 03 — Connectedness and Compactness
> Syllabus coverage: connectedness, compactness (path-connectedness, components, local compactness, Heine–Borel)
> Cheatsheet: [../Cheatsheets/03-Connectedness-Compactness.md](../Cheatsheets/03-Connectedness-Compactness.md)

**Q1.** `[Concept]` ★ Which of the following subsets of $\mathbb R$ (usual topology) is connected?

(A) $\mathbb Q$

(B) $[0,1]\cup[2,3]$

(C) $\{x: x^2>1\}$

(D) $[0,\infty)$

**Q2.** `[Concept]` ★★ The topologist's sine curve $S=\{(x,\sin\tfrac1x):0<x\le1\}\cup(\{0\}\times[-1,1])$ is

(A) path-connected

(B) connected but not path-connected

(C) not connected

(D) locally connected

**Q3.** `[Numerical]` ★★ The number of connected components of $GL_2(\mathbb R)$ (as a subspace of $\mathbb R^4$) is

(A) 1

(B) 2

(C) 3

(D) 4

**Q4.** `[Multi-Statement]` ★★ Consider:

I. $\mathbb R$ with the cofinite topology is compact.

II. $[0,1]$, as a subspace of the lower limit line $\mathbb R_l$, is compact.

III. $\mathbb R$ with the cocountable topology is compact.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★

**Assertion (A):** Every closed and bounded subset of a metric space is compact.

**Reason (R):** A subset of $\mathbb R^n$ is compact if and only if it is closed and bounded.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ Match the space (List-I) with its property (List-II).

| List-I | List-II |
|---|---|
| A. $\mathbb Q$ (subspace of $\mathbb R$) | 1. Connected but not path-connected |
| B. Topologist's sine curve | 2. Connected, locally compact, not compact |
| C. $\mathbb R^n$ | 3. Totally disconnected, not locally compact |
| D. Cantor set | 4. Compact, totally disconnected, no isolated points |

(A) A-3, B-1, C-2, D-4

(B) A-4, B-1, C-2, D-3

(C) A-3, B-2, C-1, D-4

(D) A-1, B-3, C-2, D-4

**Q7.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) A compact subset of a Hausdorff space is closed.

(B) A closed subset of a compact space is compact.

(C) A compact subset of any topological space is closed.

(D) A continuous image of a compact space is compact.

**Q8.** `[Application]` ★★ The map $f:[0,2\pi)\to S^1$, $f(t)=e^{it}$, is a continuous bijection but not a homeomorphism. Which hypothesis of the theorem "a continuous bijection from a compact space onto a Hausdorff space is a homeomorphism" fails?

(A) $S^1$ is not Hausdorff

(B) $[0,2\pi)$ is not compact

(C) $S^1$ is not connected

(D) $f$ is not injective

**Q9.** `[Application]` ★★★ For which of the following spaces is the one-point (Alexandroff) compactification NOT Hausdorff?

(A) $\mathbb R$

(B) $\mathbb N$ (discrete)

(C) $\mathbb Q$

(D) $(0,1)$

**Q10.** `[Numerical]` ★ The number of connected components of $\{(x,y)\in\mathbb R^2: x^2+y^2\ne1,\ xy\ne0\}$ is

(A) 4

(B) 6

(C) 8

(D) 10

**Q11.** `[Multi-Statement]` ★★★ Consider:

I. $\mathbb Q$ is locally compact.

II. $\mathbb R^\omega$ with the product topology is locally compact.

III. Every compact Hausdorff space is locally compact.

Which of the above is/are correct?

(A) III only

(B) I and III only

(C) II and III only

(D) I, II and III

**Q12.** `[Concept]` ★ The connected components of a topological space are always

(A) open

(B) closed

(C) both open and closed

(D) path-connected

**Q13.** `[Application]` ★★ Which of the following pairs of spaces are homeomorphic?

(A) $[0,1]$ and $S^1$

(B) $\mathbb R$ and $\mathbb R^2$

(C) $[0,1)$ and $[0,1]$

(D) $S^1\setminus\{p\}$ and $(0,1)$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | B | Concept |
| 3 | B | Numerical |
| 4 | A | Multi-Statement |
| 5 | D | Assertion-Reason |
| 6 | A | Match |
| 7 | C | NOT-true |
| 8 | B | Application |
| 9 | C | Application |
| 10 | C | Numerical |
| 11 | A | Multi-Statement |
| 12 | B | Concept |
| 13 | D | Application |

## Solutions
**Q1 — (D).** The connected subsets of $\mathbb R$ are exactly the intervals. $[0,\infty)$ is an interval. $\mathbb Q$ is totally disconnected, and the sets in (B) and (C) are unions of two disjoint closed rays or intervals.

**Q2 — (B).** $S$ is the closure of the connected graph $\{(x,\sin1/x)\}$, so it is connected. No path can join $(0,0)$ to a point of the graph, because $\sin(1/x)$ oscillates without a limit as $x\to0^+$. It is not locally connected at points of the segment either.

**Q3 — (B).** $\det: GL_2(\mathbb R)\to\mathbb R\setminus\{0\}$ is continuous and onto, so there are at least 2 components. Each of $\{\det>0\}$ and $\{\det<0\}$ is path-connected. $GL_n(\mathbb C)$ is connected, which is the trap (A).

**Q4 — (A).** I: every open cover has a member $U$ missing only finitely many points, and finitely many more members cover those points. II: the cover $\{[1-\tfrac1n,1-\tfrac1{n+1})\}_{n\ge1}\cup\{[1,2)\}$ of $[0,1]$ consists of disjoint sets, so it has no finite subcover. III: take distinct $x_1,x_2,\dots$ and $U_n=\mathbb R\setminus\{x_k:k\ge n\}$. These are open and increasing with union $\mathbb R$, but no finite subfamily covers $\mathbb R$.

**Q5 — (D).** R is the Heine–Borel theorem. A is false: in $\mathbb R$ with the discrete metric $d\le1$, the whole space is closed and bounded but not compact. Likewise the closed unit ball of $\ell^2$ is not compact.

**Q6 — (A).** $\mathbb Q$: components are singletons, and no point has a compact neighbourhood. Topologist's sine curve: Q2. $\mathbb R^n$: Heine–Borel gives local compactness, but it is unbounded. Cantor set: compact, totally disconnected and perfect.

**Q7 — (C).** In an indiscrete space with at least two points, every subset is compact, but $\{x\}$ is not closed. (A) needs the Hausdorff hypothesis.

**Q8 — (B).** $S^1$ is a compact Hausdorff space and $f$ is bijective, so the domain must fail to be compact. Indeed $f$ maps the open set $[0,1)$ to a set that is not open in $S^1$.

**Q9 — (C).** The one-point compactification of $X$ is Hausdorff iff $X$ is locally compact Hausdorff. $\mathbb Q$ is not locally compact. The others give $S^1$, $\{0\}\cup\{1/n\}$ and $S^1$ respectively.

**Q10 — (C).** The two coordinate axes cut the plane into 4 open quadrants. The unit circle splits each quadrant into an inner piece and an outer piece, giving $4\times2=8$.

**Q11 — (A).** I: a compact neighbourhood of a point of $\mathbb Q$ would contain $[a,b]\cap\mathbb Q$ with closure $[a,b]$ in $\mathbb R$, which is not a subset of $\mathbb Q$. II: every basic neighbourhood contains entire factors $\mathbb R$, so its closure is not compact. III: take the whole space as the compact neighbourhood.

**Q12 — (B).** The closure of a connected set is connected, so each component is closed. Components need not be open: in $\mathbb Q$ the components $\{q\}$ are not open. Components need not be path-connected: see the topologist's sine curve.

**Q13 — (D).** $S^1\setminus\{p\}\cong\mathbb R\cong(0,1)$. The other pairs are distinguished by invariants. (A) Removing an interior point disconnects $[0,1]$, but removing any single point leaves $S^1$ connected. (B) $\mathbb R$ minus a point is disconnected, but $\mathbb R^2$ minus a point is not. (C) Compactness.
