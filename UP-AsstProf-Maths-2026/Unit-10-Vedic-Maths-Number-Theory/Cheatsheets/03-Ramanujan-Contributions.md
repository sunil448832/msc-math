# Cheatsheet · Unit 10 · Topic 03 — Contribution of Ramanujan in Number Theory
> Questions: [../Questions/03-Ramanujan-Contributions.md](../Questions/03-Ramanujan-Contributions.md)

## 1. Life facts
| Event | Fact |
|---|---|
| Born | **22 December 1887**, **Erode** (Tamil Nadu). Grew up in **Kumbakonam**. |
| Early influence | G. S. Carr's *Synopsis of Elementary Results in Pure Mathematics* |
| Job | Clerk at the Madras Port Trust (1912) |
| First published paper | On Bernoulli numbers, *Journal of the Indian Mathematical Society* (1911) |
| Letter to G. H. Hardy | January 1913, containing about 120 theorems |
| Cambridge | Arrived in **1914**, **Trinity College**; worked with Hardy and Littlewood |
| Degree | B.A. by research, 1916 (work on **highly composite numbers**) |
| Honours | **FRS 1918** (one of the youngest) and **Fellow of Trinity 1918** (the first Indian) |
| Returned to India | 1919 |
| Died | **26 April 1920**, Kumbakonam, aged 32 |
| Notebooks | 3 notebooks plus the **"lost notebook"**, found by **George Andrews** in 1976 (Trinity library) |
| Commemoration | **22 December = National Mathematics Day** (declared Dec 2011). 2012 = National Mathematical Year. SASTRA Ramanujan Prize. ICTP Ramanujan Prize. |
| Biography and film | *The Man Who Knew Infinity* (Robert Kanigel, 1991; film 2015) |

## 2. Partitions
- $p(n)$ is the number of ways to write $n$ as an unordered sum of positive integers.
- Values: $p(0..12) = 1,1,2,3,5,7,11,15,22,30,42,56,77$; $p(100) = 190569292$.
- Generating function (Euler): $\sum p(n)q^n = \prod_{n\ge1}(1-q^n)^{-1}$.
- **Ramanujan's congruences** (1919):
$$p(5n+4)\equiv0\ (\mathrm{mod}\ 5),\qquad p(7n+5)\equiv0\ (\mathrm{mod}\ 7),\qquad p(11n+6)\equiv0\ (\mathrm{mod}\ 11).$$
  Note the pattern $24\cdot r\equiv1\pmod\ell$: $24\cdot4\equiv1\ (5)$, $24\cdot5\equiv1\ (7)$, $24\cdot6\equiv1\ (11)$.
- Identity behind the mod-5 case: $\sum p(5n+4)q^n = 5\dfrac{(q^5;q^5)_\infty^5}{(q;q)_\infty^6}$ ("the most beautiful", per Hardy).
- **Dyson's rank** (1944) explains the mod 5 and mod 7 congruences combinatorially. The **crank** (Andrews–Garvan, 1988) explains all three.
- **Hardy–Ramanujan asymptotic** (1918):
$$p(n)\sim\frac{1}{4n\sqrt3}\exp\left(\pi\sqrt{\tfrac{2n}{3}}\right).$$
  This came from the **circle method**. Rademacher (1937) turned it into an exact convergent series.

## 3. Rogers–Ramanujan identities
$$G(q)=\sum_{n\ge0}\frac{q^{n^2}}{(q;q)_n}=\prod_{n\ge0}\frac{1}{(1-q^{5n+1})(1-q^{5n+4})},\qquad H(q)=\sum_{n\ge0}\frac{q^{n^2+n}}{(q;q)_n}=\prod_{n\ge0}\frac{1}{(1-q^{5n+2})(1-q^{5n+3})}.$$
- First identity: partitions into parts differing by $\ge2$ are equinumerous with partitions into parts $\equiv\pm1\pmod5$.
- Second identity: partitions into parts differing by $\ge2$ **and all parts $\ge2$** are equinumerous with partitions into parts $\equiv\pm2\pmod5$.
- They were first proved by L. J. Rogers (1894) and rediscovered by Ramanujan (around 1913). The Rogers–Ramanujan continued fraction is $R(q)=q^{1/5}H(q)/G(q)$.

## 4. Ramanujan's tau function
$$\Delta(z)=q\prod_{n\ge1}(1-q^n)^{24}=\sum_{n\ge1}\tau(n)q^n,\quad q=e^{2\pi i z}.$$
- Values: $\tau(1)=1$, $\tau(2)=-24$, $\tau(3)=252$, $\tau(4)=-1472$, $\tau(5)=4830$, $\tau(6)=-6048$, $\tau(7)=-16744$.
- **Ramanujan's conjectures (1916):**
  1. $\tau$ is multiplicative: $\tau(mn)=\tau(m)\tau(n)$ for $\gcd(m,n)=1$. Proved by **Mordell 1917**.
  2. $\tau(p^{k+1})=\tau(p)\tau(p^k)-p^{11}\tau(p^{k-1})$. Proved by **Mordell 1917**.
  3. $|\tau(p)|\le 2p^{11/2}$. Proved by **Deligne 1974** as a consequence of the Weil conjectures.
- **Congruence:** $\tau(n)\equiv\sigma_{11}(n)\pmod{691}$.
- $\Delta$ is the unique normalised cusp form of weight 12 for $SL_2(\mathbb Z)$ and a Hecke eigenform. **Lehmer's conjecture**: $\tau(n)\neq0$ for all $n$ (still open).

## 5. Other number-theoretic contributions
| Topic | Statement |
|---|---|
| **1729 (Hardy–Ramanujan / taxicab number)** | $1729=1^3+12^3=9^3+10^3$, the smallest number that is a sum of two positive cubes in two ways. (It is also $7\cdot13\cdot19$, a Carmichael number, but not the smallest Carmichael number, which is 561.) |
| **Highly composite numbers** (1915) | $n$ with $d(m)<d(n)$ for all $m<n$: 1, 2, 4, 6, 12, 24, 36, 48, 60, 120, 180, 240, 360, 720, 840, … If $n=2^{a_2}3^{a_3}\cdots p^{a_p}$, then $a_2\ge a_3\ge\cdots$ and the last exponent is 1, except for $n=4, 36$. |
| **Hardy–Ramanujan theorem** (1917) | The normal order of $\omega(n)$ is $\log\log n$: almost all $n$ have about $\log\log n$ distinct prime factors. Precursor of Erdős–Kac. |
| **Ramanujan primes** (2009 name, from his 1919 proof of Bertrand's postulate) | $R_n$ is the least $x$ with $\pi(x)-\pi(x/2)\ge n$ for all $x\ge R_n$: $2, 11, 17, 29, 41, 47, \dots$ |
| **Ramanujan sum** (1918) | $c_q(n)=\sum_{(a,q)=1}e^{2\pi i an/q}=\sum_{d\mid(q,n)}\mu(q/d)d$. $c_q(1)=\mu(q)$, $c_q(0)=\varphi(q)$. Multiplicative in $q$. Used for expansions such as $\sigma(n)/n=\frac{\pi^2}{6}\sum_q c_q(n)/q^2$. |
| **Landau–Ramanujan constant** | The number of $n\le x$ that are sums of two squares is $\sim K\,\dfrac{x}{\sqrt{\ln x}}$ with $K\approx0.7642$. |
| **Ramanujan–Nagell equation** | $2^n-7=x^2$ has solutions only for $n=3,4,5,7,15$ (Nagell 1948). |
| **Mock theta functions** | Introduced in his last letter to Hardy (January 1920). Understood via harmonic Maass forms (Zwegers 2002). |
| **Series for $1/\pi$** (1914) | $\dfrac1\pi=\dfrac{2\sqrt2}{9801}\sum_{k\ge0}\dfrac{(4k)!\,(1103+26390k)}{(k!)^4\,396^{4k}}$, giving about 8 digits per term |
| **Ramanujan's ternary form** | $x^2+y^2+10z^2$ |
| **Ramanujan's master theorem**, **Ramanujan summation** | Regularised $1+2+3+\cdots \;\text{"="}\; -\tfrac1{12}$ (not a genuine sum) |
| **Ramanujan theta function** | $f(a,b)=\sum_{n\in\mathbb Z}a^{n(n+1)/2}b^{n(n-1)/2}$ |
| **Ramanujan graphs** (later name) | Expanders that meet the Ramanujan bound $\lambda\le2\sqrt{k-1}$ |

## 6. Exam traps
- Born in **Erode**, died in **Kumbakonam**. Do not mix up the birth date (22 Dec 1887) with the death date (26 Apr 1920).
- FRS and the Trinity Fellowship were **both in 1918**.
- Congruence pairs: (5, 4), (7, 5), (11, 6). They are not $p(5n+1)$ etc.
- $\tau$ is multiplicative but **not completely** multiplicative ($\tau(4)=-1472\ne\tau(2)^2=576$).
- The bound $|\tau(p)|\le 2p^{11/2}$ was proved by **Deligne**. Mordell proved multiplicativity.
- $72$ is **not** highly composite. $d(1729)=8$.
- 1729 is the smallest for two **positive cubes** in two ways (allowing negative cubes, 91 works: $91=6^3+(-5)^3=4^3+3^3$).
- The **Rogers–Ramanujan identities** were first proved by Rogers (1894). Ramanujan rediscovered them.
