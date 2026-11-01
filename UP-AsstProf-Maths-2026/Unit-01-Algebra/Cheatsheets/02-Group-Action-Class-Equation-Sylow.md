# Cheatsheet · Unit 1 · Topic 02 — Group Action, Class Equation, Sylow
> Questions: [../Questions/02-Group-Action-Class-Equation-Sylow.md](../Questions/02-Group-Action-Class-Equation-Sylow.md)

## 1. Group actions
A (left) action of $G$ on a set $X$ is a map $G\times X\to X$ with $e\cdot x=x$ and $g\cdot(h\cdot x)=(gh)\cdot x$. Equivalently, it is a homomorphism $G\to\operatorname{Sym}(X)$.
- **Orbit** $Gx=\lbrace gx\rbrace$ and **stabilizer** $G_x=\lbrace g:gx=x\rbrace \le G$. The orbits partition $X$.
- **Orbit–Stabilizer:** $|Gx|=[G:G_x]$, so orbit sizes divide $|G|$.
- Stabilizers of points in the same orbit are conjugate: $G_{gx}=gG_xg^{-1}$.
- **Faithful** means the kernel $\bigcap_x G_x$ is trivial. **Transitive** means there is one orbit.
- **Burnside's (Cauchy–Frobenius) lemma:** $\sharp \text{orbits}=\dfrac1{|G|}\sum_{g\in G}|\operatorname{Fix}(g)|$.
- **$p$-group fixed points:** if $|G|=p^n$ acts on a finite $X$, then $|X|\equiv|X^G|\pmod p$.
- Standard actions:

| Action | Orbits | Stabilizer | Consequence |
|---|---|---|---|
| Left multiplication on $G$ | one | trivial | Cayley's theorem |
| Left mult. on $G/H$ | one | $gHg^{-1}$ | $G\to S_{[G:H]}$, kernel $\operatorname{core}H$ |
| Conjugation on $G$ | conjugacy classes | centralizer $C(a)$ | class equation |
| Conjugation on subgroups | conjugates of $H$ | normalizer $N(H)$ | #conjugates $=[G:N(H)]$ |

## 2. Class equation
$$|G|=|Z(G)|+\sum_{a\in\text{reps of non-central classes}}[G:C(a)]$$
Each $[G:C(a)]\gt 1$ is a divisor of $|G|$.
- **$p$-groups:** $|G|=p^n$ with $n\ge1$ implies $Z(G)\ne1$. Groups of order $p^2$ are abelian. A non-abelian group of order $p^3$ has $|Z|=p$.
- **Classes in $S_n$** correspond to cycle types, i.e. partitions of $n$: $p(3)=3,\ p(4)=5,\ p(5)=7,\ p(6)=11$.
- Class size in $S_n$ for cycle type $1^{m_1}2^{m_2}\cdots$ is $\dfrac{n!}{\prod k^{m_k}m_k!}$.
- **Splitting in $A_n$:** an $S_n$-class contained in $A_n$ splits into two $A_n$-classes iff the cycle type consists of **distinct odd lengths**, e.g. 5-cycles in $A_5$, $(3,1)$ in $A_4$.
- Standard class equations:

| Group | Class equation |
|---|---|
| $S_3$ | $6=1+2+3$ |
| $D_4$ | $8=1+1+2+2+2$ |
| $Q_8$ | $8=1+1+2+2+2$ |
| $A_4$ | $12=1+3+4+4$ |
| $S_4$ | $24=1+3+6+6+8$ |
| $D_5$ | $10=1+2+2+5$ |
| $A_5$ | $60=1+15+20+12+12$ (simple: no union of classes containing $1$ has size dividing 60, except 1 and 60) |
| $S_5$ | $120=1+10+15+20+20+30+24$ |

- Number of conjugacy classes $k(G)$: for abelian $G$ it is $|G|$. For $D_n$ it is $(n+3)/2$ if $n$ is odd and $(n+6)/2$ if $n$ is even.

## 3. Cauchy and Sylow theorems
Let $|G|=p^a m$ with $p\nmid m$.
- **Cauchy:** if $p\mid|G|$ then $G$ has an element of order $p$.
- **Sylow I (existence):** Sylow $p$-subgroups (order $p^a$) exist. In fact, subgroups of order $p^k$ exist for every $k\le a$.
- **Sylow II (conjugacy):** all Sylow $p$-subgroups are conjugate. Every $p$-subgroup lies in some Sylow $p$-subgroup.
- **Sylow III (counting):** $n_p\equiv1\pmod p$ and $n_p\mid m$. Also $n_p=[G:N_G(P)]$.
- $n_p=1\iff P\trianglelefteq G$. A unique Sylow subgroup is characteristic.
- Subgroups of prime order $p$ meet trivially, so $n_p$ subgroups of order $p$ give $n_p(p-1)$ elements of order $p$.

## 4. Standard applications
| Order | Conclusion | Reason |
|---|---|---|
| $pq$, $p\lt q$, $p\nmid q-1$ | cyclic | $n_p=n_q=1$ (e.g. 15, 33, 35, 51, 65, 77, 85, 91) |
| $pq$, $p\mid q-1$ | $\mathbb Z_{pq}$ or one non-abelian group | e.g. 6, 10, 21, 39, 55 |
| $p^2q$ | not simple | counting |
| 12 | not simple. $n_3=1$ or $n_2=1$ | $A_4$ has $n_3=4$, $n_2=1$ |
| 30 | not simple, and has a normal (cyclic) subgroup of order 15 | $20+24\gt 30$ |
| 56 | not simple | $n_7=8$ uses 48 elements, which leaves room for only one Sylow 2-subgroup |
| 36 | not simple | $n_3\in\lbrace 1,4\rbrace$. $G\to S_4$ is not injective since $36\nmid24$ |
| 60 | $A_5$ is the unique simple group of this order | |
| 168 | simple group $PSL(2,7)$, $n_7=8$ | |

- **Burnside's $p^aq^b$ theorem:** such groups are solvable, hence not simple unless of prime order.
- Smallest non-abelian simple group is $A_5$ (order 60). There are no non-abelian simple groups of order $\lt 60$, and the next one has order 168.
- **Index trick:** if $[G:H]=n$ and $|G|\nmid n!$, then $G$ is not simple. If $p$ is the smallest prime divisor of $|G|$, then any subgroup of index $p$ is normal.
- Sylow numbers to know: $S_3$: $n_2=3,n_3=1$. $A_4$: $n_2=1,n_3=4$. $S_4$: $n_2=3,n_3=4$. $A_5$: $n_2=5,n_3=10,n_5=6$. $S_5$: $n_2=15,n_3=10,n_5=6$.

## Exam traps
- $n_p$ counts **subgroups**. The number of **elements** of order $p$ is $n_p(p-1)$, which only works for subgroups of prime order.
- $n_p\equiv1\pmod p$ AND $n_p\mid m$ (the $p'$-part), not $n_p\mid|G|$.
- In Burnside's lemma, divide by $|G|$ after summing the fixed points of every element, identity included.
- For classes in $A_n$, check the splitting criterion (distinct odd cycle lengths). Otherwise the class size is the same as in $S_n$.
- "Order $pq$ implies cyclic" needs $p\nmid q-1$: 21, 39, 55 are counterexamples.
- Groups of order $p^3$ can be non-abelian ($D_4$, $Q_8$ for $p=2$).
