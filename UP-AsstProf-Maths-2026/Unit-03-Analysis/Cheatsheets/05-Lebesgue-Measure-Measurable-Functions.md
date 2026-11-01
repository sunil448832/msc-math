# Cheatsheet · Unit 3 · Topic 05 — Lebesgue Measure & Measurable Functions
> Questions: [../Questions/05-Lebesgue-Measure-Measurable-Functions.md](../Questions/05-Lebesgue-Measure-Measurable-Functions.md)

## 1. Outer measure
$$m^\ast (E)=\inf\Big\lbrace \sum_k\ell(I_k):\ E\subseteq\bigcup_k I_k,\ I_k\text{ open intervals}\Big\rbrace .$$
- $m^\ast (I)=\ell(I)$ for every interval. $m^\ast$ is monotone, **countably subadditive** and translation invariant, but **not** countably additive on all of $\mathcal P(\mathbb R)$.
- Countable sets have $m^\ast =0$: $\mathbb{N}$, $\mathbb{Z}$, $\mathbb{Q}$, algebraic numbers.
- $m^\ast (E)=\inf\lbrace m(G):G\supseteq E\text{ open}\rbrace$ (outer regularity).

## 2. Measurable sets
- **Carathéodory:** $E$ is measurable $\iff m^\ast (A)=m^\ast (A\cap E)+m^\ast (A\cap E^c)$ for all $A$.
- **Equivalent forms:** for every $\varepsilon\gt 0$ there is an open $G\supseteq E$ with $m^\ast (G\setminus E)\lt \varepsilon$; or a closed $F\subseteq E$ with $m^\ast (E\setminus F)\lt \varepsilon$. Also, $E=G_\delta\setminus(\text{null})=F_\sigma\cup(\text{null})$.
- The measurable sets $\mathcal M$ form a $\sigma$-algebra containing all intervals, open, closed, $G_\delta$, $F_\sigma$ and Borel sets, and all null sets. $m=m^\ast |_{\mathcal M}$ is **countably additive**.
- **Complete:** every subset of a null set is measurable (and null).
- **Cardinalities:** $|\text{Borel}|=\mathfrak c$ but $|\mathcal M|=2^{\mathfrak c}$, so $\text{Borel}\subsetneq\mathcal M\subsetneq\mathcal P(\mathbb R)$.
- **Continuity of measure:** $E_n\uparrow$ ⇒ $m(\bigcup E_n)=\lim m(E_n)$; $E_n\downarrow$ with $m(E_1)\lt \infty$ ⇒ $m(\bigcap E_n)=\lim m(E_n)$. The finiteness is needed: $E_n=[n,\infty)$.
- $m(E+x)=m(E)$ and $m(cE)=|c|\thinspace m(E)$.

## 3. Null sets and Cantor-type sets
| Set | Cardinality | Measure | Notes |
|---|---|---|---|
| countable sets, $\mathbb Q$ | countable | $0$ | dense possible |
| Cantor ternary set $C$ | $\mathfrak c$ | $0$ | compact, perfect, nowhere dense, totally disconnected; removed length $\sum\frac{2^{n-1}}{3^n}=1$ |
| fat Cantor (remove $2^{n-1}$ gaps of length $4^{-n}$) | $\mathfrak c$ | $1/2$ | nowhere dense, positive measure |
| general: remove a total length $\alpha\in(0,1]$ | | $1-\alpha$ | |
| numbers in $[0,1]$ with no digit $7$ | $\mathfrak c$ | $0$ | $(9/10)^n\to0$ |
| $[0,1]\setminus\mathbb Q$ | $\mathfrak c$ | $1$ | dense with dense complement |
- **Null ≠ countable** (Cantor set). **Nowhere dense ≠ null** (fat Cantor). **Dense ≠ positive measure** ($\mathbb Q$).
- An open dense set can have arbitrarily small measure: $\bigcup(r_k-\varepsilon2^{-k},r_k+\varepsilon2^{-k})$.
- **Cantor function $\phi$:** continuous, increasing, onto $[0,1]$, constant on each gap, $\phi'=0$ a.e., maps the null set $C$ onto $[0,1]$. Then $\psi=x+\phi$ is a homeomorphism $[0,1]\to[0,2]$ with $m(\psi(C))=1$.
- Lipschitz maps send null sets to null sets. Continuous maps need not ($\phi$).

## 4. Non-measurable sets
- **Vitali set:** pick one representative from each class of $x\sim y\iff x-y\in\mathbb Q$ in $[0,1]$ (axiom of choice). Disjoint rational translates give $1\le\sum_{r}m(V)\le3$, a contradiction.
- Every set with $m^\ast (E)\gt 0$ contains a non-measurable subset.
- Without the axiom of choice (Solovay), it is consistent that every set is measurable.
- A non-measurable set inside $\psi(C)$ pulls back to a measurable null set that is **not Borel**.

## 5. Measurable functions
- $f:E\to\overline{\mathbb R}$ is measurable $\iff\lbrace f\gt a\rbrace \in\mathcal M$ for every $a$. Equivalent conditions use $\ge,\lt ,\le$, or $f^{-1}(G)$ measurable for every open $G$.
- **Closed under:** $f\pm g$, $fg$, $cf$, $|f|$, $f^+$, $f^-$, $\max/\min$, $\sup_n$, $\inf_n$, $\limsup$, $\liminf$, pointwise limits, and $g\circ f$ for continuous (or Borel) $g$.
- **Not** in general: $f\circ g$ with $g$ continuous. And $|f|$ measurable does not make $f$ measurable ($\chi_V-\chi_{V^c}$).
- Continuous, monotone and step functions are measurable; $\chi_E$ is measurable $\iff E\in\mathcal M$.
- **Almost everywhere:** if $f=g$ a.e. and $f$ is measurable, then $g$ is measurable (completeness). E.g. $\chi_{\mathbb Q}=0$ a.e.
- **Simple approximation:** every measurable $f\ge0$ is the limit of an increasing sequence of simple functions $\phi_n\uparrow f$, uniformly on sets where $f$ is bounded.

## 6. The three principles of Littlewood
| Principle | Theorem | Exact statement |
|---|---|---|
| Every measurable set is nearly a finite union of intervals | Regularity | $m(E)\lt \infty$ ⇒ $\forall\varepsilon$ there are intervals $I_1..I_n$ with $m(E\thinspace \triangle\thinspace \bigcup I_k)\lt \varepsilon$ |
| Every measurable function is nearly continuous | **Lusin** | $f$ measurable on $[a,b]$ (a.e. finite) ⇒ $\forall\varepsilon$ there is a closed $F$ with $m([a,b]\setminus F)\lt \varepsilon$ and $f\vert_F$ continuous. Equivalently, there is $g\in C$ with $m\lbrace f\ne g\rbrace \lt \varepsilon$ |
| Every a.e. convergent sequence is nearly uniformly convergent | **Egorov** | $m(E)\lt \infty$, $f_n$ measurable, $f_n\to f$ a.e. (with $f$ finite a.e.) ⇒ $\forall\varepsilon$ there is a closed $F\subseteq E$ with $m(E\setminus F)\lt \varepsilon$ and $f_n\to f$ uniformly on $F$ |
- The condition $m(E)\lt \infty$ is essential in Egorov: $\chi_{[n,\infty)}$ or $\chi_{[n,n+1]}$ on $\mathbb R$.
- Lusin does **not** say "$`f`$ is continuous at the points of $F$". It says the **restriction** $`f|_F`$ is continuous ($`\chi_{\mathbb Q}`$ restricted to the irrationals).
- **Convergence in measure:** $f_n\to f$ in measure ⇒ some subsequence converges a.e. (Riesz). On a finite-measure domain, a.e. convergence ⇒ convergence in measure. The "typewriter" sequence converges in measure but nowhere pointwise.

## 7. Exam traps
- Countable ⇒ null, but null ⇏ countable.
- Borel ⊊ Lebesgue. "Every Lebesgue set is Borel" is false.
- Outer measure is subadditive, not additive. Additivity fails for disjoint non-measurable sets.
- Continuity from above needs $m(E_1)\lt \infty$, and Egorov needs $m(E)\lt \infty$.
- A continuous image of a null set can have positive measure (Cantor function).
- $f\circ g$ (measurable∘continuous) can be non-measurable, but $g\circ f$ (continuous∘measurable) is fine.
- Nowhere dense sets can have positive measure; dense open sets can have small measure.
