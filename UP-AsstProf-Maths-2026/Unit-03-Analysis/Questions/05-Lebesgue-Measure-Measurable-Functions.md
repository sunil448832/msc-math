# Unit 3 · Topic 05 — Lebesgue Measure and Lebesgue Measurable Functions
> Syllabus coverage: Lebesgue measure (outer measure, measurable sets, null sets, Cantor set, non-measurable sets, Borel vs Lebesgue sets), Lebesgue measurable functions (operations, almost everywhere, Egorov's and Lusin's theorems)
> Cheatsheet: [../Cheatsheets/05-Lebesgue-Measure-Measurable-Functions.md](../Cheatsheets/05-Lebesgue-Measure-Measurable-Functions.md)

**Q1.** `[Concept]` ★ The Lebesgue outer measure of $\mathbb{Q}\cap[0,1]$ is

(A) $0$

(B) $1$

(C) $1/2$

(D) not defined, since the set is dense in $[0,1]$

**Q2.** `[Numerical]` ★★★ A "fat Cantor set" $F\subset[0,1]$ is built as follows. At stage $n=1,2,3,\dots$, remove an open interval of length $1/4^n$ from the middle of each of the $2^{n-1}$ closed intervals that remain. Then $m(F)=$

(A) $0$

(B) $1/4$

(C) $1/2$

(D) $2/3$

**Q3.** `[Multi-Statement]` ★★ Let $C$ be the Cantor ternary set.

I. $C$ is uncountable.

II. $m(C)=0$.

III. $C$ has at least one isolated point.

Which of the above is/are correct?

(A) I only

(B) II and III only

(C) I and II only

(D) I, II and III

**Q4.** `[Assertion-Reason]` ★★
**Assertion (A):** Every subset of $\mathbb{R}$ with Lebesgue measure zero is countable.
**Reason (R):** The Cantor set has Lebesgue measure zero.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q5.** `[Match]` ★★ Match each set (List-I) with its Lebesgue measure (List-II).

| List-I | List-II |
|---|---|
| a. the Cantor ternary set | 1. $1$ |
| b. $[0,1]\setminus\mathbb{Q}$ | 2. $\infty$ |
| c. $\bigcup_{n\ge1}\left[n,\thinspace n+\tfrac1n\right]$ | 3. $0$ |
| d. $\lbrace x\in[0,2\pi]:\sin x\gt \tfrac12\rbrace$ | 4. $\dfrac{2\pi}{3}$ |

(A) a-3, b-1, c-2, d-4

(B) a-3, b-1, c-4, d-2

(C) a-1, b-3, c-2, d-4

(D) a-3, b-2, c-1, d-4

**Q6.** `[NOT-true / Counterexample]` ★★ Which of the following is **NOT** true?

(A) Every Borel subset of $\mathbb{R}$ is Lebesgue measurable.

(B) Every Lebesgue measurable subset of $\mathbb{R}$ is a Borel set.

(C) Every subset of a set of Lebesgue measure zero is Lebesgue measurable.

(D) Lebesgue outer measure is translation invariant.

**Q7.** `[Concept]` ★ The classical (Vitali) construction of a non-Lebesgue-measurable subset of $[0,1]$ uses

(A) the Cantor function and the Baire category theorem

(B) the equivalence relation $x\sim y\iff x-y\in\mathbb{Q}$, together with the axiom of choice

(C) the equivalence relation $x\sim y\iff x-y\in\mathbb{Z}$, and countable additivity alone

(D) the Heine–Borel theorem

**Q8.** `[Application]` ★★★ Let $\phi$ be the Cantor function on $[0,1]$ and $\psi(x)=x+\phi(x)$, so that $\psi$ is a homeomorphism of $[0,1]$ onto $[0,2]$. If $C$ is the Cantor set, then $m(\psi(C))=$

(A) $0$

(B) $1/2$

(C) $1$

(D) $2$

**Q9.** `[Application]` ★★ The sequence $f_n=\chi_{[n,\infty)}$ on $\mathbb{R}$ converges to $0$ everywhere, but there is no measurable set $F$ with $m(\mathbb{R}\setminus F)\lt 1$ on which $f_n\to0$ uniformly. Which hypothesis of **Egorov's theorem** does this example show cannot be dropped?

(A) measurability of each $f_n$

(B) finiteness of the measure of the domain

(C) continuity of the limit function

(D) monotonicity of the sequence $(f_n)$

**Q10.** `[Concept]` ★ Lusin's theorem states that if $f:[a,b]\to\mathbb{R}$ is Lebesgue measurable, then for every $\varepsilon\gt 0$

(A) $f$ is continuous except on a set of measure less than $\varepsilon$

(B) there is a closed set $F$ with $m([a,b]\setminus F)\lt \varepsilon$ such that $f|_F$ is continuous

(C) there is a step function $g$ with $f=g$ outside a set of measure $0$

(D) $f$ is bounded except on a finite set

**Q11.** `[Multi-Statement]` ★★ Let $f,g:\mathbb{R}\to\mathbb{R}$.

I. If $f$ is Lebesgue measurable, then $|f|$ is Lebesgue measurable.

II. If $|f|$ is Lebesgue measurable, then $f$ is Lebesgue measurable.

III. If $f$ is Lebesgue measurable and $g=f$ almost everywhere, then $g$ is Lebesgue measurable.

Which of the above is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and III only

**Q12.** `[NOT-true / Counterexample]` ★★★ Which of the following is **NOT** true in general?

(A) If $(f_n)$ are measurable, then $\sup_nf_n$ and $\limsup_nf_n$ are measurable.

(B) Every monotone function $f:\mathbb{R}\to\mathbb{R}$ is Borel measurable.

(C) If $f$ is Lebesgue measurable and $g:\mathbb{R}\to\mathbb{R}$ is continuous, then $g\circ f$ is Lebesgue measurable.

(D) If $f$ is Lebesgue measurable and $g:\mathbb{R}\to\mathbb{R}$ is continuous, then $f\circ g$ is Lebesgue measurable.

**Q13.** `[Numerical]` ★★ Let $E$ be the set of $x\in[0,1]$ whose decimal expansion does not use the digit $7$. Then $m(E)=$

(A) $0$

(B) $9/10$

(C) $1/10$

(D) $1/2$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | C | Numerical |
| 3 | C | Multi-Statement |
| 4 | D | Assertion-Reason |
| 5 | A | Match |
| 6 | B | NOT-true / Counterexample |
| 7 | B | Concept |
| 8 | C | Application |
| 9 | B | Application |
| 10 | B | Concept |
| 11 | D | Multi-Statement |
| 12 | D | NOT-true / Counterexample |
| 13 | A | Numerical |

## Solutions
**Q1 — (A).** The set is countable: $\lbrace r_k\rbrace$. Cover $r_k$ by an interval of length $\varepsilon/2^k$; the total length is $\le\varepsilon$. Density is irrelevant to measure, which is why (B) is the trap.

**Q2 — (C).** The total removed length is $\sum_{n\ge1}2^{n-1}\cdot4^{-n}=\frac14\sum_{n\ge0}2^{-n}=\frac12$, so $m(F)=1-\frac12=\frac12$. $F$ is closed, nowhere dense and perfect, yet has positive measure. (A) is the ordinary Cantor set.

**Q3 — (C).** $C$ is in bijection with ternary expansions using only the digits $0$ and $2$, hence with $\lbrace 0,1\rbrace ^{\mathbb N}$, so it is uncountable. Its complement has length $\sum\frac{2^{n-1}}{3^n}=1$, so $m(C)=0$. $C$ is **perfect** (closed, no isolated points), so III is false.

**Q4 — (D).** The Cantor set is a counterexample to A: it is uncountable with measure zero. So A is false and R is true. (Countable ⇒ null holds, but the converse fails.)

**Q5 — (A).** a: $0$. b: $1-m(\mathbb{Q}\cap[0,1])=1$. c: the intervals are disjoint for $n\ge2$ (and $[1,2]$ meets $[2,2.5]$ only at a point), so the measure is $\sum\frac1n=\infty$. d: $(\pi/6,5\pi/6)$ has length $2\pi/3$.

**Q6 — (B).** There are $\mathfrak c$ Borel sets. But every subset of the Cantor set is Lebesgue measurable (it is null), which gives $2^{\mathfrak c}$ Lebesgue measurable sets. So some Lebesgue measurable sets are not Borel. (C) is completeness of Lebesgue measure. (A) and (D) are standard.

**Q7 — (B).** Choose one point from each coset of $\mathbb{Q}$ in $[0,1]$ (axiom of choice) to form $V$. The translates $V+r$, $r\in\mathbb{Q}\cap[-1,1]$, are disjoint, and their union lies between $[0,1]$ and $[-1,2]$. Countable additivity and translation invariance then force $1\le\sum m(V)\le3$, which is impossible. Using $\mathbb{Z}$ in place of $\mathbb{Q}$ gives just $[0,1)$.

**Q8 — (C).** On each removed open interval $\phi$ is constant, so $\psi$ there is a translation and preserves length. Hence $m(\psi([0,1]\setminus C))=m([0,1]\setminus C)=1$. Since $\psi$ is a bijection onto $[0,2]$, $m(\psi(C))=2-1=1$. So a homeomorphism can map a null set onto a set of positive measure. (This also shows that a subset of $\psi(C)$ which is non-measurable pulls back to a measurable null set.)

**Q9 — (B).** Each $f_n$ is measurable and the convergence is monotone, but $\sup|f_n-0|=1$ on every set that contains points of $[n,\infty)$ for all $n$. Egorov needs $m(E)\lt \infty$. Egorov never requires (C) or (D).

**Q10 — (B).** This is Lusin's theorem: the **restriction** to a large closed set is continuous, and in fact there is a continuous $g$ on $\mathbb{R}$ with $m\lbrace f\ne g\rbrace \lt \varepsilon$. (A) is false: $\chi_{\mathbb Q}$ is measurable but discontinuous everywhere. Its restriction to the irrationals is continuous, though.

**Q11 — (D).** $|f|=\phi\circ f$ with $\phi$ continuous, so I holds. III holds because Lebesgue measure is complete. II fails: if $V$ is non-measurable, $f=\chi_V-\chi_{V^c}$ has $|f|\equiv1$ but $\lbrace f\gt 0\rbrace =V$.

**Q12 — (D).** $g\circ f$ is fine, because preimages of open sets under $g$ are open. But $f\circ g$ can fail. With $\psi$ from Q8, take a non-measurable $N\subset\psi(C)$. Then $A=\psi^{-1}(N)\subset C$ is null, hence measurable, and $\chi_A\circ\psi^{-1}=\chi_N$ is not measurable even though $\psi^{-1}$ is continuous. (A) and (B) are standard ($\lbrace f\gt a\rbrace$ is an interval for monotone $f$).

**Q13 — (A).** The set of $x$ whose first $n$ digits avoid $7$ has measure $(9/10)^n$, which tends to $0$. Being "most" digits does not help: almost every number uses every digit (Borel's normal numbers). (B) only accounts for the first digit.
