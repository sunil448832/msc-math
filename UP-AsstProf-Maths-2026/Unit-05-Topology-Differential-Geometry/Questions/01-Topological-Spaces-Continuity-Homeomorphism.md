# Unit 5 · Topic 01 — Topological Spaces, Continuity, Homeomorphism
> Syllabus coverage: Basic concepts of Topology, Continuity, Homeomorphism
> Cheatsheet: [../Cheatsheets/01-Topological-Spaces-Continuity-Homeomorphism.md](../Cheatsheets/01-Topological-Spaces-Continuity-Homeomorphism.md)

**Q1.** `[Numerical]` ★ The number of distinct topologies on a set with 3 elements is

(A) 29

(B) 27

(C) 33

(D) 64

**Q2.** `[Concept]` ★ Let $X$ be an infinite set with the cofinite topology. Then $X$ is

(A) Hausdorff

(B) discrete

(C) not $T_1$

(D) $T_1$ but not Hausdorff

**Q3.** `[Multi-Statement]` ★★ Let $\mathbb R_l$ denote $\mathbb{R}$ with the lower limit topology (basis $\lbrace [a,b): a\lt b\rbrace$). Consider:

I. Every set $`[a,b)`$ is both open and closed in $`\mathbb R_l`$.

II. The topology of $\mathbb R_l$ is strictly finer than the usual topology of $\mathbb{R}$.

III. $\mathbb R_l$ is second countable.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q4.** `[Numerical]` ★★ Let $\mathbb{R}$ carry the cocountable topology (open sets: $\emptyset$ and complements of countable sets). The interior and the closure of $\mathbb{Q}$ are, respectively,

(A) $\emptyset$ and $\mathbb{R}$

(B) $\emptyset$ and $\mathbb{Q}$

(C) $\mathbb{Q}$ and $\mathbb{R}$

(D) $\mathbb{Q}$ and $\mathbb{Q}$

**Q5.** `[Assertion-Reason]` ★★

**Assertion (A):** The open interval $`(0,1)`$ is homeomorphic to $`\mathbb{R}`$.

**Reason (R):** Boundedness is a topological property.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[NOT-true / Counterexample]` ★ Which of the following is NOT a topological property (i.e. not preserved by homeomorphisms)?

(A) Compactness

(B) Connectedness

(C) Completeness (of a metric)

(D) Hausdorffness

**Q7.** `[Match]` ★★ Match the topology on $`\mathbb{R}`$ (List-I) with the closure of the set $`(0,1)`$ in it (List-II).

| List-I (topology on $`\mathbb{R}`$) | List-II (closure of $`(0,1)`$) |
|---|---|
| A. Usual topology | 1. $(0,1]$ |
| B. Cofinite topology | 2. $\mathbb{R}$ |
| C. Lower limit topology (basis $`[a,b)`$) | 3. $`[0,1]`$ |
| D. Upper limit topology (basis $(a,b]$) | 4. $[0,1)$ |

(A) A-3, B-2, C-1, D-4

(B) A-2, B-3, C-4, D-1

(C) A-3, B-3, C-4, D-1

(D) A-3, B-2, C-4, D-1

**Q8.** `[Concept]` ★ Let $\tau_1,\tau_2$ be topologies on the same set $X$. The identity map $\mathrm{id}:(X,\tau_1)\to(X,\tau_2)$ is continuous if and only if

(A) $\tau_1\subseteq\tau_2$

(B) $\tau_1\cap\tau_2=\lbrace \emptyset,X\rbrace$

(C) $\tau_1=\tau_2$

(D) $\tau_2\subseteq\tau_1$

**Q9.** `[Application]` ★★★ Let $f:(\mathbb{R},\text{cofinite})\to(\mathbb{R},\text{usual})$ be a function. Then $f$ is continuous if and only if

(A) $f$ is constant

(B) $f$ is any function

(C) $f$ is a polynomial

(D) $f$ takes only finitely many values

**Q10.** `[Multi-Statement]` ★★ Which of the following collections is/are a **basis** for some topology on $\mathbb{R}$?

I. $\lbrace (a,b): a\lt b,\ a,b\in\mathbb{Q}\rbrace$

II. $\lbrace [a,b): a\lt b,\ a,b\in\mathbb{Q}\rbrace$

III. $\lbrace (a,\infty): a\in\mathbb{R}\rbrace \cup\lbrace (-\infty,b): b\in\mathbb{R}\rbrace$

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q11.** `[Application]` ★★★ The number of topologies on a 3-element set, counted **up to homeomorphism** (i.e. the number of pairwise non-homeomorphic 3-point topological spaces), is

(A) 9

(B) 7

(C) 12

(D) 29

**Q12.** `[NOT-true / Counterexample]` ★★ Which of the following statements is NOT true?

(A) A homeomorphism is a continuous, open bijection.

(B) If $f:X\to Y$ is a homeomorphism then $f(\overline{A})=\overline{f(A)}$ for every $A\subseteq X$.

(C) Every continuous bijection between topological spaces is a homeomorphism.

(D) A space homeomorphic to a Hausdorff space is Hausdorff.

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Numerical |
| 2 | D | Concept |
| 3 | B | Multi-Statement |
| 4 | B | Numerical |
| 5 | C | Assertion-Reason |
| 6 | C | NOT-true |
| 7 | D | Match |
| 8 | D | Concept |
| 9 | A | Application |
| 10 | B | Multi-Statement |
| 11 | A | Application |
| 12 | C | NOT-true |

## Solutions
**Q1 — (A).** Counts of topologies on $n$ points: $1,4,29,355,6942$ for $n=1,\dots,5$ (verified by brute force). 64 = $2^6$ is the number of families of non-trivial subsets, not of topologies.

**Q2 — (D).** Singletons are closed (finite), so $T_1$. Two non-empty open sets in an infinite cofinite space always intersect (their complements are finite), so it cannot be Hausdorff.

**Q3 — (B).** $`[a,b)`$ is a basic open set; its complement $(-\infty,a)\cup[b,\infty)$ is a union of basic sets, so it is also open. $(a,b)=\bigcup[a+1/n,b)$, so $\mathbb R_l$ is finer, and $[0,1)$ is not usual-open, so strictly finer. III is false: any basis must contain for each $x$ a set $B_x$ with $x=\min B_x$, giving uncountably many distinct sets.

**Q4 — (B).** $\mathbb{Q}$ is countable, hence closed, so $\overline{\mathbb{Q}}=\mathbb{Q}$. Every non-empty open set is co-countable, hence uncountable, so it cannot lie inside $\mathbb{Q}$: $\mathrm{int}\thinspace \mathbb{Q}=\emptyset$. The trap (A) is the answer for the usual topology.

**Q5 — (C).** $x\mapsto\tan(\pi(x-\tfrac12))$ is a homeomorphism $(0,1)\to\mathbb{R}$. This very example shows that boundedness is **not** topological, so R is false.

**Q6 — (C).** $`(0,1)`$ (not complete) is homeomorphic to $`\mathbb{R}`$ (complete). Completeness depends on the metric, not only on the topology.

**Q7 — (D).** Usual: $`[0,1]`$. Cofinite: the closed sets are finite sets and $`\mathbb{R}`$, and $`(0,1)`$ is infinite, so the closure is $`\mathbb{R}`$. Lower limit: $`[1,1+\varepsilon)`$ misses $`(0,1)`$, but every $`[0,\varepsilon)`$ meets it, so the closure is $`[0,1)`$. Upper limit: by symmetry $`(0,1]`$.

**Q8 — (D).** $\mathrm{id}^{-1}(U)=U$ must be $\tau_1$-open for every $U\in\tau_2$, i.e. $\tau_2\subseteq\tau_1$ (the domain is finer). A common slip is to reverse the inclusion.

**Q9 — (A).** If $f(p)\ne f(q)$, take disjoint usual-open $U\ni f(p)$, $V\ni f(q)$. Then $f^{-1}(U),f^{-1}(V)$ are disjoint non-empty cofinite-open sets, which is impossible in an infinite cofinite space. Constants are clearly continuous. Option (D) fails because, for example, the indicator function of $\lbrace 0\rbrace$ is not continuous: $f^{-1}(\lbrace 1\rbrace )=\lbrace 0\rbrace$ is not open.

**Q10 — (B).** I and II cover $\mathbb{R}$, and the intersection of two members is again a member or empty, so both are bases (II gives a topology different from $\mathbb R_l$, but it is still a basis). III is only a **subbasis**: $(0,\infty)\cap(-\infty,1)=(0,1)$ contains no ray around $\tfrac12$.

**Q11 — (A).** The 29 labelled topologies fall into 9 homeomorphism classes (verified by brute force). 29 is the labelled count.

**Q12 — (C).** $t\mapsto e^{it}$ from $[0,2\pi)$ onto $S^1$ is a continuous bijection whose inverse is discontinuous at $1$. Another example is $\mathrm{id}:(X,\text{discrete})\to(X,\text{indiscrete})$.
