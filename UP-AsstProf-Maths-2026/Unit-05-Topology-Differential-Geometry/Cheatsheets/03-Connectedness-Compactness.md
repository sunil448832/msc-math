# Cheatsheet · Unit 5 · Topic 03 — Connectedness and Compactness
> Questions: [../Questions/03-Connectedness-Compactness.md](../Questions/03-Connectedness-Compactness.md)

## 1. Connectedness
- $X$ is **connected** if it is not the union of two disjoint non-empty open sets. Equivalently, the only clopen sets are $\emptyset$ and $X$, and every continuous $f:X\to\lbrace 0,1\rbrace$ (discrete) is constant.
- The connected subsets of $\mathbb R$ are exactly the **intervals**, including rays, singletons and $\mathbb R$.
- Rules:
  - A continuous image of a connected space is connected (this gives the Intermediate Value Theorem).
  - If $A$ is connected and $A\subseteq B\subseteq\overline A$, then $B$ is connected.
  - A union of connected sets with a common point is connected.
  - Arbitrary products of connected spaces are connected (product topology).
  - Quotients of connected spaces are connected.
- **Components:** maximal connected subsets. They partition $X$ and are **closed**, but not necessarily open (they are open if there are finitely many, or if $X$ is locally connected).
- **Totally disconnected:** all components are singletons. Examples: $\mathbb Q$, $\mathbb R\setminus\mathbb Q$, the Cantor set, $\mathbb R_l$, discrete spaces.

## 2. Path-connectedness
- Path-connected $\Rightarrow$ connected. The converse is **false**: the topologist's sine curve $\overline{\lbrace (x,\sin1/x):0\lt x\le1\rbrace }$ is connected, not path-connected and not locally connected.
- Connected + locally path-connected $\Rightarrow$ path-connected. In particular, open connected subsets of $\mathbb R^n$ (and connected manifolds) are path-connected.
- Path components $\subseteq$ components. Path components need not be closed.
- **Comb space:** connected, path-connected, but not locally connected.
- **Deleted comb space:** connected but not path-connected.

| Space | number of components |
|---|---|
| $GL_n(\mathbb R)$ | 2 ($\det\gt 0$, $\det\lt 0$) |
| $GL_n(\mathbb C)$, $SL_n(\mathbb R)$, $SO(n)$, $U(n)$ | 1 |
| $O(n)$ | 2 |
| $\mathbb R^n\setminus\lbrace 0\rbrace$ | 2 for $n=1$; 1 for $n\ge2$ |
| hyperbola $x^2-y^2=1$ | 2 |
| hyperboloid $x^2+y^2-z^2=-1$ | 2 (two sheets) |
| hyperboloid $x^2+y^2-z^2=1$ | 1 |

**Cut-point invariants** (a cut point is one whose removal disconnects the space): $[0,1]$ has cut points, $S^1$ has none. $\mathbb R$ minus a point is disconnected, $\mathbb R^2$ minus a point is not. So $[0,1]\not\cong S^1$, $\mathbb R\not\cong\mathbb R^2$ and $[0,1)\not\cong(0,1)$.

## 3. Compactness
- $X$ is **compact** if every open cover has a finite subcover. Equivalently, every family of closed sets with the finite intersection property (FIP) has non-empty intersection.
- Facts:
  - A closed subset of a compact space is compact.
  - A compact subset of a **Hausdorff** space is closed.
  - A continuous image of a compact space is compact.
  - A continuous $f:K\to\mathbb R$ on compact $K$ is bounded and attains its max and min (EVT).
  - A continuous bijection from a compact space to a Hausdorff space is a homeomorphism.
  - A finite union of compact sets is compact.
  - Tychonoff: products of compact spaces are compact.
- **Heine–Borel:** $K\subseteq\mathbb R^n$ is compact $\iff$ $K$ is closed and bounded. This fails in general metric spaces (discrete metric; the unit ball of $\ell^2$; $\mathbb Q\cap[0,1]$ is bounded but not closed in $\mathbb R$).
- **Metric spaces:** compact $\iff$ sequentially compact $\iff$ limit point compact $\iff$ complete and totally bounded.
- **Lebesgue number lemma:** every open cover of a compact metric space has a Lebesgue number $\delta\gt 0$. Consequence: a continuous map on a compact metric space is uniformly continuous.
- In general spaces, compactness and sequential compactness are independent: $[0,1]^{[0,1]}$ is compact but not sequentially compact, and $\omega_1$ is sequentially compact but not compact.

| Space | Compact? |
|---|---|
| any set, cofinite topology | ✔ (every subset too) |
| uncountable set, cocountable topology | ✘ |
| $[0,1]$ in $\mathbb R_l$ | ✘ |
| $[0,1]$ in $\mathbb R_K$ | ✘ ($K$ is closed and discrete in it) |
| finite space, or any space with finitely many open sets | ✔ |
| infinite discrete space | ✘ |
| indiscrete space | ✔ |
| Cantor set, Hilbert cube, $S^n$, $\mathbb{RP}^n$, torus | ✔ |
| closed unit ball of an infinite-dimensional normed space | ✘ (Riesz) |

## 4. Local compactness and compactification
- $X$ is **locally compact** if each point has a neighbourhood contained in a compact set (for Hausdorff spaces: each point has a neighbourhood base of compact sets).
- Examples: $\mathbb R^n$, discrete spaces, manifolds, every compact space, and open or closed subsets of a locally compact Hausdorff space.
- Non-examples: $\mathbb Q$, $\mathbb R\setminus\mathbb Q$, $\mathbb R^\omega$ (product topology), infinite-dimensional normed spaces.
- **One-point compactification** $X^\ast =X\cup\lbrace \infty\rbrace$, where the neighbourhoods of $\infty$ are complements of closed compact sets. $X^\ast$ is compact. It is Hausdorff $\iff$ $X$ is locally compact Hausdorff.
  - $\mathbb R^\ast \cong S^1$, $(\mathbb R^n)^\ast \cong S^n$, $\mathbb C^\ast \cong S^2$ (Riemann sphere), $\mathbb N^\ast \cong\lbrace 0\rbrace \cup\lbrace 1/n\rbrace$.
- Local compactness is preserved by closed and open subspaces (in Hausdorff spaces) and by **finite** products only.

## Exam traps
- "Closed and bounded $\Rightarrow$ compact" holds only in $\mathbb R^n$ (finite-dimensional normed spaces), not in general metric spaces.
- A compact set is closed only in **Hausdorff** spaces.
- Connected does not imply path-connected. The converse direction is true.
- Components are closed but not always open. Path components need not be closed.
- $GL_n(\mathbb R)$ has 2 components, while $GL_n(\mathbb C)$ is connected.
- $\mathbb Q$ is not locally compact, so its one-point compactification is not Hausdorff.
- Cofinite topology: compact. Cocountable topology on an uncountable set: not compact.
