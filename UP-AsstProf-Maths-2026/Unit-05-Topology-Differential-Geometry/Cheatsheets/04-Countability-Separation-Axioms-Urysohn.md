# Cheatsheet · Unit 5 · Topic 04 — Countability, Separation Axioms, Urysohn
> Questions: [../Questions/04-Countability-Separation-Axioms-Urysohn.md](../Questions/04-Countability-Separation-Axioms-Urysohn.md)

## 1. Countability axioms
| Axiom | Definition |
|---|---|
| First countable ($C_1$) | each point has a countable local base |
| Second countable ($C_2$) | the topology has a countable basis |
| Separable | there is a countable dense subset |
| Lindelöf | every open cover has a countable subcover |

- $C_2\Rightarrow C_1$, $C_2\Rightarrow$ separable, and $C_2\Rightarrow$ Lindelöf. None of these converses holds.
- **Metrizable spaces:** $C_2\iff$ separable $\iff$ Lindelöf. Every metric space is $C_1$.
- **Heredity:**
  - $C_1$ and $C_2$ are hereditary, and countable products preserve them.
  - Separability passes to **open** subspaces but not to arbitrary ones: the anti-diagonal of the Sorgenfrey plane is not separable.
  - The Lindelöf property passes to **closed** subspaces only. Products of Lindelöf spaces need not be Lindelöf ($\mathbb R_l^2$).
- In $C_1$ spaces sequences suffice: closure = sequential closure, and continuity = sequential continuity.

| Space | $C_1$ | $C_2$ | Separable | Lindelöf | Metrizable |
|---|---|---|---|---|---|
| $\mathbb R^n$ | ✔ | ✔ | ✔ | ✔ | ✔ |
| $\mathbb R_l$ | ✔ | ✘ | ✔ | ✔ | ✘ |
| $\mathbb R_l\times\mathbb R_l$ | ✔ | ✘ | ✔ | ✘ | ✘ |
| uncountable discrete | ✔ | ✘ | ✘ | ✘ | ✔ |
| $[0,1]^{\mathbb R}$ (product) | ✘ | ✘ | ✔ | ✔ (compact) | ✘ |
| $\mathbb R^\omega$ (product) | ✔ | ✔ | ✔ | ✔ | ✔ |
| uncountable cofinite | ✘ | ✘ | ✔ | ✔ | ✘ |
| $\ell^\infty$ | ✔ | ✘ | ✘ | ✘ | ✔ |
| $\ell^p$, $1\le p<\infty$; $C[0,1]$ | ✔ | ✔ | ✔ | ✔ | ✔ |

## 2. Separation axioms
| Name | Condition |
|---|---|
| $T_0$ | for any two distinct points, some open set contains exactly one of them |
| $T_1$ | singletons are closed (each of two points has a neighbourhood missing the other) |
| $T_2$ (Hausdorff) | distinct points have disjoint neighbourhoods |
| Regular | a point and a closed set not containing it have disjoint neighbourhoods; $T_3$ = regular + $T_1$ |
| Completely regular | a point and a closed set are separated by a continuous function; $T_{3\frac12}$ (Tychonoff) = completely regular + $T_1$ |
| Normal | disjoint closed sets have disjoint neighbourhoods; $T_4$ = normal + $T_1$ |

Implications: $T_4\Rightarrow T_{3\frac12}\Rightarrow T_3\Rightarrow T_2\Rightarrow T_1\Rightarrow T_0$. All are strict.

**Separating examples**
| Example | Shows |
|---|---|
| Sierpiński space | $T_0$, not $T_1$ |
| cofinite topology (infinite set); line with two origins | $T_1$, not $T_2$ |
| $\mathbb R_K$ | $T_2$, not regular |
| Sorgenfrey plane $\mathbb R_l^2$; Moore (Niemytzki) plane | Tychonoff, not normal |
| Deleted Tychonoff plank | Tychonoff, not normal; also shows normality is not hereditary |
| Indiscrete space ($\ge2$ points) | (vacuously) regular and normal but not $T_0$; this is why $T_1$ is included in $T_3$ and $T_4$ |

**Sufficient conditions for normality**
- metric spaces
- compact Hausdorff spaces
- regular Lindelöf spaces (in particular, regular $C_2$ spaces)
- well-ordered sets with the order topology; linearly ordered spaces
- closed subspaces of normal spaces

**Permanence**
- Hausdorff, regular and completely regular: hereditary and productive.
- Normal: **neither** hereditary (except to closed subspaces) **nor** productive ($\mathbb R_l$ is normal, $\mathbb R_l^2$ is not).
- Finite $T_1$ spaces are discrete.
- Compact + Hausdorff $\Rightarrow$ normal. Locally compact Hausdorff $\Rightarrow$ Tychonoff.

## 3. Urysohn's lemma
> $X$ is normal $\iff$ for all disjoint closed $A,B$ there is a continuous $f:X\to[0,1]$ with $f|_A\equiv0$ and $f|_B\equiv1$.

- The proof uses dyadic rationals $r$ and open sets $U_r$ with $\overline{U_r}\subseteq U_s$ for $r<s$.
- **Tietze extension theorem:** $X$ is normal $\iff$ every continuous $f:A\to[0,1]$ (or $\to\mathbb R$) on a closed set $A$ extends continuously to $X$.
- In metric spaces Urysohn is easy: $f(x)=\dfrac{d(x,A)}{d(x,A)+d(x,B)}$.

## 4. Urysohn metrization theorem
> Every **regular $T_1$ second countable** space is metrizable. Equivalently, it embeds in the Hilbert cube $[0,1]^{\mathbb N}$ (equivalently in $\mathbb R^\omega$).

- Proof sketch: regular + $C_2$ $\Rightarrow$ normal (Tychonoff's lemma: regular Lindelöf is normal). Countably many Urysohn functions $f_n$ separate points from closed sets, and $x\mapsto(f_n(x)/n)$ is an embedding into $\mathbb R^\omega$.
- "Regular" **cannot** be weakened to Hausdorff: $\mathbb R_K$ is $T_2$ and $C_2$ but not metrizable.
- $C_2$ is sufficient but not necessary (uncountable discrete spaces are metrizable). The general characterisations are **Nagata–Smirnov** (regular + $\sigma$-locally finite basis) and **Bing** ($\sigma$-discrete basis).
- **Compact Hausdorff:** metrizable $\iff$ $C_2$.
- Manifolds (Hausdorff, $C_2$, locally Euclidean) are metrizable.

## Exam traps
- Separable $\not\Rightarrow C_2$ in general ($\mathbb R_l$), but it does in **metric** spaces. This is the standard non-metrizability argument for $\mathbb R_l$.
- Urysohn's lemma is about **normal** spaces; the metrization theorem needs **regular + $C_2$ + $T_1$**.
- A Hausdorff $C_2$ space need not be metrizable ($\mathbb R_K$).
- Compact Hausdorff does not imply metrizable ($[0,1]^{\mathbb R}$, which is not first countable).
- Normality is not hereditary and not productive (Sorgenfrey plane).
- Uncountable discrete space: metrizable but not $C_2$, separable or Lindelöf.
- 3-point set: 29 topologies, of which 19 are $T_0$, and only 1 is $T_1$ (the discrete one).
