# Unit 3 · Topic 08 — Metric Spaces
> Syllabus coverage: Elements of metric spaces — convergence, continuity, uniform continuity, compactness, connectedness and completeness (also: Cantor intersection theorem, Baire category theorem, contraction mapping principle)
> Cheatsheet: [../Cheatsheets/08-Metric-Spaces.md](../Cheatsheets/08-Metric-Spaces.md)

**Q1.** `[Concept]` ★ Which of the following metric spaces is complete?

(A) $(0,1)$ with $d(x,y)=|x-y|$

(B) $\mathbb Q$ with $d(x,y)=|x-y|$

(C) $\mathbb R$ with $d(x,y)=|\tan^{-1}x-\tan^{-1}y|$

(D) $\mathbb R$ with $d(x,y)=|x-y|$

**Q2.** `[Concept]` ★ A metric space is compact if and only if it is

(A) closed and bounded

(B) complete and bounded

(C) complete and totally bounded

(D) separable and complete

**Q3.** `[Multi-Statement]` ★★ Let $f:X\to Y$ be continuous and onto, where $X,Y$ are metric spaces. Consider the following statements.

I. If $X$ is compact, then $Y$ is compact.

II. If $X$ is complete, then $Y$ is complete.

III. If $X$ is connected, then $Y$ is connected.

Which is/are necessarily correct?

(A) I only

(B) I and III only

(C) II and III only

(D) I, II and III

**Q4.** `[Assertion-Reason]` ★★
**Assertion (A):** $f(x)=x^2$ is not uniformly continuous on $\mathbb R$.
**Reason (R):** Every continuous function on a compact metric space is uniformly continuous.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q5.** `[Match]` ★★ Match each space (usual metric unless stated) with the property that it has and that **no other space in List-I** has.

| List-I | List-II |
|---|---|
| (a) $\mathbb Q$ | 1. compact |
| (b) $[0,1]$ | 2. complete and connected, but not compact |
| (c) $\mathbb R$ | 3. not complete |
| (d) $\mathbb R$ with the discrete metric | 4. complete, but not separable |

(A) a-3, b-1, c-4, d-2

(B) a-3, b-2, c-1, d-4

(C) a-3, b-1, c-2, d-4

(D) a-4, b-1, c-2, d-3

**Q6.** `[NOT-true / Counterexample]` ★★ Which of the following is **NOT** true?

(A) A closed and bounded subset of a metric space need not be compact.

(B) The closed unit ball of $\ell^2$ is not compact.

(C) Every Cauchy sequence in a metric space is bounded.

(D) Every bounded sequence in a complete metric space has a convergent subsequence.

**Q7.** `[Numerical]` ★★ The map $T(x)=\dfrac{x}{2}+\dfrac{1}{x}$ is a contraction of $[1,\infty)$ into itself. Its unique fixed point is

(A) $1$

(B) $\sqrt2$

(C) $2$

(D) $\tfrac32$

**Q8.** `[Numerical]` ★★ The number of connected components of $\lbrace (x,y)\in\mathbb R^2: x^2-y^2\ne1\rbrace$ is

(A) $1$

(B) $2$

(C) $3$

(D) $4$

**Q9.** `[Application]` ★★★ In $\mathbb R$ with the usual metric, which of the following is true?

(A) $\mathbb Q$ is an $F_\sigma$ set but not a $G_\delta$ set.

(B) The set of irrationals is an $F_\sigma$ set.

(C) $\mathbb Q$ is a $G_\delta$ set.

(D) $\mathbb R$ can be written as a countable union of nowhere dense sets.

**Q10.** `[Concept]` ★★ Which of the following functions is uniformly continuous on the given domain?

(A) $\sqrt x$ on $[0,\infty)$

(B) $1/x$ on $(0,1)$

(C) $\sin(1/x)$ on $(0,1)$

(D) $x\sin x$ on $\mathbb R$

**Q11.** `[Application]` ★★ Which of the following exists?

(A) A continuous map from $(0,1)$ onto $[0,1]$

(B) A continuous map from $[0,1]$ onto $(0,1)$

(C) A continuous map from $[0,1]$ onto $\mathbb R$

(D) A continuous map from $[0,1]$ onto $\lbrace 0,1\rbrace$

**Q12.** `[Multi-Statement]` ★★★ Let $X$ be an infinite set with the discrete metric. Consider the following statements.

I. Every subset of $X$ is both open and closed.

II. $X$ is complete but not compact.

III. Every function from $X$ to any metric space is uniformly continuous.

Which is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q13.** `[Concept]` ★★ In $\mathbb R$, the sets $F_n=[n,\infty)$ are non-empty, closed and nested, but $\bigcap_n F_n=\varnothing$. Which hypothesis of Cantor's intersection theorem fails?

(A) Completeness of the space

(B) Closedness of the $F_n$

(C) $\mathop{\mathrm{diam}}\nolimits(F_n)\to0$

(D) $F_{n+1}\subseteq F_n$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | C | Concept |
| 3 | B | Multi-Statement |
| 4 | B | Assertion-Reason |
| 5 | C | Match |
| 6 | D | NOT-true / Counterexample |
| 7 | B | Numerical |
| 8 | C | Numerical |
| 9 | A | Application |
| 10 | A | Concept |
| 11 | A | Application |
| 12 | D | Multi-Statement |
| 13 | C | Concept |

## Solutions
**Q1 — (D).** $\mathbb R$ is complete. (C) is the trap: $\tan^{-1}$ makes $\mathbb R$ isometric to $(-\pi/2,\pi/2)$, and $x_n=n$ is Cauchy for this metric but does not converge. Completeness is a metric property, not a topological one. (A) and (B) are standard incomplete spaces.

**Q2 — (C).** Compact $\iff$ complete and totally bounded $\iff$ sequentially compact. "Closed and bounded" (Heine–Borel) works only in $\mathbb R^n$, or in general finite-dimensional normed spaces.

**Q3 — (B).** Compactness and connectedness are preserved by continuous images. Completeness is not: $\tan^{-1}:\mathbb R\to(-\pi/2,\pi/2)$ is continuous and onto, from a complete space to an incomplete one.

**Q4 — (B).** A: with $x_n=n$ and $y_n=n+\frac1n$, $|x_n-y_n|\to0$ but $|x_n^2-y_n^2|\to2$. R is the Heine–Cantor theorem. But $\mathbb R$ is not compact, so R says nothing about A.

**Q5 — (C).** $\mathbb Q$: not complete (3). $[0,1]$: compact (1). $\mathbb R$: complete, connected and not compact (2). Discrete $\mathbb R$: complete (Cauchy sequences are eventually constant), but uncountable and discrete, so not separable (4). Each property in List-II belongs to only one space.

**Q6 — (D).** In $\ell^2$, the sequence $e_n$ is bounded but $\Vert e_n-e_m\Vert =\sqrt2$ for $n\neq m$, so no subsequence converges. (A) and (B) are true for the same reason, and (C) is standard.

**Q7 — (B).** $|T'(x)|=\left|\frac12-\frac1{x^2}\right|\le\frac12$ on $[1,\infty)$. Also $T(x)\ge\sqrt2\ge1$ by AM–GM, so $T$ maps $[1,\infty)$ into itself. The fixed point solves $x=\frac x2+\frac1x$, i.e. $x^2=2$, so $x=\sqrt2$. (This is Newton's iteration for $\sqrt2$.)

**Q8 — (C).** The hyperbola $x^2-y^2=1$ has two branches, which cut the plane into three regions: $x^2-y^2\lt 1$ (the middle, connected) and $x\gt \sqrt{1+y^2}$ and $x\lt -\sqrt{1+y^2}$. Answer (D) comes from wrongly counting quadrants, as for $x^2-y^2\ne0$.

**Q9 — (A).** $\mathbb Q=\bigcup\lbrace q\rbrace$ is a countable union of closed sets, so it is $F_\sigma$. If $\mathbb Q=\bigcap U_n$ with $U_n$ open, each $U_n$ would be open and dense. Together with the dense open sets $\mathbb R\setminus\lbrace q\rbrace$, this gives countably many dense open sets with empty intersection, contradicting Baire. So $\mathbb Q$ is not $G_\delta$, and equivalently the irrationals are not $F_\sigma$. (D) also contradicts Baire.

**Q10 — (A).** $\sqrt x$ is uniformly continuous, since $|\sqrt x-\sqrt y|\le\sqrt{|x-y|}$. $\sin(1/x)$ and $1/x$ do not extend continuously to $[0,1]$, so they are not uniformly continuous on $(0,1)$. $x\sin x$ is not uniformly continuous: take $x_n=2n\pi$ and $y_n=2n\pi+\frac1n$; then $|f(y_n)-f(x_n)|\approx 2\pi$.

**Q11 — (A).** For example $f(x)=\frac{1+\sin(4\pi x)}{2}$ maps $(0,1)$ onto $[0,1]$. (B) and (C) are impossible, since a continuous image of a compact set is compact (and bounded). (D) is impossible, since a continuous image of a connected set is connected.

**Q12 — (D).** I: every singleton is an open ball $B(x,\tfrac12)$, so every set is open, and its complement is open too. II: Cauchy sequences are eventually constant, so $X$ is complete. The cover by singletons has no finite subcover, so $X$ is not compact. III: $\delta=\tfrac12$ works for every $\varepsilon$.

**Q13 — (C).** $\mathbb R$ is complete and the $F_n$ are closed, nested and non-empty, but $\mathop{\mathrm{diam}}\nolimits F_n=\infty$. With $\mathop{\mathrm{diam}}\nolimits\to0$ the intersection is exactly one point. (Alternatively, compactness of $F_1$ would also do.)
