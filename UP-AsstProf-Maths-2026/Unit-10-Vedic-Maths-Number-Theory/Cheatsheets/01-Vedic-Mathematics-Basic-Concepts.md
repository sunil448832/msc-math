# Cheatsheet · Unit 10 · Topic 01 — Vedic Mathematics: Basic Concepts
> Questions: [../Questions/01-Vedic-Mathematics-Basic-Concepts.md](../Questions/01-Vedic-Mathematics-Basic-Concepts.md)

## 1. Background
- **Author:** Jagadguru Swami **Bharati Krishna Tirtha** (1884–1960), Shankaracharya of Govardhana Math, **Puri**.
- **Book:** *Vedic Mathematics*, published **1965**, after his death (Motilal Banarsidass).
- **Content:** **16 sutras** (aphorisms) and **13 sub-sutras** (upa-sutras), covering arithmetic, algebra, simple equations, factorisation, recurring decimals, divisibility, square roots and more.
- **Source claim:** the author said the sutras come from a *parishishta* (appendix) of the **Atharvaveda**. They are **not found in the standard extant Atharvaveda**, and historians treat the system as the author's own modern work. In exams this sometimes appears as a "NOT true" statement.

## 2. The 16 sutras
| # | Sutra | Meaning | Main use |
|---|---|---|---|
| 1 | Ekadhikena Purvena | By one more than the previous one | Squares of numbers ending in 5; $1/p$ for $p$ ending in 9 |
| 2 | Nikhilam Navatashcaramam Dashatah | All from 9 and the last from 10 | Multiplication near a base ($10^n$); complements |
| 3 | Urdhva-Tiryagbhyam | Vertically and crosswise | General multiplication (digit convolution) |
| 4 | Paravartya Yojayet | Transpose and apply | Division by divisors slightly above a base; equations |
| 5 | Shunyam Samyasamuccaye | When the *samuccaya* (sum) is the same, that sum is zero | Solving special equations |
| 6 | (Anurupye) Shunyamanyat | If one is in ratio, the other is zero | Simultaneous linear equations |
| 7 | Sankalana-vyavakalanabhyam | By addition and by subtraction | Simultaneous equations with swapped coefficients |
| 8 | Puranapuranabhyam | By completion or non-completion | Completing the square or cube |
| 9 | Chalana-Kalanabhyam | Differences and similarities | Calculus-type (derivative) ideas, quadratics |
| 10 | Yavadunam | Whatever the extent of its deficiency | Squares near a base |
| 11 | Vyashtisamashtih | Part and whole | Factorisation, averages |
| 12 | Shesanyankena Charamena | The remainders by the last digit | Recurring decimals ($1/7$ etc.) |
| 13 | Sopantyadvayamantyam | The ultimate and twice the penultimate | Special equations |
| 14 | Ekanyunena Purvena | By one less than the previous one | Multiplication by 9, 99, 999, … |
| 15 | Gunitasamuchyah | The product of the sum equals the sum of the product | Checking factorisation |
| 16 | Gunakasamuchyah | The factors of the sum equal the sum of the factors | Factorisation checks |

## 3. The 13 sub-sutras
| Sub-sutra | Meaning |
|---|---|
| Anurupyena | Proportionately (working base such as 50 = 100/2) |
| Shishyate Sheshasamjnah | The remainder remains constant |
| Adyamadyenantyamantyena | The first by the first and the last by the last |
| Kevalaih Saptakam Gunyat | For 7, the multiplicand is 143 |
| Veshtanam | By osculation (divisibility tests) |
| Yavadunam Tavadunam | Lessen by the deficiency |
| Yavadunam Tavadunikritya Vargancha Yojayet | Lessen by the deficiency and set up the square of the deficiency |
| Antyayordashake'pi | Last digits totalling 10 |
| Antyayoreva | Only the last terms |
| Samuccayagunitah | The sum of coefficients in the product |
| Lopanasthapanabhyam | By alternate elimination and retention |
| Vilokanam | By mere observation |
| Gunitasamuccayah Samuccayagunitah | The product of the sums of coefficients of the factors equals the sum of coefficients of the product |

## 4. Worked techniques
**Nikhilam (base $B=10^n$).** For $a=B-x$ and $b=B-y$:
$$ab = (a-y)\cdot B + xy \quad (\text{write } xy \text{ in } n \text{ digits, carry if it overflows}).$$
- $97\times96$: $93\,|\,12 = 9312$.
- $103\times105$: $108\,|\,15 = 10815$.
- $998\times997$: $995\,|\,006 = 995006$.
- Mixed case $(B+x)(B-y)$: the right part is $-xy$, so borrow from the left.

**Anurupyena (working base).** For example, base 50 = 100/2: compute with the deficiencies, then halve the left part.

**Ekadhikena: squares ending in 5.** $(10a+5)^2 = a(a+1)\,|\,25$. Examples: $85^2 = 72\,|\,25 = 7225$ and $115^2 = 132\,|\,25=13225$.

**Antyayordashake'pi.** If the leading parts are equal ($=a$) and the last digits add to 10: $\overline{a u}\times\overline{a v} = a(a+1)\,|\,uv$. Example: $47\times43=2021$.

**Yavadunam (squares near a base).** For $N=B\pm d$: $N^2 = (N\pm d)\,|\,d^2$, i.e. the left part is $N\pm d = B\pm 2d$ and the right part $d^2$ is padded to $n$ digits.
- $96^2 = 92\,|\,16 = 9216$; $104^2 = 108\,|\,16=10816$; $996^2 = 992\,|\,016=992016$.

**Ekanyunena (multiplier $99\ldots9$ with the same number of digits).** $N\times(10^n-1) = (N-1)\,|\,(10^n-1-(N-1))$. Example: $457\times999=456\,|\,543$.

**Urdhva-Tiryagbhyam (2-digit).** $\overline{ab}\times\overline{cd}$: the columns are $ac \;|\; ad+bc \;|\; bd$ (with carries). Example: $23\times41$ gives $8\,|\,2+12=14\,|\,3$, so $943$.

**Paravartya Yojayet (division).** For a divisor just above a base, write its excess digits with the sign changed (the "flag"). Bring down the first digit. Multiply each quotient digit by the flag and add it into the next columns. The last $n$ columns form the remainder.
- Example: $1234\div112$ gives quotient $11$, remainder $2$.

**Ekadhikena for $1/19$.** The ekadhika of 1 (in 19) is 2. Multiply by 2 from right to left starting with 1 (or divide by 2 from left to right). This gives
$$1/19 = 0.\overline{052631578947368421}\quad(\text{period }18).$$
For $1/29$ the multiplier is 3. In general the period is $\operatorname{ord}_p 10$.

**Shunyam Samyasamuccaye (cases).**
1. A common factor in every term gives that factor $=0$. Example: $12x+3x=4x+5x \Rightarrow x=0$.
2. If the products of the independent terms are equal, then $x=0$. Example: $(x+7)(x+9)=(x+3)(x+21)$.
3. For $\dfrac{1}{x+a}+\dfrac1{x+b}=\dfrac1{x+c}+\dfrac1{x+d}$ with $a+b=c+d$: the common sum of the denominators $=0$.
4. For $\dfrac{N_1}{D_1}=\dfrac{N_2}{D_2}$ with $N_1+N_2 = k(D_1+D_2)$: $N_1+N_2=0$. Example: $\frac{3x+4}{6x+7}=\frac{x+1}{2x+3}$ gives $x=-5/4$.

**Sankalana-vyavakalanabhyam.** For $ax+by=p$ and $bx+ay=q$: adding gives $(a+b)(x+y)=p+q$ and subtracting gives $(a-b)(x-y)=p-q$.

## 5. Vinculum (bar) numbers
- A bar digit $\bar d$ means $-d$ in that place. Example: $2\bar1 = 20-1 = 19$; $3\bar1\bar1 = 300-11=289$; $1\bar{2}\bar{3}=100-23=77$.
- To convert to vinculum form, use Nikhilam on the digits $\ge 6$: for example $189 = 2\bar1\bar1$.
- Vinculum form makes multiplication by large digits easier (for example, multiplying by $9 = 1\bar1$).

## 6. Navasesh (digit sums / casting out nines) and beejank
- The digit root of $N$ is $N \bmod 9$ (with 9 in place of 0). It satisfies $\text{dr}(a\pm b)$, $\text{dr}(ab)$ = the same operation applied to the digit roots.
- **Check:** if the digit root of the product $\ne$ dr(a)·dr(b), the answer is wrong. If they match, the answer is **not necessarily** right (transposed digits and errors of a multiple of 9 are not detected).
- Example: $12345\times6789 = 83810205$: $6\times3=18\to9$, and $8+3+8+1+0+2+0+5=27\to9$ ✓.
- **Eleven check:** alternating digit sums work the same way modulo 11 and catch transpositions.

## 7. Exam traps
- **16** sutras and **13** sub-sutras. Do not swap these numbers.
- Ekadhikena means "one **more**"; Ekanyunena means "one **less**".
- Nikhilam means "all from **9**, last from **10**", not the other way round.
- In Nikhilam/Yavadunam, **pad the right part to $n$ digits** for base $10^n$ ($996^2$ is $992016$, not $99216$).
- Urdhva-Tiryagbhyam is the general method. Nikhilam is only convenient near a base.
- A navasesh match does **not** prove an answer correct.
- The book is a 20th-century (1965) work. The Atharvaveda origin of the sutras is disputed and they are not in the extant Vedic texts.
