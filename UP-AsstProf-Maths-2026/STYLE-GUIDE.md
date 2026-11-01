# Style Guide (format used by every module)

## Folder layout
```
Unit-XX-<Name>/
  Questions/NN-<Topic>.md      one file per topic
  Cheatsheets/NN-<Topic>.md    same filename, the matching formula/concept sheet
```

## Question files
- **Exam format:** UPESSC/UPHESC Assistant Professor papers are objective MCQs with 4 options (A–D) and one correct answer.
- **Quality over quantity:** each topic has 10–14 questions, and no two questions test the same idea in the same way.
- **Every question type appears in each topic** (where the topic allows it). Each question is tagged with its type:
  | Tag | Type | What it looks like in past papers |
  |---|---|---|
  | `[Concept]` | Direct fact / definition / theorem recall | "The number of Sylow 3-subgroups of ... is" |
  | `[Numerical]` | Short computation (≤ 2 min) | "The value of $\oint ...$ is" |
  | `[Multi-Statement]` | Statements I, II, III → choose correct combination | "Which of the above is/are correct?" |
  | `[Assertion-Reason]` | A and R, with the standard 4 options | "Both A and R true and R explains A" |
  | `[Match]` | List-I ↔ List-II with coded options | "A-2, B-4, C-1, D-3" |
  | `[NOT-true / Counterexample]` | Spot the false statement or the counterexample | "Which of the following is NOT ..." |
  | `[Application]` | Applies a theorem to a non-obvious situation, or a conceptual trap | |
- Difficulty is shown as ★ (easy), ★★ (moderate) or ★★★ (hard, CSIR-NET level).
- The **answer key and solutions are at the end of the file**, so you can attempt the questions first. Each solution says why the correct option is right and, where useful, why the tempting wrong option is wrong.

Standard Assertion–Reason options:
(A) Both A and R are true and R is the correct explanation of A
(B) Both A and R are true but R is NOT the correct explanation of A
(C) A is true but R is false
(D) A is false but R is true

## Cheatsheet files
These are compact revision sheets: definitions, key theorems (stated precisely, with their hypotheses), formulas, standard results and examples or counterexamples, and the common exam traps. They are meant to be read in about 10 minutes before the exam.

## Notation
Math is written in LaTeX and is made safe for GitHub.

GitHub runs Markdown *before* MathJax. Because of that, some ordinary LaTeX gets damaged: backslash-punctuation such as `\{` and `\,` loses its backslash, `*` and `_` can turn into italics, `|` splits table cells, and `<` can be read as an HTML tag. These files therefore follow a few rules.

**Inside math, use the escape-free form:**

| Instead of | Write |
|---|---|
| `\{` `\}` | `\lbrace` `\rbrace` |
| `\,` | `\thinspace` |
| `\;` | `\ ` (backslash-space) |
| `\!` | `\negthinspace` |
| `\\|` | `\Vert` |
| `\|` inside a table row | `\vert` |
| `\\` | `\cr` |
| `<` `>` | `\lt` `\gt` |
| `*` | `\ast` |
| `\mathbb{Z}_n` | `\mathbb Z_n` (braces dropped when the argument is a single character) |

**Delimiters:**
- Use `$...$` for normal inline math.
- Use `` $`...`$ `` for inline math that GitHub would otherwise break: environments with `&`, maths directly after `"`, `-` or `**`, and spans caught in `_`/`*` emphasis.
- Use a ` ```math ` fenced block for display math containing `&`.
- Use `$$...$$` on its own lines for other display math.

All formulas are checked with GitHub's renderer, MathJax 3 and KaTeX. In the VS Code preview, the `` $`...`$ `` and ` ```math ` forms appear as code. Everything else renders there too.
