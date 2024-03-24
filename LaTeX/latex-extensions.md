# LaTeX-extensions

## physics

physics 是一款便携输入物理符号、矩阵及方程的拓展包。

目前已知问题：

LaTeX 默认除号命令 `\div` 在physics包中有新的含义，表示$\nabla \cdot$ 。但直接输入 `\div` 可能会出现排版错误问题，此时可用 `{\div}` 替换，来解决排版问题。若需在 physics 包开启状态下显示默认除号，在其他LaTeX环境下可使用 `\divisionsmybol` 表示，但 MathJax 似乎并不支持此用法。替代解决办法为：

1. 直接在输入框中输入 `÷` 字符。
2. 在 unicode 扩展开启状态下，输入 `\unicode{x00f7}`。

以下参考样式请**手动打开physics扩展查看**。

| 类型                              | 样式（需开启physics扩展查看）                                | LaTeX                                                       |
| --------------------------------- | ------------------------------------------------------------ | ----------------------------------------------------------- |
| 括号 Automatic Bracing            | $\quantity{\frac{1}{1+\frac{1}{2}}}$                         | \quantity{ }                                                |
|                                   | $\qty{\frac{1}{1+\frac{1}{2}}}$                              | \qty{ }                                                     |
|                                   | $\pqty{\frac{1}{1+\frac{1}{2}}}$                             | \pqty{ }                                                    |
|                                   | $\bqty{\frac{1}{1+\frac{1}{2}}}$                             | \bqty{ }                                                    |
|                                   | $\vqty{\frac{1}{1+\frac{1}{2}}}$                             | \vqty{ }                                                    |
|                                   | $\absolutevalue{\frac{1}{1+\frac{1}{2}}}$                    | \absolutevalue{ }                                           |
|                                   | $\abs{\frac{1}{1+\frac{1}{2}}}$                              | \abs{ }                                                     |
|                                   | $\norm{\frac{1}{1+\frac{1}{2}}}$                             | \norm{ }                                                    |
|                                   | $\evaluated{\frac{1}{1+\frac{1}{2}}}_1^2$                    | \evaluated{ }_1^2                                           |
|                                   | $\eval{\frac{1}{1+\frac{1}{2}}}_1^2$                         | \eval{ }_1^2                                                |
|                                   | $\order{\frac{x}{2}}$                                        | \order{ }                                                   |
|                                   | $\commutator{A}{B}$                                          | \commutator{A} {B}                                          |
|                                   | $\comm{A}{B}$                                                | \comm{A} {B}                                                |
|                                   | $\anticommutator{A}{B}$                                      | \anticommutator{A} {B}                                      |
|                                   | $\acomm{A}{B}$                                               | \acomm{A} {B}                                               |
|                                   | $\poissonbracket{A}{B}$                                      | \poissonbracket{A} {B}                                      |
|                                   | $\pb{A}{B}$                                                  | \pb{A} {B}                                                  |
| 矢量符号 Vector Notation          | $\vectorbold{a}$                                             | \vectorbold{ }                                              |
|                                   | $\vb{a}$                                                     | \vb{ }                                                      |
|                                   | $\vb\psi$                                                    | \vb{ }                                                      |
|                                   | $\vb*{a}$                                                    | \vb*{ }                                                     |
|                                   | $\vb*{\psi}$                                                 | \vb*{ }                                                     |
|                                   | $\vectorarrow{a}$                                            | \vectorarrow{ }                                             |
|                                   | $\va{a}$                                                     | \va{ }                                                      |
|                                   | $\va\psi$                                                    | \va{ }                                                      |
|                                   | $\va*{a}$                                                    | \va*{ }                                                     |
|                                   | $\va*{\psi}$                                                 | \va*{ }                                                     |
|                                   | $\vectorunit{a}$                                             | \vectorunit{ }                                              |
|                                   | $\vu{a}$                                                     | \vu{ }                                                      |
|                                   | $\vu{\psi}$                                                  | \vu{ }                                                      |
|                                   | $\vu*{a}$                                                    | \vu*{ }                                                     |
|                                   | $\vu*{\psi}$                                                 | \vu*{ }                                                     |
|                                   | $\dotproduct$                                                | \dotproduct                                                 |
|                                   | $\vdot$                                                      | \vdot                                                       |
|                                   | $\crossproduct$                                              | \crossproduct                                               |
|                                   | $\cross$                                                     | \cross                                                      |
|                                   | $\cp$                                                        | \cp                                                         |
|                                   | $\gradient(\psi)$                                            | \gradient( )                                                |
|                                   | $\grad(\psi)$                                                | \grad( )                                                    |
|                                   | $\grad[\psi]$                                                | \grad[ ]                                                    |
|                                   | $\grad{\psi}$                                                | \grad{ }                                                    |
|                                   | $\divergence(\psi)$                                          | \divergence( )                                              |
|                                   | $\div(\psi)$                                                 | \div( )                                                     |
|                                   | $\div[\psi]$                                                 | \div[ ]                                                     |
|                                   | $\div{\psi}$                                                 | \div{ }                                                     |
|                                   | $\curl(\psi)$                                                | \curl( )                                                    |
|                                   | $\curl[\psi]$                                                | \curl[ ]                                                    |
|                                   | $\curl{\psi}$                                                | \curl{ }                                                    |
|                                   | $\laplacian(\psi)$                                           | \laplacian( )                                               |
|                                   | $\laplacian[\psi]$                                           | \laplacian[ ]                                               |
|                                   | $\laplacian{\psi}$                                           | \laplacian{ }                                               |
| 运算符 Operators                  | $\sin x$                                                     | \sin                                                        |
|                                   | $\sin(x)$                                                    | \sin( )                                                     |
|                                   | $\sin[2]{x}$                                                 | \sin\[2\]( )                                                |
|                                   | $\tr \rho$                                                   | \tr                                                         |
|                                   | $\Tr \rho$                                                   | \Tr                                                         |
|                                   | $\rank M$                                                    | \rank                                                       |
|                                   | $\erf(x)$                                                    | \erf( )                                                     |
|                                   | $\Res[f(z)]$                                                 | \Res[ ]                                                     |
|                                   | $\principalvalue{\int f(z) \, \dd z}$                        | \principalvalue{ }                                          |
|                                   | $\pv{\int f(z)\, \dd z}$                                     | \pv{ }                                                      |
|                                   | $\PV{\int f(z)\, \dd z}$                                     | \PV{ }                                                      |
|                                   | $\Re{\frac{1}{1+\frac{1}{2}}}$                               | \Re{ }                                                      |
|                                   | $\Im{\frac{1}{1+\frac{1}{2}}}$                               | \Im{ }                                                      |
| 快速文本 Quick Quad Text          | $\qqtext{some texts}$                                        | \qqtext{ }                                                  |
|                                   | $\qq{some texts}$                                            | \qq{ }                                                      |
|                                   | $\qq*{some texts}$                                           | \qq*{ }                                                     |
|                                   | $\qcomma$                                                    | \qcomma                                                     |
|                                   | $\qc$                                                        | \qc                                                         |
|                                   | $\qcc$                                                       | \qcc                                                        |
|                                   | $\qif$                                                       | \qif                                                        |
|                                   | $\qthen$                                                     | \qthen                                                      |
|                                   | $\qelse$                                                     | \qelse                                                      |
|                                   | $\qotherwise$                                                | \qotherwise                                                 |
|                                   | $\qunless$                                                   | \qunless                                                    |
|                                   | $\qgiven$                                                    | \qgiven                                                     |
|                                   | $\qusing$                                                    | \qusing                                                     |
|                                   | $\qassume$                                                   | \qassume                                                    |
|                                   | $\qlet$                                                      | \qlet                                                       |
|                                   | $\qfor$                                                      | \qfor                                                       |
|                                   | $\qall$                                                      | \qall                                                       |
|                                   | $\qeven$                                                     | \qeven                                                      |
|                                   | $\qodd$                                                      | \qodd                                                       |
|                                   | $\qinteger$                                                  | \qinteger                                                   |
|                                   | $\qand$                                                      | \qand                                                       |
|                                   | $\qor$                                                       | \qor                                                        |
|                                   | $\qas$                                                       | \qas                                                        |
|                                   | $\qin$                                                       | \qin                                                        |
| 导数 Derivatives                  | $\differential{x}$                                           | \differential{ }                                            |
|                                   | $\dd{x}$                                                     | \dd{ }                                                      |
|                                   | $\dd[3]{x}$                                                  | \dd[3] {x}                                                  |
|                                   | $\dd(\cos{\theta})$                                          | \dd( )                                                      |
|                                   | ${\derivative{f}{x}}$                                        | \derivative{ }{x}                                           |
|                                   | $\dv{x}$                                                     | \dv{ }                                                      |
|                                   | $\dv{f}{x}$                                                  | \dv{ }{x}                                                   |
|                                   | $\dv[n]{f}{x}$                                               | \dv[ ]{f}{x}                                                |
|                                   | $\dv{x}(x^2+x^3)$                                            | \dv{x}( )                                                   |
|                                   | $\dv*{f}{x}$                                                 | \dv*{ }{x}                                                  |
|                                   | $\partialderivative{f}{x}$                                   | \partialderivative{ }{x}                                    |
|                                   | $\pdv{x}$                                                    | \pdv{ }                                                     |
|                                   | $\pdv{f}{x}$                                                 | \pdv{ }{x}                                                  |
|                                   | $\pdv[n]{f}{x}$                                              | \pdv[ ]{f}{x}                                               |
|                                   | $\pdv{x}(x^2+x^3)$                                           | \pdv{x}( )                                                  |
|                                   | $\pdv{f}{x}{y}$                                              | \pdv{ }{x}{y}                                               |
|                                   | $\variation{F[g(x)]}$                                        | \variation{ }                                               |
|                                   | $\var{F[g(x)]}$                                              | \var{ }                                                     |
|                                   | $\var(E-TS)$                                                 | \var( )                                                     |
|                                   | $\functionalderivative{F}{g}$                                | \functionalderivative{ }{g}                                 |
|                                   | $\fdv{g}$                                                    | \fdv{ }                                                     |
|                                   | $\fdv{F}{g}$                                                 | \fdv{ }{g}                                                  |
|                                   | $\fdv{V}(E-TS)$                                              | \fdv{V}( )                                                  |
|                                   | $\fdv*{F}{x}$                                                | \fdv*{ }{x}                                                 |
| 狄拉克符号 Dirac Bracket Notation | $\ket{\frac{\psi + \phi}{2}}$                                | \ket{ }                                                     |
|                                   | $\ket*{\frac{\psi + \phi}{2}}$                               | \ket*{ }                                                    |
|                                   | $\bra{\frac{\psi + \phi}{2}}$                                | \bra{ }                                                     |
|                                   | $\bra*{\frac{\psi + \phi}{2}}$                               | \bra*{ }                                                    |
|                                   | $\innerproduct{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}$ | \innerproduct{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}} |
|                                   | $\braket{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}$      | \braket{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}       |
|                                   | $\braket*{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}$     | \braket*{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}      |
|                                   | $\braket{\frac{\psi + \phi}{2}}$                             | \braket{ }                                                  |
|                                   | $\outerproduct{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}$ | \outerproduct{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}} |
|                                   | $\dyad{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}$        | \dyad{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}         |
|                                   | $\ketbra{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}$      | \ketbra{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}       |
|                                   | $\op{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}$          | \op{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}           |
|                                   | $\ketbra*{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}$     | \ketbra*{\frac{\psi + \phi}{2}}{\frac{\psi + \phi}{2}}      |
|                                   | $\ketbra{\frac{\psi + \phi}{2}}$                             | \ketbra{ }                                                  |
|                                   | $\expectationvalue{\frac{\psi + \phi}{2}}$                   | \expectationvalue{ }                                        |
|                                   | $\expval{\frac{\psi + \phi}{2}}$                             | \expval{ }                                                  |
|                                   | $\ev*{\frac{\psi + \phi}{2}}$                                | \ev{ }                                                      |
|                                   | $\ev{\frac{A + B}{2}}{\psi}$                                 | \ev{ }{\psi}                                                |
|                                   | $\ev*{\frac{\psi + \phi}{2}}$                                | \ev*{ }                                                     |
|                                   | $\ev**{\frac{\psi + \phi}{2}}$                               | \ev**{ }                                                    |
|                                   | $\matrixelement{m}{\frac{A + B}{2}}{n}$                      | \matrixelement{m}{ }{n}                                     |
|                                   | $\matrixel{m}{\frac{A + B}{2}}{n}$                           | \matrixel{m}{ }{n}                                          |
|                                   | $\mel{m}{\frac{A + B}{2}}{n}$                                | \mel{m}{ }{n}                                               |
|                                   | $\mel*{m}{\frac{A + B}{2}}{n}$                               | \mel*{m}{ }{n}                                              |
|                                   | $\mel**{m}{\frac{A + B}{2}}{n}$                              | \mel**{m}{ }{n}                                             |
| 矩阵宏 Matrix macros              | $\mqty{a &b\\c&d}$                                           | \mqty{a & b \\ c & d}                                       |
|                                   | $\mqty(a&b\\c&d)$                                            | \mqty(a & b \\ c & d)                                       |
|                                   | $\mqty*(a&b\\c&d)$                                           | \mqty*(a & b \\ c & d)                                      |
|                                   | $\mqty[a&b\\c&d]$                                            | \mqty[a & b \\ c & d]                                       |
|                                   | $\mqty|a&b\\c&d|$                                            | \mqty\|a & b \\ c & d\|                                     |
|                                   | $\smqty(a&b\\c&d)$                                           | \smqty{a & b \\ c & d}                                      |
|                                   | $\smqty(\imat{3})$                                           | \smqty(\imat{3})                                            |
|                                   | $\smqty{\xmat{1}{2}{3}}$                                     | \smqty(\xmat{1}{2}{3})                                      |
|                                   | $\smqty(\xmat*{a}{3}{3})$                                    | \smqty(\xmat*{a}{3}{3})                                     |
|                                   | $\smqty{\xmat*{a}{3}{1}}$                                    | \smqty(\xmat*{a}{3}{1})                                     |
|                                   | $\smqty(\xmat*{a}{1}{3})$                                    | \smqty(\xmat*{a}{1}{3})                                     |
|                                   | $\smqty(\zmat{2}{2})$                                        | \smqty(\zmat{2}{2})                                         |
|                                   | $\smqty(\pmat{0})$                                           | \smqty(\pmat{0})                                            |
|                                   | $\smqty(\pmat{1})$                                           | \smqty(\pmat{1})                                            |
|                                   | $\smqty(\pmat{2})$                                           | \smqty(\pmat{2})                                            |
|                                   | $\smqty(\pmat{3})$                                           | \smqty(\pmat{3})                                            |
|                                   | $\mqty(\dmat{1,2,3})$                                        | \mqty(\dmat{1,2,3})                                         |
|                                   | $\mqty(\dmat{1,2&3\\4&5})$                                   | \mqty(\dmat{1,2&3\\4&5})                                    |
|                                   | $\mqty(\admat{1,2,3})$                                       | \mqty(\admat{1,2,3})                                        |

其它具体用法可参考[physics扩展官方文档](reference\physics-extension.pdf)。

## mhchem

mhchem 是一款便捷输入化学方程式的扩展包，使用前需要在设置中手动勾选。其具体用法如下：

（1）引用

基本命令为 `\ce{}`，可在 `{}` 中输入化学相关符号。

（2）化学式

在化学环境中，数字 `0123456789` 默认为下标，`+-` 默认为上标，如需强制上标可使用 `^` 符号，例如

```latex
\ce{H2O} \ce{Sb2O3} \ce{H+} \ce{CrO4^2-} \ce{[AgCl2]-} \ce{Y^99+} \ce{Y^{99+}} 
```

$$
\ce{H2O}\quad \ce{Sb2O3}\quad \ce{H+}\quad \ce{CrO4^2-}\quad \ce{[AgCl2]-}\quad \ce{Y^99+}\quad \ce{Y^{99+}}
$$

（3）化学计量数

在化学环境中，计量数应与前面的大写字母使用**空格**分割，对于分数计量数，只需输入 `1/2` 即可显示的效果，如特殊情况需要显示 `1/2` 格式，请用 `( )` 扩起。

```latex
\ce{2H2O} \ce{0.5 H2O} \ce{1/2H2O} \ce{(1/2)H2O} \ce{$n$ H2O}
```

$$
\ce{2H2O}\quad \ce{0.5 H2O}\quad \ce{1/2H2O}\quad \ce{(1/2)H2O}\quad \ce{$n$ H2O}
$$

（4）同位素

```latex
\ce{^{227}_{90}Th+} \ce{^227_90Th+} \ce{^{0}_{-1}n^{-}} \ce{^0_-1n-}
```

$$
\ce{^{227}_{90}Th+}\quad \ce{^227_90Th+}\quad \ce{^{0}_{-1}n^{-}}\quad \ce{^0_-1n-}
$$

在一个复杂的化学式中，上标属于左侧元素还是右侧元素可能并不会明显的体现出来，但为了规范输入，建议使用`{}`分隔符作为区分：

```latex
\ce{H{}^3HO} \ce{H^3HO}
```

$$
\ce{H{}^3HO}\quad \ce{H^3HO}
$$

（5）反应箭头

mhchem 提供了方便的反应箭头输入模式

```latex
\ce{A -> B} \ce{A <- B} \ce{A <-> B}
```

$$
\ce{A -> B}\quad \ce{A <- B}\quad \ce{A <-> B}
$$

```latex
\ce{A <--> B} \ce{A <=> B} \ce{A <=>> B} \ce{A <<=> B}
```

$$
\ce{A <--> B}\quad \ce{A <=> B}\quad \ce{A <=>> B}\quad \ce{A <<=> B}
$$

箭头可以带有两个参数，即 `->[][]`，第一个 `[]` 表示上方参数，第二个 `[]` 表示下方参数

```latex
\ce{A ->[H2O] B} \ce{A ->[{上方文字}][{下方文字}] B}
```

$$
\ce{A ->[H2O] B}\quad \ce{A ->[{上方文字}][{下方文字}] B}
$$

（6）气体和沉淀

在化学环境中可使用独立的 `^` 表示气体 $\ce{^}$，使用独立的 `v` （小写字母 v ）表示沉淀 $\ce{v}$ 。

```latex
\ce{SO4^2- + Ba^2+ -> BaSO4 v}
```

$$
\ce{SO4^2- + Ba^2+ -> BaSO4 v}
$$

```latex
\ce{A v B (v) -> B ^ B (^)}
```

$$
\ce{A v B (v) -> B ^ B (^)}
$$

（7）一些复杂的例子

```latex
\ce{Zn^2+ <=>[+ 2OH-][+ 2H+] $\underset{\text{amphoteres Hydroxid}}{\ce{Zn(OH)2 v}}$ <=>[+ 2OH-][+ 2H+] $\underset{\text{Hydroxozikat}}{\ce{[Zn(OH)4]^2-}}$}
```

$$
\ce{Zn^2+ <=>[+ 2OH-][+ 2H+] $\underset{\text{amphoteres Hydroxid}}{\ce{Zn(OH)2 v}}$ <=>[+ 2OH-][+ 2H+] $\underset{\text{Hydroxozikat}}{\ce{[Zn(OH)4]^2-}}$}
$$

```latex
\ce{$K = \frac{[\ce{Hg^2+}][\ce{Hg}]}{[\ce{Hg2^2+}]}$}
```

$$
\ce{$K = \frac{[\ce{Hg^2+}][\ce{Hg}]}{[\ce{Hg2^2+}]}$}
$$

```latex
\ce{$K = \ce{\frac{[Hg^2+][Hg]}{[Hg2^2+]}}$}
```

$$
\ce{$K = \ce{\frac{[Hg^2+][Hg]}{[Hg2^2+]}}$}
$$

```latex
\ce{Hg^2+ ->[I-] $\underset{\mathrm{red}}{\ce{HgI2}}$ ->[I-]$\underset{\mathrm{red}}{\ce{[Hg^{II}I4]^2-}}$}
```

$$
\ce{Hg^2+ ->[I-] $\underset{\mathrm{red}}{\ce{HgI2}}$ ->[I-]$\underset{\mathrm{red}}{\ce{[Hg^{II}I4]^2-}}$}
$$

## cancel

cancel 扩展包为显示分数中**约分线**的 TeX 宏包，或显示其他划除效果，基本命令为 `\cancel{}`，例如：

```latex
\cfrac{x}{1 + \cfrac{\cancel{y}}{\cancel{y}}} = \cfrac{x}{2}
```

$$
\cfrac{x}{1 + \cfrac{\cancel{y}}{\cancel{y}}} = \cfrac{x}{2}
$$

```latex
\cancel{e^{i \pi} + 1 =0}
```

$$
\cancel{e^{i \pi} + 1 =0}
$$

## Ams

在 AMS 包开启状态下，会在公式后进行自动编号。默认自动编号只在部分环境中起作用，如 `{equation}`、`{eqnarray}` 等。

如，以下代码：

```latex
\begin{equation}
E = mc^2 
\end{equation}
```

在 Ams 包未开启状态下：
$$
\begin{equation}
E = mc^2
\end{equation}
$$
在 Ams 包开启状态下：
$$
\begin{equation}
E = mc^2 \tag{1}
\end{equation}
$$
如您在开启了 AMS 包状态下，整个公式均不希望出现编号，可使用 `{equation\*}`、或者 `{eqnarray\*}` 环境；或单个方程不希望出现编号，可以在指定方程后面添加 `\nonumber` 命令，如：

```latex
\begin{eqnarray*}
E = mc^2 \\
e^{i\pi}+1=0
\end{eqnarray*}

```

$$
\begin{eqnarray*}
E = mc^2 \\
e^{i\pi}+1=0
\end{eqnarray*}
$$

```latex
\begin{eqnarray}
E = mc^2 \\
e^{i\pi}+1=0 \nonumber
\end{eqnarray}
```

$$
\begin{eqnarray}
E = mc^2 \tag{1}\\
e^{i\pi}+1=0
\end{eqnarray}
$$

如您在开启了 AMS 包状态下，个别公式不希望出现编号，或者个别公式希望出现特有编号，可在公式后面使用 `\tag{}` 或者 `\notag` 命令，如：

```latex
\begin{eqnarray}
E = mc^2 \notag\\
e^{i\pi}+1=0 \tag{b}
\end{eqnarray}
```

$$
\begin{eqnarray}
E = mc^2 \notag\\
e^{i\pi}+1=0 \tag{b}
\end{eqnarray}
$$



## AmsCd

amsCd 扩展包是一款生成矩阵图的 TeX 宏包环境，基本环境命令为 `\begin{CD}` `\end{CD}`，基本用法如下：

`@<<<` 表示左箭头；

`@>>>` 表示右箭头；

`@AAA` 表示上箭头；

`@VVV` 表示下箭头；

`@=` 表示水平等号；

`@|` 表示竖直等号；

`@.` 表示空箭头（占位）。

以 `@` 表示箭头开始，以 `<、>、A、V` 等表示箭头方向。如需在箭头上或下插入变量，直接在第一和第二，或第二和第三个箭头方向符号中插入即可，用法实例如下：

```latex
\begin{CD}
A @>a>> B\\
@VVbV @VVcV\\
C @>d>> D
\end{CD}
```

$$
\begin{CD}
A @>a>> B\\
@VVbV @VVcV\\
C @>d>> D
\end{CD}
$$

```latex
\begin{CD}
A @>a>b> B\\
@VlVrV @AlArA\\
C @<a<b< D
\end{CD}
```

$$
\begin{CD}
A @>a>b> B\\
@VlVrV @AlArA\\
C @<a<b< D
\end{CD}
$$

## Unicode

Unicode 扩展包一款显示 Unicode 字符的 TeX 宏包，基本命令为 `\unicode{}`，`{}` 中参数应输入指定字符的**十进制**或**十六进制** Unicode 代码，注意十六进制编码需在前面添加标识位 `x`，例如：

```latex
\unicode{8751} \unicode{x220f}        
```

$$
\unicode{8751}\qquad \unicode{x220f}
$$

## Bbox

Bbox 扩展包一款用于设置公式背景颜色的 TeX 宏包，具体用法如下：

（1）设置背景颜色

在公式中可以使用 `\bbox[options]{math}` 来调用背景颜色命令，第一个参数为颜色或大小，需注意用 `[ ]` 包围，第二个参数为公式。例如：

```latex
\bbox[red]{x+y}
```

$$
\bbox[red]{x+y}
$$

（2）调整背景大小

默认情况下，背景大小为作用范围的最大边界，如需扩大背景，可在第一个参数中加入大小信息，例如：

```latex
\bbox[2pt]{x+y} %设置透明背景，并增加2pt额外距离
```

$$
\bbox[2pt]{x+y}
$$

```latex
\bbox[red,5pt]{x+y} %设置红色背景，并增加5pt额外距离
```

$$
\bbox[red,5pt]{x+y}
$$

## NoErrors

NoErrors 扩展包是一款阻止显示 TeX 错误消息的宏包，使用后将不会显示代码具体错误，而只会显示原始 TeX 代码。

## NewCommand

Newcommand 扩展包提供了 `\def, \newcommand，\renewcommand，\let，\newenvironment` 和 `\renewenvironment` 宏命令，用于在 TeX 中创建新的宏和环境。例如：

```latex
\def\RR{{\bf R}} %将{\bf R}（加粗的R）定义为\RR
\RR %调用\RR命令
```

$$
\def\RR{{\bf R}} %将{\bf R}（加粗的R）定义为\RR
\RR %调用\RR命令
$$