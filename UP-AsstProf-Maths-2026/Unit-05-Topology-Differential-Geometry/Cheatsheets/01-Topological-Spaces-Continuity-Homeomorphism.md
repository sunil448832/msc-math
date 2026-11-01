# Cheatsheet · Unit 5 · Topic 01 — Topological Spaces, Continuity, Homeomorphism
> Questions: [../Questions/01-Topological-Spaces-Continuity-Homeomorphism.md](../Questions/01-Topological-Spaces-Continuity-Homeomorphism.md)

## 1. Topology, basis, subbasis
- **Topology** $\tau$ on $X$: contains $\emptyset, X$, and is closed under arbitrary unions and finite intersections.
- **Basis** $\mathcal{B}$: (i) the members cover $X$; (ii) if $x\in B_1\cap B_2$, then there is $B_3\in\mathcal B$ with $x\in B_3\subseteq B_1\cap B_2$. The open sets are the unions of basis elements.
- **Subbasis** $\mathcal S$: any family covering $X$. The finite intersections of its members form a basis. *Example:* rays $(a,\infty),(-\infty,b)$ form a subbasis (not a basis) for the usual topology of $\mathbb{R}$.
- Comparing topologies: $\tau'$ is finer than $\tau$ iff for each $x\in B\in\mathcal B$ there is $B'\in\mathcal B'$ with $x\in B'\subseteq B$.

## 2. Standard topologies on $\mathbb{R}$ (and on a set $X$)
| Topology | Open sets / basis | Key facts |
|---|---|---|
| Discrete | all subsets | every function out of it is continuous; metrizable |
| Indiscrete | $\lbrace \emptyset,X\rbrace$ | every function into it is continuous; not $T_0$ if $\vert X\vert \ge2$ |
| Cofinite | $\emptyset$ and complements of finite sets | $T_1$, not $T_2$ ($X$ infinite); compact; every subspace is compact; connected if $X$ infinite |
| Cocountable | $\emptyset$ and complements of countable sets | $T_1$, not $T_2$ ($X$ uncountable); **not** compact; Lindelöf; convergent sequences are eventually constant |
| Lower limit $\mathbb R_l$ | basis $[a,b)$ | strictly finer than usual; $[a,b)$ is clopen; totally disconnected; first countable, separable, Lindelöf, **not** second countable, not metrizable; normal |
| $K$-topology $\mathbb R_K$ | $(a,b)$ and $(a,b)\setminus K$, with $K=\lbrace 1/n\rbrace$ | Hausdorff, not regular |

Fineness on $\mathbb{R}$: cofinite $\subsetneq$ usual $\subsetneq$ $\mathbb R_l$, and usual $\subsetneq \mathbb R_K$. The topologies $\mathbb R_l$ and $\mathbb R_K$ are not comparable.

## 3. Closure, interior, boundary
- $\overline A$ = smallest closed set containing $A$ = $A\cup A'$ ($A'$ = the set of limit points). $x\in\overline A$ iff every basic neighbourhood of $x$ meets $A$.
- $\mathrm{int}A$ = largest open set inside $A$. $\partial A=\overline A\setminus\mathrm{int}A=\overline A\cap\overline{X\setminus A}$.
- $\overline{A\cup B}=\overline A\cup\overline B$, but in general $\overline{A\cap B}\subsetneq\overline A\cap\overline B$. Similarly $\mathrm{int}(A\cap B)=\mathrm{int}A\cap\mathrm{int}B$.
- $X\setminus\overline A=\mathrm{int}(X\setminus A)$.
- Kuratowski: at most **14** distinct sets can be obtained from one set by repeatedly taking closure and complement.

| Set $(0,1)$ in … | closure | interior of $[0,1]$ |
|---|---|---|
| usual | $[0,1]$ | $(0,1)$ |
| cofinite | $\mathbb{R}$ | $\emptyset$ |
| cocountable | $\mathbb{R}$ | $\emptyset$ |
| $\mathbb R_l$ | $[0,1)$ | $[0,1)$ |
| upper limit | $(0,1]$ | $(0,1]$ |

In the cocountable topology: $\overline{\mathbb Q}=\mathbb Q$ and $\mathrm{int}\thinspace \mathbb Q=\emptyset$. In the usual topology: $\overline{\mathbb Q}=\mathbb R$, $\partial\mathbb Q=\mathbb R$.

## 4. Counting topologies on finite sets
| $n$ | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| all topologies | 1 | 4 | **29** | 355 | 6942 |
| $T_0$ topologies | 1 | 2 | **19** | 219 | 4231 |
| up to homeomorphism | 1 | 3 | **9** | 33 | 139 |

- A finite $T_1$ space is discrete, so it has $2^n$ open sets.
- Topologies on a finite set correspond to preorders, and $T_0$ topologies correspond to partial orders.

## 5. Continuity
For $f:X\to Y$ the following are equivalent:
1. $f^{-1}(V)$ is open for every open $V$ (it suffices to check basic or subbasic $V$).
2. $f^{-1}(C)$ is closed for every closed $C$.
3. $f(\overline A)\subseteq\overline{f(A)}$ for all $A$.
4. For each $x$ and each neighbourhood $V$ of $f(x)$ there is a neighbourhood $U$ of $x$ with $f(U)\subseteq V$.

Further facts:
- In metric spaces continuity is the same as sequential continuity. In general spaces this holds when $X$ is first countable.
- **Pasting lemma:** if $X=A\cup B$ with $A,B$ both closed (or both open) and $f|_A,f|_B$ continuous and agreeing on $A\cap B$, then $f$ is continuous.
- $\mathrm{id}:(X,\tau_1)\to(X,\tau_2)$ is continuous iff $\tau_2\subseteq\tau_1$.
- Any map from a discrete space is continuous, and any map into an indiscrete space is continuous.
- A continuous map from an infinite cofinite space (or any space in which two non-empty open sets always meet) to a Hausdorff space is **constant**.
- **Open map:** images of open sets are open. **Closed map:** images of closed sets are closed. These are independent of continuity.

## 6. Homeomorphism
- A homeomorphism is a bijection $f$ with $f$ and $f^{-1}$ continuous, equivalently a continuous open bijection (or a continuous closed bijection).
- A continuous bijection need **not** be a homeomorphism: $[0,2\pi)\to S^1$; $\mathrm{id}:\text{discrete}\to\text{usual}$.
- A continuous bijection from a compact space to a Hausdorff space **is** a homeomorphism.
- **Topological properties** (preserved by homeomorphisms): compactness, connectedness, path-connectedness, $T_i$ axioms, countability axioms, metrizability, number of components, cut-points.
- **Not topological:** boundedness, completeness, Cauchy-ness, diameter, total boundedness. Example: $(0,1)\cong\mathbb{R}$.

**Standard homeomorphisms and non-homeomorphisms**
- $(a,b)\cong(0,1)\cong\mathbb{R}$; $S^n\setminus\lbrace pt\rbrace \cong\mathbb R^n$ (stereographic projection); open disc $\cong\mathbb R^2$.
- $[0,1]\not\cong(0,1)$ (compactness).
- $[0,1)\not\cong(0,1)$: removing $0$ from $[0,1)$ leaves it connected, but removing any point from $(0,1)$ disconnects it.
- $\mathbb{R}\not\cong\mathbb R^2$ (removing a point); $S^1\not\cong[0,1]$; $\mathbb R^m\cong\mathbb R^n\iff m=n$ (invariance of domain).

## Exam traps
- Rays form a **subbasis**, not a basis.
- The cofinite topology is $T_1$ but not $T_2$, and it is compact. The cocountable topology is $T_1$, not $T_2$, and **not** compact.
- In $\mathbb R_l$, $[a,b)$ is clopen and $\overline{(0,1)}=[0,1)$, not $[0,1]$.
- The identity map is continuous when the domain topology is **finer**.
- 29 labelled topologies on 3 points, but only 9 up to homeomorphism, and 19 of them are $T_0$.
- Boundedness and completeness are **not** topological properties.
- A continuous bijection is not automatically a homeomorphism; it is one when the domain is compact and the codomain Hausdorff.
