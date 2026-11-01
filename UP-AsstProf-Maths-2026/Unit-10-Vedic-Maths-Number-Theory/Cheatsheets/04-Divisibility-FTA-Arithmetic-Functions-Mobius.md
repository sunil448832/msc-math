# Cheatsheet · Unit 10 · Topic 04 — Divisibility, FTA, Arithmetical Functions, Möbius Inversion
> Questions: [../Questions/04-Divisibility-FTA-Arithmetic-Functions-Mobius.md](../Questions/04-Divisibility-FTA-Arithmetic-Functions-Mobius.md)

## 1. Divisibility, gcd and lcm
- **Division algorithm:** for $a\in\mathbb Z$ and $b>0$ there are unique $q, r$ with $a=bq+r$ and $0\le r<b$.
- **Bézout:** $\gcd(a,b)=ax+by$ for some $x,y\in\mathbb Z$. In fact $\gcd(a,b)$ is the least positive element of $\{ax+by\}$.
- **Euclidean algorithm:** $\gcd(a,b)=\gcd(b,a\bmod b)$. Example: $\gcd(1071,462)=21$.
- $\gcd(a,b)\cdot\operatorname{lcm}(a,b)=ab$ for $a,b>0$. This fails for three numbers: $\gcd(a,b,c)\operatorname{lcm}(a,b,c)\ne abc$ in general.
- **Euclid's lemma:** if $p$ is prime and $p\mid ab$, then $p\mid a$ or $p\mid b$. More generally, if $a\mid bc$ and $\gcd(a,b)=1$, then $a\mid c$.
- $\gcd(2^m-1,2^n-1)=2^{\gcd(m,n)}-1$ and $\gcd(F_m,F_n)=F_{\gcd(m,n)}$ (Fibonacci).
- The number of ordered pairs with $\operatorname{lcm}(a,b)=n$ is $d(n^2)$. The number of pairs with $\gcd=1$ and $ab=n$ is $2^{\omega(n)}$.

## 2. Fundamental theorem of arithmetic
Every $n>1$ factors as $n=p_1^{a_1}\cdots p_k^{a_k}$, and this factorisation is **unique** up to order.
- Existence follows by induction. Uniqueness follows from Euclid's lemma.
- **It fails in** $\mathbb Z[\sqrt{-5}]$ ($6=2\cdot3=(1\pm\sqrt{-5})$), and in the even integers $2\mathbb Z$ ($60=6\cdot10=2\cdot30$).
- Euclid: there are infinitely many primes. $\sum 1/p$ diverges (Euler).
- **PNT:** $\pi(x)\sim x/\ln x$.

## 3. Arithmetical functions
For $n=\prod p_i^{a_i}$:
| Function | Definition | Formula | Multiplicative? |
|---|---|---|---|
| $d(n)=\tau(n)$ | number of divisors | $\prod(a_i+1)$ | yes (not completely) |
| $\sigma(n)$ | sum of divisors | $\prod\dfrac{p_i^{a_i+1}-1}{p_i-1}$ | yes |
| $\sigma_k(n)$ | $\sum_{d\mid n}d^k$ | $\prod\frac{p^{k(a+1)}-1}{p^k-1}$ | yes |
| $\varphi(n)$ | $\#\{1\le k\le n:\gcd(k,n)=1\}$ | $n\prod_{p\mid n}(1-\frac1p)$ | yes |
| $\mu(n)$ | $1$ if $n=1$; $(-1)^k$ if $n$ is square-free with $k$ primes; $0$ otherwise | — | yes |
| $\omega(n)$, $\Omega(n)$ | distinct / total prime factors | $k$, $\sum a_i$ | additive / completely additive |
| $\lambda(n)$ (Liouville) | $(-1)^{\Omega(n)}$ | — | completely multiplicative |
| $\Lambda(n)$ (von Mangoldt) | $\ln p$ if $n=p^k$, else 0 | $\sum_{d\mid n}\Lambda(d)=\ln n$ | neither |
| $J_k(n)$ (Jordan) | $n^k\prod(1-p^{-k})$ | $\sum_{d\mid n}J_k(d)=n^k$ | yes |

- **Multiplicative** means $f(mn)=f(m)f(n)$ whenever $\gcd(m,n)=1$, with $f(1)=1$. **Completely multiplicative** means this holds for all $m,n$. Examples of completely multiplicative functions: $\mathbf1$, $\mathrm{Id}$, $\lambda$, Dirichlet characters.
- A multiplicative function is determined by its values on prime powers.

**Standard values**
- $d(360)=24$, $\sigma(360)=1170$, $\varphi(360)=96$.
- $d(10!)=270$.
- $\varphi(p^k)=p^{k}-p^{k-1}$.

**Facts about $\varphi$**
- $\varphi(n)$ is even for $n\ge3$.
- $\varphi(n)=n-1$ iff $n$ is prime.
- $\varphi(2n)=\varphi(n)$ iff $n$ is odd.
- $\varphi(n)=n/2$ iff $n=2^k$ ($k\ge1$).
- $\varphi(mn)=\varphi(m)\varphi(n)\frac{d}{\varphi(d)}$ with $d=\gcd(m,n)$.
- The sum of the integers $\le n$ that are coprime to $n$ is $n\varphi(n)/2$ (for $n>1$).
- $\varphi(n)=12$ has 6 solutions: $13,21,26,28,36,42$.
- $\varphi(n)=14$ has none, so 14 is a non-totient. Odd numbers $>1$ are never values of $\varphi$.

**Facts about $d$ and $\sigma$**
- $d(n)$ is odd iff $n$ is a square.
- $\sigma(n)$ is odd iff $n$ is a square or twice a square.
- $\prod_{d\mid n}d = n^{d(n)/2}$.

## 4. Dirichlet convolution and Möbius inversion
- **Convolution:** $(f*g)(n)=\sum_{d\mid n}f(d)g(n/d)$.
- Convolution is commutative and associative with identity $\varepsilon(n)=[n=1]$.
- $f$ has an inverse iff $f(1)\ne0$.
- If $f$ and $g$ are multiplicative, so is $f*g$.

**Key identities**
$$\mu*\mathbf1=\varepsilon,\qquad \mathbf1*\mathbf1=d,\qquad \mathrm{Id}*\mathbf1=\sigma,\qquad \varphi*\mathbf1=\mathrm{Id},\qquad \mu*\mathrm{Id}=\varphi,\qquad \Lambda*\mathbf1=\ln,\qquad \lambda*\mathbf1=[n=\square].$$

**Möbius inversion.**
$$F(n)=\sum_{d\mid n}f(d)\ \ \forall n \iff f(n)=\sum_{d\mid n}\mu(d)F(n/d)\ \ \forall n.$$
- Consequences: $\dfrac{\varphi(n)}{n}=\sum_{d\mid n}\dfrac{\mu(d)}{d}$ and $\mu*d=\mathbf1$.
- **Multiplicative form:** if $F(n)=\prod_{d\mid n}f(d)$, then $f(n)=\prod_{d\mid n}F(n/d)^{\mu(d)}$.
- $\sum_{d\mid n}|\mu(d)| = 2^{\omega(n)}$ and $\sum_{d\mid n}\mu(d)d(d)=(-1)^{\omega(n)}$.

**Mertens function.** $M(x)=\sum_{n\le x}\mu(n)$: $M(10)=-1$, $M(20)=-3$.

**Square-free numbers.** The count of square-free $n\le x$ is $\sum_{d\le\sqrt x}\mu(d)\lfloor x/d^2\rfloor$. For $x=100$ it is 61, and in general it is $\sim\frac{6}{\pi^2}x$.

## 5. Perfect numbers
- $n$ is **perfect** if $\sigma(n)=2n$: $6, 28, 496, 8128, \dots$ Equivalently $\sum_{d\mid n}1/d=2$.
- **Euclid–Euler:** an even $n$ is perfect iff $n=2^{p-1}(2^p-1)$ with $2^p-1$ a (Mersenne) prime.
- If $2^p-1$ is prime then $p$ is prime. The **converse is false**: $2^{11}-1=2047=23\cdot89$.
- No odd perfect number is known (open problem).
- Abundant: $\sigma(n)>2n$ (12 is the smallest). Deficient: $\sigma(n)<2n$. Amicable pair: $(220,284)$.

## 6. Floor function and Legendre's formula
- $\lfloor x\rfloor$ facts: $\lfloor x+n\rfloor=\lfloor x\rfloor+n$; $\lfloor\lfloor x\rfloor/n\rfloor=\lfloor x/n\rfloor$; $\lfloor 2x\rfloor\ge2\lfloor x\rfloor$.
- **Legendre's formula:**
$$v_p(n!)=\sum_{k\ge1}\left\lfloor\frac{n}{p^k}\right\rfloor=\frac{n-s_p(n)}{p-1},$$
  where $s_p(n)$ is the sum of the base-$p$ digits of $n$.
- Examples: $v_2(100!)=97$, $v_5(100!)=24$, $v_3(50!)=22$.
- Trailing zeros of $n!$ are $v_5(n!)$: 24 for $100!$ and 249 for $1000!$.
- $\binom{2n}{n}$ is divisible by every prime in $(n,2n]$. The product of $k$ consecutive integers is divisible by $k!$.
- **Kummer:** $v_p\binom{m+n}{m}$ equals the number of carries when adding $m$ and $n$ in base $p$.
- $\sum_{k\le n}d(k)=\sum_{k\le n}\lfloor n/k\rfloor$. For $n=10$ this is 27.

## 7. Exam traps
- $\mu(1)=1$, not 0. $\mu(n)=0$ as soon as $p^2\mid n$.
- $\varphi$, $d$, $\sigma$ and $\mu$ are multiplicative but **not completely** multiplicative.
- $\varphi(1)=1$ (and $\varphi(2)=1$).
- In Legendre's formula, **keep adding** the terms for $p^2, p^3, \dots$. The trailing zeros of $1000!$ are $249$, not $200$.
- The count of pairs with lcm $=n$ is $d(n^2)$, not $d(n)^2$.
- $2^p-1$ need not be prime for prime $p$.
- $\gcd\cdot\operatorname{lcm}=$ product holds only for **two** numbers.
