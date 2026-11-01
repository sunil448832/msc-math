# Cheatsheet · Unit 1 · Topic 04 — UFD, PID, Euclidean Domain, Polynomial Rings
> Questions: [../Questions/04-UFD-PID-Euclidean-Polynomial-Rings.md](../Questions/04-UFD-PID-Euclidean-Polynomial-Rings.md)

## 1. Divisibility in an integral domain $D$
- $a\mid b$ iff $\langle b\rangle\subseteq\langle a\rangle$. **Associates** ($a\sim b$): $a=ub$ with $u$ a unit, iff $\langle a\rangle=\langle b\rangle$.
- **Irreducible:** a non-zero non-unit with $a=bc\Rightarrow b$ or $c$ a unit.
- **Prime:** a non-zero non-unit with $p\mid ab\Rightarrow p\mid a$ or $p\mid b$, i.e. $\langle p\rangle$ is a prime ideal.
- In an ID, **prime implies irreducible** always. **Irreducible implies prime holds in a UFD** but not in general.
- In a PID, $p$ irreducible $\iff$ $\langle p\rangle$ maximal $\iff$ $\langle p\rangle$ prime.

## 2. The hierarchy
$$\text{Field}\subset\text{ED}\subset\text{PID}\subset\text{UFD}\subset\text{ID}$$
All inclusions are strict:

| Ring | Field | ED | PID | UFD |
|---|---|---|---|---|
| $\mathbb{Q},\mathbb{R},\mathbb{C},\mathbb{Z}_p$ | ✓ | ✓ | ✓ | ✓ |
| $\mathbb{Z}$, $F[x]$, $\mathbb{Z}[i]$, $\mathbb{Z}[\omega]$, $\mathbb{Z}[\sqrt{-2}]$, $\mathbb{Z}[\sqrt2]$ | ✗ | ✓ | ✓ | ✓ |
| $\mathbb{Z}[\tfrac{1+\sqrt{-19}}2]$ | ✗ | ✗ | ✓ | ✓ |
| $\mathbb{Z}[x]$, $F[x,y]$, $\mathbb{Z}[x_1,\dots]$ | ✗ | ✗ | ✗ | ✓ |
| $\mathbb{Z}[\sqrt{-5}]$, $\mathbb{Z}[\sqrt{-3}]$, $\mathbb{Z}[2i]$, $F[x^2,x^3]$ | ✗ | ✗ | ✗ | ✗ |

- **ED:** there is a $\delta:D\setminus\{0\}\to\mathbb{Z}_{\ge0}$ with division with remainder: $a=bq+r$ where $r=0$ or $\delta(r)<\delta(b)$. Examples of $\delta$: $|n|$ on $\mathbb{Z}$, $\deg$ on $F[x]$, the norm $a^2+b^2$ on $\mathbb{Z}[i]$.
- **PID implies UFD.** In a PID every non-zero prime ideal is maximal, and $\gcd(a,b)$ exists and equals $ra+sb$ (Bézout).
- **UFD:** existence and uniqueness (up to order and associates) of factorization into irreducibles. Equivalently: ACCP holds and irreducible = prime. gcds exist in a UFD but need not be $R$-linear combinations ($\gcd(2,x)=1$ in $\mathbb{Z}[x]$, yet $1\notin\langle 2,x\rangle$).
- **Gauss's theorem:** if $D$ is a UFD then $D[x]$ is a UFD, and hence so is $D[x_1,\dots,x_n]$.
- **$D[x]$ is a PID $\iff$ $D$ is a field** (and then it is an ED).
- Norm-Euclidean imaginary quadratic: $\mathbb{Z}[\sqrt{-d}]$ or $\mathcal{O}$ for $d=1,2,3,7,11$. Imaginary quadratic rings of integers that are PIDs: $d=1,2,3,7,11,19,43,67,163$.

## 3. Quadratic integer rings, norm $N(a+b\sqrt{d})=a^2-db^2$
- $N$ is multiplicative, and $u$ is a unit iff $N(u)=\pm1$.
- Units: $\mathbb{Z}[i]$ has 4 ($\pm1,\pm i$). $\mathbb{Z}[\omega]$ has 6. $\mathbb{Z}[\sqrt{-d}]$ with $d\ge2$ has 2 ($\pm1$). Real quadratic rings ($d>1$) have **infinitely many** (Pell), e.g. $1+\sqrt2$.
- To show $\alpha$ is irreducible, show that no element has norm equal to a proper factor of $N(\alpha)$. E.g. in $\mathbb{Z}[\sqrt{-5}]$, $a^2+5b^2=2$ or $3$ has no solution, so $2$, $3$ and $1\pm\sqrt{-5}$ are irreducible but not prime: $6=2\cdot3=(1+\sqrt{-5})(1-\sqrt{-5})$.
- **Gaussian primes:** $1+i$ (above 2); $a\pm bi$ where $a^2+b^2=p\equiv1\pmod4$; and $p$ itself when $p\equiv3\pmod 4$.
- $|\mathbb{Z}[i]/\langle\alpha\rangle|=N(\alpha)$. $\mathbb{Z}[i]/\langle p\rangle\cong\mathbb{F}_{p^2}$ iff $p\equiv3 \pmod 4$.
- **Fermat (two squares):** an odd prime $p=a^2+b^2$ iff $p\equiv1\pmod4$.

## 4. Polynomial rings
- **Division algorithm** in $F[x]$, or in $R[x]$ when the divisor is monic. **Remainder theorem:** $f(a)$ is the remainder mod $x-a$.
- **Number of roots:** over an ID, a polynomial of degree $n$ has $\le n$ roots. This fails otherwise: $x^2-1$ has 4 roots in $\mathbb{Z}_8$, and $x^2+1$ has infinitely many roots in $\mathbb{H}$.
- For an ID $D$: $\deg(fg)=\deg f+\deg g$ and $U(D[x])=U(D)$.
- In $F[x]$: $f$ irreducible $\iff\langle f\rangle$ maximal $\iff F[x]/\langle f\rangle$ is a field.

## 5. Irreducibility tests
| Test | Statement |
|---|---|
| Degree 2 or 3 | Over a field, reducible $\iff$ there is a root in $F$ |
| Rational root | A root $p/q$ in lowest terms of $a_nx^n+\dots+a_0\in\mathbb{Z}[x]$ has $p\mid a_0$ and $q\mid a_n$ |
| Gauss's lemma | A primitive $f\in\mathbb{Z}[x]$ is irreducible in $\mathbb{Z}[x]\iff$ it is irreducible in $\mathbb{Q}[x]$. Products of primitives are primitive |
| **Eisenstein** | $f=\sum a_ix^i\in\mathbb{Z}[x]$ and a prime $p$ with $p\nmid a_n$, $p\mid a_i$ for $i<n$, $p^2\nmid a_0$. Then $f$ is irreducible over $\mathbb{Q}$ |
| Shift | $f(x)$ is irreducible $\iff f(x+c)$ is irreducible. E.g. $\Phi_p(x+1)$ is Eisenstein at $p$ |
| Mod $p$ | If $p\nmid a_n$ and $\bar f$ is irreducible over $\mathbb{Z}_p$ with the same degree, then $f$ is irreducible over $\mathbb{Q}$. The converse fails: $x^4+1$ |
| Reciprocal | $f$ is irreducible $\iff x^nf(1/x)$ is irreducible (when $a_0\neq0$) |

Standard facts: $x^n-p$ is irreducible over $\mathbb{Q}$ for all $n$ (Eisenstein), so $\mathbb{Q}$ has irreducibles of every degree. $x^4+4=(x^2+2x+2)(x^2-2x+2)$. $x^4+1$ is irreducible over $\mathbb{Q}$ but reducible over every $\mathbb{Z}_p$. Over $\mathbb{R}$, irreducibles have degree 1 or 2. Over $\mathbb{C}$, they have degree 1.

## Exam traps
- **Irreducible in $\mathbb{Z}[x]$ requires primitive.** $2x+4$ is reducible in $\mathbb{Z}[x]$ but irreducible in $\mathbb{Q}[x]$. And $2$ is irreducible in $\mathbb{Z}[x]$ but a unit in $\mathbb{Q}[x]$.
- "No rational roots implies irreducible" holds **only for degree $\le3$**. $(x^2+1)^2$ has no roots but is reducible.
- Eisenstein is sufficient, not necessary: $x^2+1$ fails Eisenstein for every $p$ but is irreducible.
- UFD does not imply PID ($\mathbb{Z}[x]$, $F[x,y]$). PID does not imply ED ($\mathbb{Z}[\frac{1+\sqrt{-19}}2]$, not $\mathbb{Z}[\sqrt{-19}]$, which is not even a UFD).
- In $\mathbb{Z}[\sqrt{-5}]$ factorizations exist but are not unique. A "not a UFD" proof needs irreducibility via norms, not just two factorizations.
- Real quadratic rings have infinitely many units.
