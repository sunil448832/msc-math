# Cheatsheet · Unit 3 · Topic 08 — Metric Spaces
> Questions: [../Questions/08-Metric-Spaces.md](../Questions/08-Metric-Spaces.md)

## 1. Basics
- **Metric axioms:**
  - $d(x,y)\ge0$, with $d(x,y)=0\iff x=y$
  - symmetry: $d(x,y)=d(y,x)$
  - triangle inequality: $d(x,z)\le d(x,y)+d(y,z)$
- **Building new metrics from $d$:**
  - Bounded metrics $\frac{d}{1+d}$ and $\min(d,1)$ give the same topology and the same Cauchy sequences.
  - $|\tan^{-1}x-\tan^{-1}y|$ gives the same topology on $\mathbb R$, but **different Cauchy sequences**.
- **Discrete metric:** every set is open and closed, every function on it is uniformly continuous, it is complete, and it is compact $\iff$ finite and separable $\iff$ countable.
- **Interior, closure, limit points:** $\bar A=A\cup A'$ and $x\in\bar A\iff$ some sequence in $A$ converges to $x$.
- In a metric space, the closed ball $\bar B(x,r)$ need not equal $\overline{B(x,r)}$ (discrete metric, $r=1$).
- **Dense:** $\bar A=X$. **Nowhere dense:** $\operatorname{int}\bar A=\varnothing$. **Separable:** has a countable dense subset.

## 2. Convergence and continuity
- Limits are unique (metric spaces are Hausdorff). A convergent sequence is Cauchy, and a Cauchy sequence is bounded.
- A Cauchy sequence with a convergent subsequence converges.
- **Equivalent definitions of continuity:** $\varepsilon$–$\delta$; sequential ($x_n\to x\Rightarrow f(x_n)\to f(x)$); preimage of open is open; preimage of closed is closed.
- **Uniformly continuous:** $\delta$ depends only on $\varepsilon$. Lipschitz $\Rightarrow$ uniformly continuous $\Rightarrow$ continuous.
- A uniformly continuous map sends Cauchy sequences to Cauchy sequences (a merely continuous map need not: $1/x$ on $(0,1)$).
- $f$ uniformly continuous on a dense $A\subseteq X$, with values in a complete $Y$ $\Rightarrow$ $f$ has a unique continuous extension to $X$.
- **On a bounded interval $(a,b)$:** $f$ is uniformly continuous $\iff$ $f$ extends continuously to $[a,b]$.

| Function | Uniformly continuous? |
|---|---|
| $\sqrt x$ on $[0,\infty)$ | Yes (Hölder-$\frac12$) |
| $\sin x$, $\tan^{-1}x$, $\lvert x\rvert$ on $\mathbb R$ | Yes (Lipschitz) |
| $x\sin(1/x)$ on $(0,1)$ | Yes (extends) |
| $x^2$, $x\sin x$, $e^x$, $\sin(x^2)$ on $\mathbb R$ | No |
| $1/x$, $\sin(1/x)$ on $(0,1)$ | No |
| $1/x$ on $[1,\infty)$ | Yes |
| $f$ with bounded derivative | Yes |

## 3. Completeness
- **Complete:** every Cauchy sequence converges.
  - Complete: $\mathbb R^n$, $\ell^p$, $C[a,b]$ with $\|\cdot\|_\infty$, $L^p$.
  - Not complete: $\mathbb Q$, $(0,1)$, $(C[0,1],\|\cdot\|_1)$, polynomials with sup norm.
- A closed subset of a complete space is complete, and a complete subspace of any metric space is closed.
- **Cantor intersection theorem:** $X$ is complete $\iff$ every nested sequence of non-empty closed sets with $\operatorname{diam}\to0$ has intersection **exactly one point**.
- **Baire category theorem:** in a complete metric space, a countable intersection of dense open sets is dense. Equivalently, a non-empty complete space is not a countable union of nowhere dense sets (it is of second category).
  - $\mathbb Q$ is not $G_\delta$, and the irrationals are not $F_\sigma$.
  - A complete metric space without isolated points is uncountable.
  - An infinite-dimensional Banach space has no countable Hamel basis.
  - There is no function continuous exactly on $\mathbb Q$.
- **Banach contraction principle:** if $X$ is complete (and non-empty) and $d(Tx,Ty)\le\alpha d(x,y)$ with $0\le\alpha<1$, then $T$ has a **unique** fixed point $x^*$, and $T^nx_0\to x^*$ for every $x_0$, with error
  $$d(x_n,x^*)\le\frac{\alpha^n}{1-\alpha}d(x_1,x_0).$$
  - Strict "$<$" without a uniform $\alpha<1$ is **not** enough: $x+\frac1x$ on $[1,\infty)$ has $|Tx-Ty|<|x-y|$ but no fixed point.
  - On a compact space, $d(Tx,Ty)<d(x,y)$ does suffice.
- Every metric space has a **completion**, unique up to isometry.

## 4. Compactness
- **Equivalent conditions (metric spaces):** compact $\iff$ sequentially compact $\iff$ complete and totally bounded $\iff$ every infinite subset has a limit point (Bolzano–Weierstrass property).
- **Heine–Borel:** in $\mathbb R^n$, compact $\iff$ closed and bounded. This fails in general: unit ball of $\ell^2$; bounded infinite discrete spaces.
- Compact $\Rightarrow$ closed, bounded, complete and separable. A closed subset of a compact set is compact.
- **Continuous images:** a continuous image of a compact set is compact.
  - A continuous $f:K\to\mathbb R$ attains its max and min.
  - A continuous function on a compact set is uniformly continuous (Heine–Cantor).
  - A continuous bijection from a compact space onto a Hausdorff space is a homeomorphism.
- **Lebesgue number lemma:** every open cover of a compact metric space has a Lebesgue number $\delta>0$.
- A finite product of compact spaces is compact. **Riesz:** the closed unit ball of a normed space is compact $\iff$ the dimension is finite.

## 5. Connectedness
- **Connected:** not a union of two disjoint non-empty open sets. Equivalently, every continuous $f:X\to\{0,1\}$ is constant.
- **Subsets of $\mathbb R$:** connected $\iff$ interval.
- Continuous image of connected is connected (this gives the IVT). Closure of connected is connected. A union of connected sets with a common point is connected.
- **Path-connected $\Rightarrow$ connected.** The converse fails: the topologist's sine curve $\{(x,\sin\frac1x)\}\cup(\{0\}\times[-1,1])$. For open subsets of $\mathbb R^n$ the two notions agree.
- **Totally disconnected:** $\mathbb Q$, the irrationals, the Cantor set.
- **Standard component counts:**

| Set | Components |
|---|---|
| $GL_n(\mathbb R)$ | 2 |
| $GL_n(\mathbb C)$ | 1 |
| $O(n)$ | 2 |
| $SO(n)$ | 1 |
| $\mathbb R^2\setminus\{xy=0\}$ | 4 |
| $\{x^2-y^2\ne1\}$ | 3 |
| $\{x^2-y^2\ne0\}$ | 4 |
| $\mathbb R^n\setminus\{\text{countable set}\}$, $n\ge2$ | 1 (path-connected) |
| $\mathbb R\setminus\{\text{point}\}$ | 2 |

- **Homeomorphism invariants:**
  - $\mathbb R$ is not homeomorphic to $\mathbb R^2$ (remove a point).
  - $[0,1]$ is not homeomorphic to $S^1$.
  - $(0,1)\cong\mathbb R$, but $[0,1]\not\cong(0,1)$.

## 6. Which properties survive?
| Property | Continuous image | Homeomorphism | Closed subset | Finite product |
|---|---|---|---|---|
| Compact | ✔ | ✔ | ✔ | ✔ |
| Connected | ✔ | ✔ | ✘ | ✔ |
| Complete | ✘ | ✘ | ✔ | ✔ |
| Bounded | ✘ | ✘ | ✔ | ✔ |
| Separable | ✔ | ✔ | ✔ (metric case) | ✔ |

## Exam traps
- Completeness and boundedness are **not topological**: $\mathbb R\cong(0,1)$.
- "Closed and bounded $\Rightarrow$ compact" holds only in finite dimensions.
- Cantor intersection needs $\operatorname{diam}\to0$ (or compactness). Contraction needs a uniform $\alpha<1$ **and** completeness.
- Uniform continuity on $(a,b)$ is the same as continuous extendability to $[a,b]$. That test only works on **bounded** intervals.
- Connected does not imply path-connected (topologist's sine curve).
- Continuous onto maps $(0,1)\to[0,1]$ exist, but $[0,1]\to(0,1)$ onto maps do not.
