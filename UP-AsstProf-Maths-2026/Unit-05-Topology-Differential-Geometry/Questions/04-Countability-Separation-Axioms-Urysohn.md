# Unit 5 · Topic 04 — Countability and Separation Axioms; Urysohn's Lemma and Metrization Theorem
> Syllabus coverage: countability, separation axioms, Urysohn's Metrization theorem
> Cheatsheet: [../Cheatsheets/04-Countability-Separation-Axioms-Urysohn.md](../Cheatsheets/04-Countability-Separation-Axioms-Urysohn.md)

**Q1.** `[Concept]` ★ Urysohn's metrization theorem states that a topological space is metrizable if it is

(A) Hausdorff and first countable

(B) regular, $T_1$ and second countable

(C) normal and separable

(D) compact and Hausdorff

**Q2.** `[Multi-Statement]` ★★ For the lower limit line $\mathbb R_l$, consider:

I. $\mathbb R_l$ is first countable.

II. $\mathbb R_l$ is separable.

III. $\mathbb R_l$ is Lindelöf.

IV. $\mathbb R_l$ is second countable.

Which of the above are correct?

(A) I and II only

(B) I, II and III only

(C) II, III and IV only

(D) I, II, III and IV

**Q3.** `[Assertion-Reason]` ★★

**Assertion (A):** The lower limit line $\mathbb R_l$ is not metrizable.

**Reason (R):** In a metrizable space separability implies second countability, and $\mathbb R_l$ is separable but not second countable.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q4.** `[Match]` ★★ Match each space (List-I) with the strongest property it has from List-II.

| List-I | List-II |
|---|---|
| A. Infinite set with the cofinite topology | 1. $T_0$ but not $T_1$ |
| B. Sierpiński space $\lbrace 0,1\rbrace$, $\tau=\lbrace \emptyset,\lbrace 1\rbrace ,\lbrace 0,1\rbrace \rbrace$ | 2. Regular but not normal |
| C. $\mathbb R_K$ ($K$-topology) | 3. $T_1$ but not Hausdorff |
| D. Sorgenfrey plane $\mathbb R_l\times\mathbb R_l$ | 4. Hausdorff but not regular |

(A) A-3, B-1, C-4, D-2

(B) A-1, B-3, C-4, D-2

(C) A-3, B-1, C-2, D-4

(D) A-4, B-1, C-3, D-2

**Q5.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) Every metric space is normal.

(B) Every compact Hausdorff space is normal.

(C) Every subspace of a normal space is normal.

(D) Every regular Lindelöf space is normal.

**Q6.** `[Numerical]` ★★ The number of $T_0$ topologies on a set with 3 elements is

(A) 9

(B) 19

(C) 25

(D) 29

**Q7.** `[Concept]` ★ "For any two disjoint closed sets $A,B$ there is a continuous $f:X\to[0,1]$ with $f|_A=0$ and $f|_B=1$." By Urysohn's lemma this property holds in every

(A) Hausdorff space

(B) regular space

(C) first countable space

(D) normal space

**Q8.** `[Application]` ★★★ Which of the following spaces is NOT metrizable?

(A) $[0,1]^{\mathbb N}$ with the product topology

(B) $\mathbb R^\omega$ with the uniform topology

(C) $[0,1]^{\mathbb R}$ with the product topology

(D) $\ell^2$ with its norm topology

**Q9.** `[Multi-Statement]` ★★ Consider:

I. Every second countable space is separable and Lindelöf.

II. Every separable space is second countable.

III. For a metrizable space: second countable $\iff$ separable $\iff$ Lindelöf.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) I, II and III

(D) I and III only

**Q10.** `[Application]` ★★ $\mathbb R_l$ is normal, but $\mathbb R_l\times\mathbb R_l$ is not. This example shows that

(A) a product of normal spaces need not be normal

(B) a product of regular spaces need not be regular

(C) a product of Hausdorff spaces need not be Hausdorff

(D) a product of separable spaces need not be separable

**Q11.** `[Application]` ★★ An uncountable set $X$ with the discrete topology is

(A) metrizable but not second countable

(B) second countable

(C) not first countable

(D) not normal

**Q12.** `[NOT-true / Counterexample]` ★★★ Which of the following conditions is NOT sufficient for a topological space to be metrizable?

(A) Compact, Hausdorff and second countable

(B) Regular, $T_1$ and second countable

(C) Hausdorff and second countable

(D) Normal, $T_1$ and second countable

**Q13.** `[Numerical]` ★ A $T_1$ topology on a set with 5 elements has exactly how many open sets?

(A) 5

(B) 6

(C) 16

(D) 32

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | B | Multi-Statement |
| 3 | A | Assertion-Reason |
| 4 | A | Match |
| 5 | C | NOT-true |
| 6 | B | Numerical |
| 7 | D | Concept |
| 8 | C | Application |
| 9 | D | Multi-Statement |
| 10 | A | Application |
| 11 | A | Application |
| 12 | C | NOT-true |
| 13 | D | Numerical |

## Solutions
**Q1 — (B).** Urysohn: regular + $T_1$ + second countable $\Rightarrow$ metrizable. The proof embeds the space in $[0,1]^{\mathbb N}$. Compact Hausdorff spaces need not be metrizable (Q8 (C)), and neither do Hausdorff first countable spaces ($\mathbb R_l$).

**Q2 — (B).** $\lbrace [x,x+1/n)\rbrace$ is a countable local base, so $\mathbb R_l$ is first countable. $\mathbb Q$ is dense, so it is separable. It is Lindelöf (standard). It is not second countable: each basis must contain a set with minimum $x$ for every $x$.

**Q3 — (A).** In a metric space, the balls of rational radius around the points of a countable dense set form a countable basis. Since $\mathbb R_l$ is separable but not second countable, it cannot be metrizable. R explains A.

**Q4 — (A).** Cofinite: points are closed but there is no Hausdorff separation. Sierpiński: $T_0$, but $\lbrace 1\rbrace$ is not closed. $\mathbb R_K$: Hausdorff, but $0$ and the closed set $K$ cannot be separated. Sorgenfrey plane: regular (a product of regular spaces) but not normal, since its anti-diagonal is closed and discrete.

**Q5 — (C).** Normality is not hereditary. $[0,\omega_1]\times[0,\omega]$ is compact Hausdorff, hence normal, but its subspace with the corner point removed (the deleted Tychonoff plank) is not normal. Another route: every Tychonoff space embeds in a compact Hausdorff cube $[0,1]^J$, and some Tychonoff spaces, such as the Sorgenfrey plane, are not normal. Normality is inherited only by **closed** subspaces. (A), (B) and (D) are standard theorems.

**Q6 — (B).** Of the 29 topologies on 3 points, 19 are $T_0$. These correspond to the 19 partial orders on a 3-element set (verified by brute force).

**Q7 — (D).** This is Urysohn's lemma, and the property actually *characterises* normality. In a regular space, two disjoint closed sets need not even be separated by open sets (the Sorgenfrey plane is an example). Even a point and a closed set may fail to be separated by a function, because regular does not imply completely regular.

**Q8 — (C).** An uncountable product of non-trivial spaces is not first countable, so it is not metrizable, even though it is compact Hausdorff. The Hilbert cube is metrizable (countable product). The uniform topology and $\ell^2$ come from metrics.

**Q9 — (D).** I: pick one point from each basic set, and use a countable basis to reduce covers. II fails for $\mathbb R_l$. III is the standard metric equivalence.

**Q10 — (A).** The Sorgenfrey plane is regular and separable (products preserve regularity and countable products of separable spaces are separable), so (B) and (D) are false statements. Hausdorffness is always preserved by products, so (C) is false too.

**Q11 — (A).** It is metrizable by the discrete metric, hence first countable and normal. It is not second countable, because every basis must contain every singleton $\lbrace x\rbrace$, and there are uncountably many.

**Q12 — (C).** $\mathbb R_K$ is Hausdorff and second countable (use rational endpoints) but not regular, hence not metrizable. Each of (A), (B) and (D) implies regular + $T_1$ + second countable, so Urysohn applies.

**Q13 — (D).** In a finite $T_1$ space every subset is a finite union of closed points, hence closed. So every subset is open and the topology is discrete, with $2^5=32$ open sets.
