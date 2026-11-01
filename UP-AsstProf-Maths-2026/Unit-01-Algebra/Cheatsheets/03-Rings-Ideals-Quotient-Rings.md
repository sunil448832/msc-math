# Cheatsheet · Unit 1 · Topic 03 — Rings, Ideals, Quotient Rings
> Questions: [../Questions/03-Rings-Ideals-Quotient-Rings.md](../Questions/03-Rings-Ideals-Quotient-Rings.md)

## 1. Basic definitions
- **Ring** $(R,+,\cdot)$: an abelian group under $+$, with associative multiplication that distributes over $+$. The terms *commutative* and *with unity* are added when they hold.
- **Zero divisor:** $a\ne0$ with $ab=0$ for some $b\ne0$. **Integral domain (ID):** a commutative ring with $1\ne0$ and no zero divisors. **Field:** a commutative ring with $1\ne 0$ in which every non-zero element is a unit.
- **Unit:** $a$ with $ab=1$. **Nilpotent:** $a^n=0$. **Idempotent:** $e^2=e$.
- **Characteristic:** the least $n>0$ with $n\cdot1=0$, or $0$ if there is none. For an ID it is $0$ or a prime. $\operatorname{char}(R\times S)=\operatorname{lcm}$ of the two characteristics.
- A finite ID is a field. In a finite commutative ring with 1, every element is a unit or a zero divisor (or 0).
- Field $\subset$ ID, and the inclusion is strict: $\mathbb{Z}$ is an ID but not a field.

## 2. $\mathbb{Z}_n$ counts ($n=\prod p_i^{a_i}$, $\omega(n)$ = number of distinct primes)
| Quantity | Formula | Example $n=72$ |
|---|---|---|
| Units | $\varphi(n)$ | 24 |
| Non-zero zero divisors | $n-1-\varphi(n)$ | 47 |
| Nilpotents | $n/\operatorname{rad}(n)$ (the multiples of $\prod p_i$) | 12 |
| Idempotents | $2^{\omega(n)}$ | 4 |
| Ideals | $d(n)$, all of the form $\langle d\rangle$ with $d\mid n$ | 12 |
| Maximal ideals | $\omega(n)$, namely $\langle p_i\rangle$. Prime ideals are the same as maximal ones | 2 |
| Ring homs $\mathbb{Z}_m\to\mathbb{Z}_n$ | number of $e\in\mathbb{Z}_n$ with $e^2=e$ and $me=0$ | |
| Unital ring homs $\mathbb{Z}_m\to\mathbb{Z}_n$ | 1 if $n\mid m$, else 0 | |

$\mathbb{Z}_n$ is a field $\iff$ an ID $\iff$ $n$ is prime. $\mathbb{Z}_n$ is reduced (no non-zero nilpotents) iff $n$ is squarefree.

## 3. Ideals
- $I\subseteq R$ is an **ideal** if it is an additive subgroup and $rI\subseteq I\supseteq Ir$. If it contains a unit then $I=R$.
- Sums, intersections and products of ideals are ideals. A union generally is not.
- A commutative ring with 1 is a field iff its only ideals are $0$ and $R$.
- Ideals of $\mathbb{Z}$ are the $n\mathbb{Z}$. $\gcd$ corresponds to the sum: $m\mathbb{Z}+n\mathbb{Z}=\gcd(m,n)\mathbb{Z}$. $\operatorname{lcm}$ corresponds to the intersection: $m\mathbb{Z}\cap n\mathbb{Z}=\operatorname{lcm}(m,n)\mathbb{Z}$. And $m\mathbb{Z}\cdot n\mathbb{Z}=mn\mathbb{Z}$.
- $M_n(F)$ is a simple ring: it has no two-sided ideals except $0$ and $M_n(F)$.

## 4. Prime and maximal ideals (commutative ring $R$ with 1)
| Ideal $P$ | Definition | Quotient test |
|---|---|---|
| Prime | $P\neq R$ and $ab\in P\Rightarrow a\in P$ or $b\in P$ | $R/P$ is an ID |
| Maximal | $P\ne R$, no ideal strictly between $P$ and $R$ | $R/P$ is a field |

- Maximal implies prime. Prime does not imply maximal: $\langle x\rangle\subset\langle 2,x\rangle$ in $\mathbb{Z}[x]$, and $\{0\}$ in $\mathbb{Z}$.
- In a **PID**, non-zero prime implies maximal. In a **finite** commutative ring, prime is the same as maximal.
- Every proper ideal is contained in a maximal ideal (Zorn), so every non-zero ring with 1 has a maximal ideal.
- **Nilradical** $=\{\text{nilpotents}\}=\bigcap(\text{prime ideals})$. **Jacobson radical** $=\bigcap(\text{maximal ideals})$, and it contains the nilradical.
- Maximal ideals of $C[0,1]$ are $M_c=\{f:f(c)=0\}$, with $C[0,1]/M_c\cong\mathbb{R}$.
- Prime ideals of $\mathbb{Z}[x]$: $0$; $\langle p\rangle$; $\langle f\rangle$ with $f$ irreducible primitive; and the maximal ones $\langle p,f\rangle$ with $f$ irreducible mod $p$.
- Ideals of $F[x]$ are $\langle f\rangle$. $\langle f\rangle$ is maximal iff it is prime iff $f$ is irreducible.

## 5. Quotient rings and homomorphisms
- $R/I=\{a+I\}$, with $(a+I)(b+I)=ab+I$.
- **First isomorphism theorem:** for an onto $\phi:R\to S$, $R/\ker\phi\cong S$. Kernels are exactly the ideals.
- **Correspondence:** ideals of $R/I$ correspond to ideals of $R$ containing $I$, and prime/maximal ideals correspond likewise.
- **Chinese Remainder Theorem:** for comaximal $I,J$ (i.e. $I+J=R$), $R/(I\cap J)\cong R/I\times R/J$. Hence $\mathbb{Z}_{mn}\cong\mathbb{Z}_m\times\mathbb{Z}_n$ when $\gcd(m,n)=1$.
- Standard quotients:

| Quotient | Isomorphic to |
|---|---|
| $\mathbb{Z}[x]/\langle x\rangle$ | $\mathbb{Z}$ (ID, not a field) |
| $\mathbb{Z}[x]/\langle 2,x\rangle$ | $\mathbb{Z}_2$ |
| $\mathbb{Z}[x]/\langle x^2+1\rangle$ | $\mathbb{Z}[i]$ |
| $\mathbb{Z}[x]/\langle n\rangle$ | $\mathbb{Z}_n[x]$ |
| $\mathbb{R}[x]/\langle x^2+1\rangle$ | $\mathbb{C}$ |
| $\mathbb{R}[x]/\langle x^2-1\rangle$ | $\mathbb{R}\times\mathbb{R}$ |
| $\mathbb{R}[x]/\langle x^2\rangle$ | dual numbers (one non-zero nilpotent direction) |
| $F[x]/\langle f\rangle$, $\deg f=n$ | an $n$-dim $F$-algebra; a field iff $f$ is irreducible |
| $\mathbb{Z}[i]/\langle a+bi\rangle$ | ring of order $a^2+b^2$ |
| $\mathbb{Z}[i]/\langle 1+i\rangle$ | $\mathbb{Z}_2$ |
| $\mathbb{Z}[i]/\langle 3\rangle$ | $\mathbb{F}_9$ |

## 6. Units and nilpotents (general)
- If $a$ is nilpotent then $1+a$ is a unit, with $(1+a)^{-1}=1-a+a^2-\cdots$.
- In a commutative ring, the nilpotents form an ideal, and unit + nilpotent is a unit.
- $U(R\times S)=U(R)\times U(S)$.
- $f=a_0+a_1x+\cdots\in R[x]$ ($R$ commutative) is a unit iff $a_0$ is a unit and $a_1,\dots,a_n$ are nilpotent. E.g. $1+2x$ is a unit in $\mathbb{Z}_4[x]$.
- For an ID $D$: $U(D[x])=U(D)$ and $\deg(fg)=\deg f+\deg g$.

## Exam traps
- **"Every subring is an ideal"** is false ($\mathbb{Z}\subset\mathbb{Q}$). "Every ideal is a subring" depends on whether subrings are required to contain 1.
- **$\{0\}$ is prime in any ID but maximal only in a field.**
- Irreducibility of $x^2+x+1$ depends on the field. Over $\mathbb{Z}_3$ it equals $(x-1)^2$, so the quotient has nilpotents.
- Ring homs from $\mathbb{Z}_m$: count the *idempotents* $e$ with $me=0$, not $\gcd(m,n)$.
- Characteristic of a product is the lcm, not the sum or product.
- $\mathbb{Z}\times\mathbb{Z}$ is not an ID, since $(1,0)(0,1)=0$. $\{0\}\times\mathbb{Z}$ is a prime ideal of it.
- A nilpotent in a non-commutative ring: in $M_2(\mathbb{R})$, $\begin{pmatrix}0&1\\0&0\end{pmatrix}$. There the nilpotents do **not** form an ideal.
