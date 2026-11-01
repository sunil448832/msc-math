# Cheatsheet · Unit 10 · Topic 02 — Contributions of Ancient Indian Mathematicians
> Questions: [../Questions/02-Ancient-Indian-Mathematicians.md](../Questions/02-Ancient-Indian-Mathematicians.md)

All dates are approximate (the usual textbook values). "c." means circa.

## 1. Master table
| Mathematician | Date | Main work(s) | Key contributions |
|---|---|---|---|
| **Baudhayana** | c. 800–600 BCE | *Baudhayana Sulba Sutra* | Altar geometry. Statement equivalent to the **Pythagorean theorem** (the diagonal of a rectangle produces both areas). $\sqrt2\approx 1+\frac13+\frac1{3\cdot4}-\frac1{3\cdot4\cdot34}=\frac{577}{408}$. Squaring the circle (approximately). |
| Apastamba, Katyayana | later Sulba authors | Sulba Sutras | Further altar geometry |
| **Pingala** | c. 3rd–2nd c. BCE | *Chandahsutra* (prosody) | Enumeration of metres with short/long syllables (a **binary**-type representation). *Meru-prastara* (the Pascal triangle, made explicit by the commentator Halayudha, 10th c.). |
| Jaina mathematicians | BCE–early CE | *Surya Prajnapti* etc. | Classification of infinities, combinatorics |
| Bakhshali manuscript | early centuries CE | — | Uses a dot for zero. Square-root approximation formula. |
| **Aryabhata I** | b. **476 CE** (Kusumapura/Pataliputra) | ***Aryabhatiya*** (**499 CE**) | **$\pi\approx 62832/20000 = 3.1416$** (called "approximate", *asanna*). Table of **sine differences** (*jya*), step $3^\circ45'$, $R=3438$. ***Kuttaka*** for $ax+by=c$. Sums $\sum n,\ \sum n^2,\ \sum n^3$. Rotation of the Earth. Alphabetic numeral notation. |
| **Varahamihira** | c. 505–587 | ***Pancha-siddhantika***, *Brihat Samhita* | Summary of five astronomical siddhantas. Trigonometric relations between sine values. Combinatorial (Pascal-type) table. |
| **Bhaskara I** | c. 600–680 | *Mahabhaskariya*, *Laghubhaskariya*, *Aryabhatiyabhashya* (629) | **Rational sine approximation** $\sin x\approx \dfrac{16x(\pi-x)}{5\pi^2-4x(\pi-x)}$. Hindu numerals with zero in place-value notation. Commentary on Aryabhata. |
| **Brahmagupta** | **598–c. 668** | ***Brahmasphutasiddhanta*** (**628**), *Khandakhadyaka* (665) | **Rules for zero** and negative numbers. **Brahmagupta's identity / bhavana**. **Cyclic quadrilateral** area and diagonals. Pell-type equations ($92x^2+1=y^2$). Quadratic solution. Interpolation formula. |
| **Mahavira** | c. 9th c. (c. 850), Rashtrakuta court (Amoghavarsha) | ***Ganitasarasangraha*** | Formula for **${}^nC_r$**. Arithmetic, operations with zero. Ellipse perimeter approximation. Geometric series. |
| **Sridhara** | c. 8th–9th c. | *Patiganita*, *Trishatika* | **Rule for solving quadratics** (the "Sridharacharya formula"). Zero, fractions. |
| **Aryabhata II** | c. 10th c. | *Maha-siddhanta* | Kuttaka, astronomy |
| **Bhaskara II** (Bhaskaracharya) | **1114–1185** | ***Siddhanta Shiromani*** (c. 1150): **Lilavati**, **Bijaganita**, Grahaganita, Goladhyaya; *Karanakutuhala* | **Chakravala** method in full form (example $x^2-61y^2=1$, least solution $x=1766319049,\ y=226153980$). Ideas related to differentials. $a/0$ as infinite (*khahara*). Permutations, combinatorics. |
| Narayana Pandita | c. 14th c. | *Ganita Kaumudi* (1356) | Magic squares, combinatorics, Narayana's cow sequence |
| **Madhava of Sangamagrama** | c. **1340–1425** | (works known through his successors) | **Founder of the Kerala school**. Power series for **$\sin x$, $\cos x$, $\arctan x$**. **$\pi/4 = 1-\frac13+\frac15-\cdots$** with correction terms. Value of $\pi$ correct to 11 decimal places. |
| Parameshvara | c. 1360–1455 | *Drgganita* | Circumradius of a cyclic quadrilateral. Mean-value-type ideas. |
| **Nilakantha Somayaji** | **1444–1544** | ***Tantrasangraha*** (c. 1500), *Aryabhatiya-bhashya* | Revised planetary model. Explained why $\pi$ is irrational ("incommensurable"). |
| Jyeshthadeva | c. 1500–1575 | ***Yuktibhasha*** (in Malayalam) | **Proofs** (*yukti*) of the Kerala series |

## 2. Key results with formulas
**Zero and place value.** Decimal place-value notation with zero was established in India by about the 5th–7th century. Brahmagupta (628) gave the first systematic rules:
- $a+0=a$, $a-0=a$, $a\times0=0$.
- He also stated $0/0=0$, which is wrong by modern standards.
- Bhaskara II called $a/0$ *khahara* (infinite).

**Brahmagupta's identity (bhavana).**
$$(a^2 + Nb^2)(c^2+Nd^2) = (ac \pm Nbd)^2 + N(ad \pm bc)^2 .$$
In Pell form: if $x_1^2-Ny_1^2=k_1$ and $x_2^2-Ny_2^2=k_2$, then
$$(x_1x_2+Ny_1y_2)^2 - N(x_1y_2+x_2y_1)^2 = k_1k_2.$$
For $N=1$, i.e. the two-squares form, this is the Brahmagupta–Fibonacci identity.

**Brahmagupta's formula (cyclic quadrilateral).**
$$\text{Area}=\sqrt{(s-a)(s-b)(s-c)(s-d)},\qquad s=\frac{a+b+c+d}2.$$
It holds only for **cyclic** quadrilaterals. With $d=0$ it reduces to Heron's formula.
- Diagonals: $p^2=\frac{(ac+bd)(ad+bc)}{ab+cd}$ and $q^2=\frac{(ac+bd)(ab+cd)}{ad+bc}$, so $pq = ac+bd$ (Ptolemy).

**Brahmagupta's theorem.** In a cyclic quadrilateral with **perpendicular diagonals**, the line through the intersection of the diagonals that is perpendicular to one side bisects the opposite side.

**Kuttaka (Aryabhata I).** Solves $ax+by=c$ (equivalently $ax\equiv c \pmod b$) by repeated division, much like the Euclidean algorithm. A solution exists iff $\gcd(a,b)\mid c$.

**Chakravala (Jayadeva, Bhaskara II).** Solves $x^2-Ny^2=1$:
1. Start from $a^2-Nb^2=k$.
2. Choose $m$ with $k\mid a+bm$ and $|m^2-N|$ minimal.
3. Update $a\to \frac{am+Nb}{|k|}$, $b\to\frac{a+bm}{|k|}$, $k\to\frac{m^2-N}{k}$.
4. Repeat until $k=\pm1,\pm2,\pm4$, then finish with bhavana.

Famous cases: $N=61$ gives $(1766319049,\ 226153980)$; $N=92$ gives $(1151,120)$; $N=67$ gives $(48842,5967)$.

**Madhava series.**
$$\arctan x = x-\frac{x^3}3+\frac{x^5}5-\cdots,\qquad \sin x = x - \frac{x^3}{3!}+\cdots,\qquad \cos x = 1-\frac{x^2}{2!}+\cdots$$
- $\frac\pi4 = 1-\frac13+\frac15-\cdots$ (Madhava–Leibniz).
- $\pi = \sqrt{12}\left(1-\frac{1}{3\cdot3}+\frac1{5\cdot3^2}-\cdots\right)$.

**Aryabhata's sine table.** 24 values of $R\sin\theta$ at intervals of $3^\circ45'$ with $R=3438$ (since $3438\approx 21600/2\pi$ minutes of arc). He gave them as *differences*.

**Sum formulas (Aryabhata).** $\sum_{k=1}^n k^2 = \frac{n(n+1)(2n+1)}6$ and $\sum k^3 = \left(\sum k\right)^2$.

**Mahavira.** ${}^nC_r = \frac{n(n-1)\cdots(n-r+1)}{1\cdot2\cdots r}$.

**Sridhara's quadratic rule.** Multiply $ax^2+bx=c$ by $4a$, then complete the square: $x = \frac{\sqrt{b^2+4ac}-b}{2a}$.

**Pingala.** Counting metres of $n$ syllables gives $2^n$ patterns. Counting by total length gives the numbers now called Fibonacci (later made explicit by Virahanka, c. 7th c., and Hemachandra, 12th c.).

## 3. Quick author ↔ work recall
| Work | Author |
|---|---|
| Sulba Sutra | Baudhayana (also Apastamba, Katyayana, Manava) |
| Chandahsutra | Pingala |
| Aryabhatiya | Aryabhata I |
| Pancha-siddhantika, Brihat Samhita | Varahamihira |
| Mahabhaskariya, Laghubhaskariya | Bhaskara I |
| Brahmasphutasiddhanta, Khandakhadyaka | Brahmagupta |
| Ganitasarasangraha | Mahavira |
| Patiganita, Trishatika | Sridhara |
| Lilavati, Bijaganita, Siddhanta Shiromani | Bhaskara II |
| Ganita Kaumudi | Narayana Pandita |
| Tantrasangraha | Nilakantha Somayaji |
| Yuktibhasha | Jyeshthadeva |

## 4. Exam traps
- **Bhaskara I** (7th c., commentator on Aryabhata, sine approximation) is **not Bhaskara II** (12th c., Lilavati, chakravala).
- Aryabhata's $\pi$ is $3.1416$ (62832/20000), **not** $22/7$.
- Brahmagupta's area formula needs a **cyclic** quadrilateral.
- *Lilavati* and *Bijaganita* are **parts of Siddhanta Shiromani**.
- Kuttaka is for **linear** indeterminate equations. Chakravala and bhavana are for **quadratic** (Pell) ones.
- The **Madhava** series predates Gregory and Leibniz by about 250 years. **Yuktibhasha** (Jyeshthadeva) contains the proofs.
- Aryabhatiya dates to 499 CE, when Aryabhata was 23 (born 476).
