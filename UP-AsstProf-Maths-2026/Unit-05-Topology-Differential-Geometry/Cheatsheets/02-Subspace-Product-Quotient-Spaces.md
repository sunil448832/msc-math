# Cheatsheet · Unit 5 · Topic 02 — Subspace, Product, Quotient Spaces; Tychonoff
> Questions: [../Questions/02-Subspace-Product-Quotient-Spaces.md](../Questions/02-Subspace-Product-Quotient-Spaces.md)

## 1. Subspace topology
- $Y\subseteq X$: $\tau_Y=\{U\cap Y: U\in\tau_X\}$. A basis is $\{B\cap Y\}$.
- **Closed sets:** $C$ is closed in $Y$ iff $C=F\cap Y$ with $F$ closed in $X$. Also $\mathrm{cl}_Y(A)=\mathrm{cl}_X(A)\cap Y$.
- Open in $Y$ implies open in $X$ **iff** $Y$ is open in $X$. Similarly for closed sets.
- Examples:
  - $[0,\tfrac12)$ is open in $[0,1)$.
  - $\mathbb Z\subset\mathbb R$ is discrete.
  - $\{1/n\}\subset\mathbb R$ is discrete, but $\{0\}\cup\{1/n\}$ is not.
  - $\mathbb Q$ is not discrete.
- **Hereditary properties:** $T_0,T_1,T_2,T_3$, metrizability, first and second countability are hereditary. Normality, compactness, connectedness, separability and the Lindelöf property are **not**; they pass to closed subspaces (normal, compact, Lindelöf) or to open subspaces (separable).
- The inclusion map is continuous. The restriction of a continuous map is continuous.

## 2. Product topology vs box topology
| | Product topology | Box topology |
|---|---|---|
| Basis | $\prod U_\alpha$, with $U_\alpha=X_\alpha$ for all but finitely many $\alpha$ | $\prod U_\alpha$, all $U_\alpha$ open |
| Characterisation | coarsest topology making all $\pi_\alpha$ continuous | finer than the product topology |
| $f:Z\to\prod X_\alpha$ continuous $\iff$ all $\pi_\alpha f$ continuous | ✔ | ✘ ($t\mapsto(t,t,\dots)$) |
| Product of compact spaces is compact | ✔ (Tychonoff) | ✘ ($\{0,1\}^{\mathbb N}$ box is discrete) |
| $\mathbb R^\omega$ connected | ✔ | ✘ (bounded/unbounded split) |
| $\mathbb R^\omega$ metrizable | ✔ ($D(x,y)=\sup_n \bar d(x_n,y_n)/n$) | ✘ |
| Finite products | equal | equal |

- For $\mathbb R^\omega$: product $\subsetneq$ uniform $\subsetneq$ box.
- Projections are **open, continuous, surjective**, but not closed in general ($xy=1$).
- The following properties **are preserved** by arbitrary products (product topology): Hausdorff, regular, completely regular, connected, path-connected, compact (Tychonoff).
- Countable products preserve metrizability, first countability and second countability.
- The following are **not preserved** by products: normality ($\mathbb R_l\times\mathbb R_l$), the Lindelöf property ($\mathbb R_l\times\mathbb R_l$), and paracompactness. Separability passes to products of at most $\mathfrak c$ separable spaces (Hewitt–Marczewski–Pondiczery).
- $\overline{\prod A_\alpha}=\prod\overline{A_\alpha}$ in both topologies.
- Uncountable products of non-trivial (at least two points, Hausdorff) spaces are not first countable, hence not metrizable. Example: $[0,1]^{\mathbb R}$ is compact but not metrizable.

## 3. Quotient spaces
- For a surjective $p:X\to Y$, $V\subseteq Y$ is open iff $p^{-1}(V)$ is open in $X$. This is the **finest** topology on $Y$ making $p$ continuous.
- **Universal property:** $g:Y\to Z$ is continuous iff $g\circ p$ is continuous.
- A continuous surjection that is open or closed is a quotient map.
- A quotient map need not be open or closed. A restriction of a quotient map need not be a quotient map. A product of two quotient maps need not be a quotient map (it is one if the other factor is locally compact Hausdorff).
- **Quotients do NOT preserve** Hausdorff, first or second countability, or metrizability.
- **Quotients DO preserve** compactness, connectedness, path-connectedness and separability (these are continuous images).

| Identification on $I^2$ (edge word) | Space |
|---|---|
| $I/\{0\sim1\}$ | $S^1$ |
| $aba^{-1}b^{-1}$: both pairs, same direction | torus $T^2$ |
| $abab^{-1}$: one pair reversed | Klein bottle |
| $abab$: both pairs reversed | $\mathbb{RP}^2$ |
| only one pair, reversed | Möbius band |
| only one pair, same direction | cylinder |
| $D^2/\partial D^2$ | $S^2$ |
| $D^n/\partial D^n$ | $S^n$ |
| $S^n/(x\sim-x)$ | $\mathbb{RP}^n$ |
| $\mathbb R/\mathbb Z$ | $S^1$ |
| $\mathbb R^2/\mathbb Z^2$ | torus |

- $\mathbb R/\mathbb Q$ (cosets) is **indiscrete**.
- $\mathbb R$ with $\mathbb Z$ collapsed to a point is Hausdorff (it collapses a closed set in a normal space) but **not first countable** at that point, so it is not metrizable. Collapsing $\mathbb Q$ (not closed) gives a non-Hausdorff space.
- The line with two origins is a quotient of two lines that is $T_1$ but not Hausdorff.

## 4. Tychonoff's theorem
> **Theorem.** An arbitrary product of compact spaces is compact in the **product topology**.

- The proof uses Zorn's lemma or ultrafilters (Alexander subbasis lemma). Over ZF the theorem is **equivalent to AC** (Kelley). The Hausdorff version is equivalent to the ultrafilter lemma (BPI).
- Consequences:
  - $[0,1]^J$ (Tychonoff cube) and the Hilbert cube $[0,1]^{\mathbb N}$ are compact.
  - The Cantor set $\cong\{0,1\}^{\mathbb N}$ is compact.
  - Banach–Alaoglu: the closed unit ball of $X^*$ is weak-* compact.
  - Every completely regular ($T_{3\frac12}$) space embeds in some $[0,1]^J$, hence has a compactification (Stone–Čech).
- Converse: if $\prod X_\alpha\ne\emptyset$ is compact, then each $X_\alpha$ is compact (continuous image under $\pi_\alpha$).

## Exam traps
- Tychonoff holds for **any** index set, but only in the **product** topology.
- The diagonal map $t\mapsto(t,t,\dots)$ is continuous for the product topology but not the box topology.
- The box topology on $\mathbb R^\omega$ is disconnected and not metrizable.
- Projections are open but **not** closed.
- Quotients of Hausdorff spaces need not be Hausdorff; subspaces and products of Hausdorff spaces are Hausdorff.
- $\mathrm{cl}_Y A=\overline{A}\cap Y$: do not add points that lie outside $Y$.
- Do not mix up the Klein bottle (one pair reversed) and $\mathbb{RP}^2$ (both pairs reversed).
- $[0,1]^{\mathbb R}$ is compact but **not** metrizable (not first countable).
