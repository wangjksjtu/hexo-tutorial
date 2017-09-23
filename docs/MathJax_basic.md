# MathJax Basic Tutorial
This tutorial is mainly from this incredible answer [here](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference).
 Also it combines my practice and other posts which are listed in __Reference__.

## Intended Readers
This tutorial is intended for beginner for Latex or MathJax and will take readers around one hour to look through. For further study, you can google related info or visit the [offical website](https://www.mathjax.org/).

What's worthy to mention is that this post is not suitable for __experts__ in __LaTex__ or __MathJax__, because it may be too simple and naive for them.  

## Content
 By walking through this post, you can master these knowledge or at least be familiar with:
 - __What MathJax is and Why we use MathJax?__
 - __MathJax Basic Syntax__
 - __Useful Example Symbols and Formulas__

 ## What is MathJax?
 __MathJax__ is a JavaScript display engine for mathematics that works in all browsers.
It can be used to display __LaTex__ formulas. In consequence, if you are experts of LaTex, you can almost use the same syntax in MathJax. For more info, check [here](https://www.mathjax.org/).

The Benefits of MathJax are:
- __High-quality typography__: MathJax™ uses CSS with web fonts or SVG, instead of bitmap images or Flash, so equations scale with surrounding text at all zoom levels.
- __Modular Input & Output__: MathJax is highly modular on input and output. Use MathML, TeX and ASCIImath as input and produce HTML+CSS, SVG and MathML as output.
- __Accessible & reusable__: MathJax is compatible with screenreaders & provides zoom for everyone. You can also copy equations into Office, LaTeX, wikis, and other software.
- __Comprehensive Documents__: http://docs.mathjax.org/en/latest/

As a result, it is of great convenience for us to use MathJax in our websites.

## Basic Syntax

### First of All
To see how any formula was written in any question or answer, including this one, right-click on the expression it and choose "Show Math As > TeX Commands". (When you do this, the '$' will not display. Make sure you add these. See the next point.)

### \$...\$ VS \$\$...\$\$
`$...$` and `$$...$$` are used for display formulas in an Latex file. Also can they be used in Markdown, if you add MathJax render.

__For inline formulas, enclose the formula in `$...$`. For displayed formulas, use `$$...$$`.__  These render differently.

`$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$` is to show $\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$ (which is __inline__ mode)

`$$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$` is to show
 $$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$
 (which is display mode)

 ps: `\sum_{i=0}^n` and `\frac` are very common in formulas.

### Greek Letters

`\alpha, \beta, …, \omega` is to show $\alpha, \beta, …, \omega$. __For uppercase__, `\Gamma, \Delta, …, \Omega` is to show $\Gamma, \Delta, …, \Omega$

Some frequently used greek letters are listed as follows. You can skip this part now and review the table when you want to search for some particular one you need in your articles.

| name | Uppercase | MathJax | Lowercase | MathJax|
| :-------------: | :-------------: | :-------------: | :-------------: | :-------------: |
| alpha | $A$ | `A` | $\alpha$ | `\alpha` |
| beta | $B$ | `B` | $\beta$ | `\beta` |
| gamma | $\Gamma$ | `\Gamma` | $\gamma$ | `\gamma` |
| delta | $\Delta$ | `\Delta` | $\delta$ | `\delta` |
| epsilon | $E$ | `E` | $\epsilon$ | `\epsilon` |
| zeta | $Z$ | `Z` | $\zeta$ | `\zeta` |
| eta | $H$ | `H` | $\eta$ | `\eta` |
| theta | $\Theta$ | `\Theta` | $\theta$ | `\theta` |
| iota | $I$ | `I` | $\iota$ | `\iota` |
| kappa | $K$ | `K` | $\kappa$ | `\kappa` |
| lambda | $\Lambda$ | `\Lambda` | $\lambda$ | `\lambda` |
| mu | $M$ | `M` | $\mu$ | `\mu` |
| nu | $N$ | `N` | $\nu$ | `\nu` |
| xi | $\Xi$ | `\Xi` | $\xi$ | `\xi` |
| pi | $\Pi$ | `\Pi` | $\pi$ | `\pi` |
| rho | $P$ | `P` | $\rho$ | `\rho` |
| sigma | $\Sigma$ | `\Sigma` | $\sigma$ | `\sigma` |
| tau | $T$ | `T` | $\tau$ | `\tau` |
| upsilon | $\Upsilon$ | `\Upsilon` | $\upsilon$ | `\upsilon` |
| phi | $\Phi$ | `\Phi` | $\phi$ | `\phi` |
| chi | $X$ | `X` | $\chi$ | `\chi` |
| psi | $\Psi$ | `\Psi` | $\psi$ | `\psi` |
| omega | $\Omega$ | `\Omega` | $\omega$ | `\omega` |

<!-- Table: Greek Letters List -->
<!-- Uncomment the upper comment line when use pacdoc --latex-engine=xelatex
pdflatex doesn't support this usage-->

<!--| omicron | $O$ | `O` | $\omicron$ | `\omicron` | -->
<!-- For \omicron is not supported in latex -->

### Superscripts or Subscripts
Just use `^` and `_`. For instance,
`x_i^2`: $x_i^2$, `log_2 x`: $log_2 x$. If superscripts or subscripts are expressions, just use `{}`.

__Groups__: Superscripts, subscripts, and other operations apply only to the next “group”. A “group” is either a single symbol, or any formula surrounded by curly braces `{`...`}`. If you do `10^10`, you will get $10^10$. Actually, you should use `10^{10}` instead. The correct display is $10^{10}$

__Other Examples__: Use curly braces to delimit a formula to which a superscript or subscript applies: `x^5^6` is an error; `x^{y^z}` is $x^{y^z}$. However, `{x^y}^z` is ${x^y}^z$
Meanwhile, `x_i^2` is $x_i^2$, but `x_{i^2}` is $x_{i^2}$

### Parentheses
 Ordinary symbols `()[]` make parentheses and brackets $(2+3)[4+4]$ Use `\{` and `\}` for curly braces `{ }`.

 These do not scale with the formula in between, so if you write `(\frac{\sqrt x}{y^3})`, the parentheses will be too small: $(\frac{\sqrt x}{y^3})$. Using `\left` and `\right` will make the sizes adjust automatically to the formula they enclose:
 `\left(\frac{\sqrt x}{y^3}\right)` is $\left(\frac{\sqrt x}{y^3}\right)$

 `\left` and `\right` apply to all the following sorts of parentheses: `(`and`)`$\left(x\right)$, `[`and`]`$\left[x\right]$, `\{`and`\}` $\left\{x\right\}$, `|` $\left|x\right|$, `\vert` $\left\vert x\right\vert$, `\Vert` $\left\Vert x\right\Vert$ , `\langle`and`\rangle` $\left\langle  x\right\rangle$, `\lceil`and`\rceil` $\left\lceil x\right\rceil$, and `\lfloor`and `\rfloor` $\left\lfloor x\right\rfloor$. There are also invisible parentheses, denoted by `.`: `\left.\frac12\right\rbrace` is $\left.\frac12\right\rbrace$.

If manual size adjustments are required: `\Biggl(\biggl(\Bigl(\bigl((x^y)\bigr)\Bigr)\biggr)\Biggr)` $\Biggl(\biggl(\Bigl(\bigl((x^y)\bigr)\Bigr)\biggr)\Biggr)$

### Sums, Integral and Others
`\sum` and `\int`:
`\sum_1^n` is $\sum_1^n$. `\sum_{i=0}^\infty i^2` is $\sum_{i=0}^\infty i^2$. `\int_a^b` is $\int_a^b$

__Others__: `\prod` $\prod$, `\bigcup` $\bigcup$ `\bigcap` $\bigcap$, `\iint` $\iint$ and `\iiint` $\iiint$.

### Fractions
There are two ways to make these. `\frac ab` is $\frac ab$. `\frac{a+1}{b+1}` is $\frac{a+1}{b+1}$. If the numerator and the denominator are complicated, you may prefer `\over`, which splits up the group that it is in: `{a+1\over b+1}` is $a+1\over b+1$


### Fonts
`\mathbb`, `\mathbf`, `\mathtt`, `\mathrm`, `\mathsf`, `\mathcal`, `\mathscr`, `\mathcal`, `\mathscr`, `\mathfrak`
`\mathbb`, `\mathbf`, `\mathtt`, `\mathrm`, `\mathsf` __Example__: $\mathbb A \mathbf A \mathtt A \mathrm A \mathsf A \mathcal A \mathscr A \mathcal A \mathscr A \mathfrak A
\mathbb A \mathbf A \mathtt A \mathrm A \mathsf A$.
-->

<!-- Comment the upper line when use pandoc to convert to pdf. This is because \mathxxxs are not supported in latex -->

### Radical signs
Use `\sqrt{}`: `\sqrt{\sqrt{x_2^3}}` is $\sqrt[3]{5 + \sqrt{x_2^3}}$

For complicated expressions, use `\left(5 + \left({x_2^3}\right)^{1/2}\right)^{1/3}`
$$
\left(5 + \left({x_2^3}\right)^{1/2}\right)^{1/3}
$$

### Special Functions
`\sin`, `\ln`, `\exp`, `\lim`
`\sin x` is $\sin x$. `\ln \sqrt[3]{x^2+y^2}` is $\ln \sqrt[3]{x^2+y^2}$ `\exp x` is $\exp(x)$. `\lim_{x\to 0}` is $\lim_{x\to 0}$.
Please pay attention the differences between __inline mode__ and __displayed mode__
$$
\lim_{x\to 0}
$$

### Special symobols and notations
<!--
- `\lt, \gi, \le \ge \neq`: $\lt\gt\le\ge\neq$. You can use `\not` to put a slash through almost anything: `\not\lt` $\not\lt$ but it often looks bad. -->
<!-- Comment the upper line when use pandoc to convert to pdf. This is because some of them such as \lt are not supported in latex -->
- `\times \div \pm \mp` $\times\div\pm\mp$. `\cdot` is a centered dot: $x \cdot y$
- `\cup \cap \setminus \subset \subseteq \subsetneq \supset \in \notin \emptyset \varnothing` $\cup \cap \setminus \subset \subseteq \subsetneq \supset \in \notin \emptyset \varnothing$
- `{n+1 \choose 2k}` or `\binom{n+1}{2k}1` ${n+1 \choose 2k}$ vs $\binom{n+1}{2k}$
- `\to \rightarrow \leftarrow \Rightarrow \Leftarrow \mapsto` $\to \rightarrow \leftarrow \Rightarrow \Leftarrow \mapsto$
- `\land \lor \lnot \forall \exists \top \bot \vdash \vDash` $\land \lor \lnot \forall \exists \top \bot \vdash \vDash$
- `\star \ast \oplus \circ \bullet`$\star \ast \oplus \circ \bullet$
- `\approx \sim \simeq \cong \equiv \prec \lhd` $\approx \sim \simeq \cong \equiv \prec \lhd$
- `\infty \aleph_0` $\infty \aleph_0$ `\nabla \partial` $\nabla \partial$ `\Im \Re` $\Im \Re$
- `\pmod` and `\equiv`: `a\equiv b\pmod n` $a\equiv b\pmod n$
- `\ldots` is the dots in $a_1, a_2, \ldots, a_n$. `\cdots` is the dots in $a_1 + a_2 + \cdots + a_n$
- Some Greek letters have variant forms: `\epsilon \varepsilon` $\epsilon \varepsilon$, `\phi \varphi` $\phi \varphi$, and others.
Script lowercase l is `\ell` $\ell$

[Detexify](http://detexify.kirelabs.org/classify.html) lets you draw a symbol on a web page and then lists the TeX symbols that seem to resemble it. These are not guaranteed to work in MathJax but are a good place to start. To check that a command is supported, note that MathJax.org maintains a [list of currently supported LaTeX commands](http://docs.mathjax.org/en/latest/tex.html#supported-latex-commands), and one can also check Dr. Carol JVF Burns's page of [TeX Commands Available in MathJax](http://www.onemathematicalcat.org/MathJaxDocumentation/TeXSyntax.htm).

### Spaces
MathJax usually decides for itself how to space formulas, using a complex set of rules. Putting extra literal spaces into formulas will not change the amount of space MathJax puts in: `a_b` and `a__b` are both $a b$. To add more space, use `\,` for a thin space $a\,b$; `\;` for a wider space. `\quad` and `\qquad` are large spaces: $a\quad b$, $a\qquad b$.

### others
__Accents and diacritical marks__: Use `\hat` for a single symbol $\hat x$, `\widehat` for a larger formula $\widehat {xyz}$. Similarly, there are `\bar` $\bar x$ and `\overline` $\overline{xyz}$, and `\vec` $\vec x$, `\overrightarrow` $\overrightarrow {xyz}$ and `\overleftrightarrow` $\overleftrightarrow {xyz}$. For dots. as in ${d \over dx}x\dot x = \ddot x^2 + \dot x \ddot x$, use `\dot` and `\ddot`

__Special characters escaping__: Just use the `\` character: `\$` $\$$, `\{` $\{$, `\_` $\_$, etc. If you want `\` itself, you should use `\backslash` $\backslash$, because `\\` is for a new line.

### In the end.
This tutorial is almost in the end. If you have walked through this tutorial carefully and do some practices(important and essential), you are able to write almost all the formulas by yourself now. More practices, more proficient you will be.

Thanks ___Mark Dominus___ again for this [incredible answer](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference), which I mainly followed and referred to.

Finally, allow me write an formula to say goodbye!
$$
F \cdot t \;
\left(
x^2 + \left(y - \sqrt[3]{x^2} \right)^2 = 1 \;
\right)
\frac {\Delta Q \cdot R} {\Delta t}
$$

## Reference
- https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference
- http://xovel.cn/article/mathjax-basic-tutorial-and-quick-reference.html
- http://detexify.kirelabs.org/classify.html
- http://docs.mathjax.org/en/latest/tex.html#supported-latex-commands
- http://www.onemathematicalcat.org/MathJaxDocumentation/TeXSyntax.htm

__Composed by__ _wangjksjtu_
