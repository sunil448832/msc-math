# Unit 5 · Topic 02 — Subspace, Product and Quotient Spaces; Tychonoff's Theorem
> Syllabus coverage: subspaces, product spaces, quotient spaces, Tychonoff's theorem
> Cheatsheet: [../Cheatsheets/02-Subspace-Product-Quotient-Spaces.md](../Cheatsheets/02-Subspace-Product-Quotient-Spaces.md)

**Q1.** `[Concept]` ★ The space $[0,1]^{\mathbb{R}}$ (uncountably many copies of $[0,1]$) with the **product** topology is

(A) compact

(B) not compact, because the product is uncountable

(C) compact only when given the box topology

(D) compact and metrizable

**Q2.** `[Multi-Statement]` ★★ On $\mathbb R^\omega=\prod_{n\ge1}\mathbb{R}$ define $f(t)=(t,t,t,\dots)$. Consider:

I. The box topology on $\mathbb R^\omega$ is strictly finer than the product topology.

II. $f:\mathbb{R}\to\mathbb R^\omega$ is continuous when $\mathbb R^\omega$ has the product topology.

III. $f:\mathbb{R}\to\mathbb R^\omega$ is continuous when $\mathbb R^\omega$ has the box topology.

Which of the above is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and II only

**Q3.** `[Assertion-Reason]` ★★

**Assertion (A):** The Hilbert cube $[0,1]^{\mathbb{N}}$ with the product topology is compact.

**Reason (R):** Any product of compact spaces is compact in the box topology.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q4.** `[Numerical]` ★ Let $X=\lbrace a,b,c\rbrace$ with topology $\tau=\lbrace \emptyset,\lbrace a\rbrace ,\lbrace a,b\rbrace ,X\rbrace$, and let $Y=\lbrace a,c\rbrace$. The number of open sets in the subspace topology on $Y$ is

(A) 2

(B) 3

(C) 4

(D) 5

**Q5.** `[Match]` ★★ Let $I^2=[0,1]\times[0,1]$ (or $I=[0,1]$ in A). Match the identification (List-I) with the quotient space (List-II).

| List-I | List-II |
|---|---|
| A. $I$ with $0\sim1$ | 1. Torus |
| B. $I^2$ with $(0,y)\sim(1,y)$ and $(x,0)\sim(x,1)$ | 2. Circle $S^1$ |
| C. $I^2$ with $(0,y)\sim(1,y)$ and $(x,0)\sim(1-x,1)$ | 3. Real projective plane $\mathbb{RP}^2$ |
| D. $I^2$ with $(0,y)\sim(1,1-y)$ and $(x,0)\sim(1-x,1)$ | 4. Klein bottle |

(A) A-2, B-1, C-3, D-4

(B) A-2, B-4, C-1, D-3

(C) A-2, B-1, C-4, D-3

(D) A-1, B-2, C-4, D-3

**Q6.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true in general?

(A) A product of Hausdorff spaces is Hausdorff.

(B) A product of connected spaces is connected (product topology).

(C) A quotient of a Hausdorff space is Hausdorff.

(D) A subspace of a Hausdorff space is Hausdorff.

**Q7.** `[Concept]` ★ The product topology on $\prod_\alpha X_\alpha$ is

(A) the finest topology making all projections $\pi_\alpha$ continuous

(B) the same as the box topology for every index set

(C) the coarsest topology making all projections $\pi_\alpha$ closed maps

(D) the coarsest topology making all projections $\pi_\alpha$ continuous

**Q8.** `[Application]` ★★★ On $\mathbb{R}$ define $x\sim y\iff x-y\in\mathbb{Q}$. The quotient space $\mathbb{R}/\negthinspace \sim$ with the quotient topology is

(A) discrete

(B) indiscrete

(C) homeomorphic to $S^1$

(D) Hausdorff but not compact

**Q9.** `[Application]` ★★ In the Sorgenfrey plane $\mathbb R_l\times\mathbb R_l$, the subspace topology on the anti-diagonal $L=\lbrace (x,-x):x\in\mathbb{R}\rbrace$ is

(A) discrete

(B) indiscrete

(C) the usual topology of a line

(D) the lower limit topology

**Q10.** `[Multi-Statement]` ★★★ Let $X,Y$ be topological spaces and $\lbrace X_\alpha\rbrace$ a family of spaces. Consider:

I. The projection $p_1:X\times Y\to X$ is always an open map.

II. The projection $p_1:X\times Y\to X$ is always a closed map.

III. A map $f:Z\to\prod_\alpha X_\alpha$ (product topology) is continuous iff every $\pi_\alpha\circ f$ is continuous.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q11.** `[Numerical]` ★ In the subspace $Y=(0,1]$ of $\mathbb{R}$, the closure of $A=(0,\tfrac12)$ is

(A) $[0,\tfrac12]$

(B) $(0,\tfrac12]$

(C) $(0,\tfrac12)$

(D) $[0,\tfrac12)$

**Q12.** `[NOT-true / Counterexample]` ★★ For $\mathbb R^\omega$ with the **box** topology, which statement is NOT true?

(A) It is finer than the product topology.

(B) It is Hausdorff.

(C) For a finite product $\mathbb R^n$ the box and product topologies coincide.

(D) $\mathbb R^\omega$ with the box topology is connected.

**Q13.** `[Concept]` ★★ Over ZF set theory, Tychonoff's theorem for **arbitrary** (not necessarily Hausdorff) compact spaces is equivalent to

(A) the Axiom of Choice

(B) the Continuum Hypothesis

(C) the Baire Category Theorem

(D) the Axiom of Countable Choice

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | D | Multi-Statement |
| 3 | C | Assertion-Reason |
| 4 | B | Numerical |
| 5 | C | Match |
| 6 | C | NOT-true |
| 7 | D | Concept |
| 8 | B | Application |
| 9 | A | Application |
| 10 | C | Multi-Statement |
| 11 | B | Numerical |
| 12 | D | NOT-true |
| 13 | A | Concept |

## Solutions
**Q1 — (A).** By Tychonoff's theorem, any product of compact spaces is compact in the product topology, whatever the size of the index set. It is **not** metrizable, because an uncountable product of non-trivial spaces is not first countable, so (D) is wrong.

**Q2 — (D).** Box open sets include all product open sets, and $\prod(-1/n,1/n)$ is box-open but not product-open, so I holds. II holds because each coordinate $t\mapsto t$ is continuous. III fails: $f^{-1}\big(\prod(-1/n,1/n)\big)=\lbrace 0\rbrace$, which is not open.

**Q3 — (C).** A is Tychonoff's theorem. R is false: $\lbrace 0,1\rbrace ^{\mathbb N}$ with the box topology is discrete and infinite, so not compact. Compactness passes to products only in the **product** topology.

**Q4 — (B).** $\lbrace U\cap Y\rbrace =\lbrace \emptyset,\lbrace a\rbrace ,\lbrace a\rbrace ,Y\rbrace =\lbrace \emptyset,\lbrace a\rbrace ,Y\rbrace$, which gives 3 open sets.

**Q5 — (C).** The square with both pairs of sides identified in the same direction gives the torus ($aba^{-1}b^{-1}$). Reversing one pair gives the Klein bottle ($abab^{-1}$). Reversing both pairs gives $\mathbb{RP}^2$ ($abab$, antipodal boundary identification). Gluing the ends of an interval gives $S^1$.

**Q6 — (C).** The quotient of $\mathbb R$ obtained by collapsing $\mathbb{Q}$ to a point, or $\mathbb R/\negthinspace \sim$ in Q8, is not Hausdorff. Statements (A), (B) and (D) are standard theorems.

**Q7 — (D).** The product topology is generated by the subbasis $\pi_\alpha^{-1}(U_\alpha)$, which makes it the smallest topology for which every projection is continuous. It equals the box topology only for **finite** products.

**Q8 — (B).** Let $V$ be open and non-empty in the quotient. Then $\pi^{-1}(V)$ is open, non-empty and invariant under translations by $\mathbb Q$. It contains some interval $(a,b)$, and $(a,b)+\mathbb Q=\mathbb R$, so $\pi^{-1}(V)=\mathbb R$. The only open sets are therefore $\emptyset$ and the whole space.

**Q9 — (A).** $\big([a,a+1)\times[-a,-a+1)\big)\cap L=\lbrace (a,-a)\rbrace$, so every point is open. This uncountable closed discrete subspace is why the Sorgenfrey plane is not Lindelöf (and not normal).

**Q10 — (C).** The projection of a basic open set $U\times V$ is $U$, so projections are open. They need not be closed: $\lbrace xy=1\rbrace$ is closed in $\mathbb R^2$ but projects onto $\mathbb R\setminus\lbrace 0\rbrace$. III is the universal property of the product topology. It **fails** for the box topology, as Q2 shows.

**Q11 — (B).** $`\mathrm{cl}_Y(A)=\mathrm{cl}_{\mathbb R}(A)\cap Y=[0,\tfrac12]\cap(0,1]=(0,\tfrac12]`$. Option (A) would include $0\notin Y$.

**Q12 — (D).** In the box topology, $`U=\lbrace`$bounded sequences$`\rbrace`$ and $`V=\lbrace`$unbounded sequences$`\rbrace`$ are disjoint, non-empty, open (each point has a box neighbourhood $\prod(x_n-1,x_n+1)$ staying in the same class) and cover $\mathbb R^\omega$. So it is disconnected. The product topology on $\mathbb R^\omega$ is connected.

**Q13 — (A).** Kelley (1950) proved that Tychonoff's theorem implies AC. The version for compact **Hausdorff** spaces is weaker: it is equivalent to the Boolean prime ideal (ultrafilter) theorem. Countable choice is strictly weaker than AC.
