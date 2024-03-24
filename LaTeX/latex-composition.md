# LaTeX 排版

## 颜色

### 字体颜色

在公式中可以使用 `\color{options}{math}` 来调用颜色命令，第一个参数为颜色，第二个参数为公式或文本内容。例如:

```latex
{\color{Blue}x^2}+{\color{Orange}2x}-{\color{LimeGreen}1}
```

$$
{\color{Blue}x^2}+{\color{Orange}2x}-{\color{LimeGreen}1}
$$

```latex
x_{1,2}=\frac{{\color{Blue}-b}\pm\sqrt{\color{Red}b^2-4ac}}{\color{Green}2a }
```

$$
x_{1,2}=\frac{{\color{Blue}-b}\pm\sqrt{\color{Red}b^2-4ac}}{\color{Green}2a }
$$

**注意：** 使用 `\color` 命令时，请将需要设置颜色的部分用 `{ }` 整体扩住，以表明 `\color` 函数作用范围。

### 背景颜色

在文本环境中可以使用 `\colorbox{options}{text}` 来调用背景颜色命令，第一个参数为颜色，第二个颜色为文本内容。例如：

```latex
\colorbox{yellow}{Thistext}
```

$$
\colorbox{yellow}{Thistext}
$$

**注意**：若需要在数学环境中使用 `\colorbox{}{}`，请在第二个参数内加入 `$\displaystyle + 公式$`，例如：

```latex
\colorbox{yellow}{$\displaystyle \frac{a}{b}$}
```

$$
\colorbox{yellow}{$\displaystyle \frac{a}{b}$}
$$

或者您可以使用 **Bbox 扩展**来替换 `\colorbox` 命令，详见[Bbox 扩展](latex-extensions.md\##Bbox)。

### 默认支持颜色

| 支持颜色                                 |                                      |                                    |                                          |
| ---------------------------------------- | ------------------------------------ | ---------------------------------- | ---------------------------------------- |
| $\color{Apricot}{Apricot}$               | $\color{Emerald}{Emerald}$           | $\color{OliveGreen}{OliveGreen}$   | $\color{RubineRed}{RubineRed}$           |
| $\color{Aquamarine}{Aquamarine}$         | $\color{ForestGreen}{ForestGreen}$   | $\color{Orange}{Orange}$           | $\color{Salmon}{Salmon}$                 |
| $\color{Bittersweet}{Bittersweet}$       | $\color{Fuchsia}{Fuchsia}$           | $\color{OrangeRed}{OrangeRed}$     | $\color{SeaGreen}{SeaGreen}$             |
| $\color{Black}{Black}$                   | $\color{Goldenrod}{Goldenrod}$       | $\color{Orchid}{Orchid}$           | $\color{Sepia}{Sepia}$                   |
| $\color{Blue}{Blue}$                     | $\color{Gray}{Gray}$                 | $\color{Peach}{Peach}$             | $\color{SkyBlue}{SkyBlue}$               |
| $\color{BlueGreen}{BlueGreen}$           | $\color{Green}{Green}$               | $\color{Periwinkle}{Periwinkle}$   | $\color{SpringGreen}{SpringGreen}$       |
| $\color{BlueViolet}{BlueViolet}$         | $\color{GreenYellow}{GreenYellow}$   | $\color{PineGreen}{PineGreen}$     | $\color{Tan}{Tan}$                       |
| $\color{BrickRed}{BrickRed}$             | $\color{JungleGreen}{JungleGreen}$   | $\color{Plum}{Plum}$               | $\color{TealBlue}{TealBlue}$             |
| $\color{Brown}{Brown}$                   | $\color{Lavender}{Lavender}$         | $\color{ProcessBlue}{ProcessBlue}$ | $\color{Thistle}{Thistle}$               |
| $\color{BurntOrange}{BurntOrange}$       | $\color{LimeGreen}{LimeGreen}$       | $\color{Purple}{Purple}$           | $\color{Turquoise}{Turquoise}$           |
| $\color{CadetBlue}{CadetBlue}$           | $\color{Magenta}{Magenta}$           | $\color{RawSienna}{RawSienna}$     | $\color{Violet}{Violet}$                 |
| $\color{CarnationPink}{CarnationPink}$   | $\color{Mahogany}{Mahogany}$         | $\color{Red}{Red}$                 | $\color{VioletRed}{VioletRed}$           |
| $\color{Cerulean}{Cerulean}$             | $\color{Maroon}{Maroon}$             | $\color{RedOrange}{RedOrange}$     | $\color{WildStrawberry}{WildStrawberry}$ |
| $\color{CornflowerBlue}{CornflowerBlue}$ | $\color{Melon}{Melon}$               | $\color{RedViolet}{RedViolet}$     | $\color{White}{White}$                   |
| $\color{Cyan}{Cyan}$                     | $\color{MidnightBlue}{MidnightBlue}$ | $\color{Rhodamine}{Rhodamine}$     | $\color{Yellow}{Yellow}$                 |
| $\color{Dandelion}{Dandelion}$           | $\color{Mulberry}{Mulberry}$         | $\color{RoyalBlue}{RoyalBlue}$     | $\color{YellowGreen}{YellowGreen}$       |
| $\color{DarkOrchid}{DarkOrchid}$         | $\color{NavyBlue}{NavyBlue}$         | $\color{RoyalPurple}{RoyalPurple}$ | $\color{YellowOrange}{YellowOrange}$     |

### 使用 RGB 颜色

如需在 `\color` 命令中使用自选RGB颜色，可使用 `{\color[RGB]{0,0,0} }` 命令，例如：

```latex
{\color[RGB]{0,200,0} e^{i \pi} + 1 = 0}
```

$$
{\color[RGB]{0,200,0} e^{i \pi} + 1 = 0}
$$

### 自定义颜色

可使用 `\definecolor` 命令进行自定义颜色，例如：

```latex
\definecolor{mygreen}{RGB}{0,200,0} {\color{mygreen}e^{i \pi} + 1 = 0 }
```

$$
\definecolor{mygreen}{RGB}{0,200,0} {\color{mygreen}e^{i \pi} + 1 = 0 }
$$

## 字体字号

### 字体

因有一些特定代码Mathjax3.0并没有相关支持，所以下表仅做参考。

| 种类                                                  | 样式                                                         | LaTeX                                                        |
| ----------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 希腊字母 Greek alphabet                               | $\mathrm{A} \mathrm{B} \Gamma \Delta \mathrm{E} \mathrm{Z} \mathrm{H} \Theta$ | \mathrm{A} \mathrm{B} \Gamma \Delta \mathrm{E} \mathrm{Z} \mathrm{H} \Theta |
|                                                       | $\mathrm{I} \mathrm{K} \Lambda \mathrm{M} \mathrm{N} \Xi \mathrm{O} \Pi$ | \mathrm{I} \mathrm{K} \Lambda \mathrm{M} \mathrm{N} \Xi \mathrm{O} \Pi |
|                                                       | $\mathrm{R} \Sigma \mathrm{T} \Upsilon \Phi \mathrm{X} \Psi \Omega$ | \mathrm{R} \Sigma \mathrm{T} \Upsilon \Phi \mathrm{X} \Psi \Omega |
|                                                       | $\alpha \beta \gamma \delta \epsilon \zeta \eta \theta$      | \alpha \beta \gamma \delta \epsilon \zeta \eta \theta        |
|                                                       | $\iota \kappa \lambda \mu \nu \xi \omicron \pi$              | \iota \kappa \lambda \mu \nu \xi \omicron \pi                |
|                                                       | $\rho \sigma \tau \upsilon \phi \chi \psi \omega$            | \rho \sigma \tau \upsilon \phi \chi \psi \omega              |
|                                                       | $\varGamma \varDelta \varTheta \varLambda \varXi \varPi \varSigma \varPhi \varUpsilon \varOmega$ | \varGamma \varDelta \varTheta \varLambda \varXi \varPi \varSigma \varPhi \varUpsilon \varOmega |
|                                                       | $\varepsilon \digamma \varkappa \varpi \varrho \varsigma \vartheta \varphi$ | \varepsilon \digamma \varkappa \varpi \varrho \varsigma \vartheta \varphi |
| 希伯来字母 Hebrew symbols                             | $\aleph \beth \gimel \daleth$                                | \aleph \beth \gimel \daleth                                  |
| 黑板报体 Blackboard bold/scripts                      | $\mathbb{ABCDEFGHI}$                                         | \mathbb{ABCDEFGHI}                                           |
|                                                       | $\mathbb{JKLMNOPQR}$                                         | \mathbb{JKLMNOPQR}                                           |
|                                                       | $\mathbb{STUVWXYZ}$                                          | \mathbb{STUVWXYZ}                                            |
| 粗体 Boldface                                         | $\mathbf{ABCDEFGHI}$                                         | \mathbf{ABCDEFGHI}                                           |
|                                                       | $\mathbf{JKLMNOPQR}$                                         | \mathbf{JKLMNOPQR}                                           |
|                                                       | $\mathbf{STUVWXYZ}$                                          | \mathbf{STUVWXYZ}                                            |
|                                                       | $\mathbf{abcdefghijklm}$                                     | \mathbf{abcdefghijklm}                                       |
|                                                       | $\mathbf{nopqrstuvwxyz}$                                     | \mathbf{nopqrstuvwxyz}                                       |
|                                                       | $\mathbf{0123456789}$                                        | \mathbf{0123456789}                                          |
| 粗体希腊字母 Boldface (Greek)                         | $\boldsymbol{\mathrm{A} \mathrm{B} \Gamma \Delta \mathrm{E} \mathrm{Z} \mathrm{H} \Theta} $ | \boldsymbol{\mathrm{A} \mathrm{B} \Gamma \Delta \mathrm{E} \mathrm{Z} \mathrm{H} \Theta} |
|                                                       | $\boldsymbol{\mathrm{I} \mathrm{K} \Lambda \mathrm{M} \mathrm{N} \Xi \mathrm{O} \Pi}$ | \boldsymbol{\mathrm{I} \mathrm{K} \Lambda \mathrm{M} \mathrm{N} \Xi \mathrm{O} \Pi} |
|                                                       | $\boldsymbol{\mathrm{R} \Sigma \mathrm{T} \Upsilon \Phi \mathrm{X} \Psi \Omega}$ | \boldsymbol{\mathrm{R} \Sigma \mathrm{T} \Upsilon \Phi \mathrm{X} \Psi \Omega} |
|                                                       | $\boldsymbol{\alpha \beta \gamma \delta \epsilon \zeta \eta \theta}$ | \boldsymbol{\alpha \beta \gamma \delta \epsilon \zeta \eta \theta} |
|                                                       | $\boldsymbol{\iota \kappa \lambda \mu \nu \xi \omicron \pi}$ | \boldsymbol{\iota \kappa \lambda \mu \nu \xi \omicron \pi}   |
|                                                       | $\boldsymbol{\rho \sigma \tau \upsilon \phi \chi \psi \omega}$ | \boldsymbol{\rho \sigma \tau \upsilon \phi \chi \psi \omega} |
|                                                       | $\boldsymbol{\varepsilon\digamma\varkappa\varpi}$            | \boldsymbol{\varepsilon\digamma\varkappa\varpi}              |
|                                                       | $\boldsymbol{\varrho\varsigma\vartheta\varphi}$              | \boldsymbol{\varrho\varsigma\vartheta\varphi}                |
| 斜体 Italics (拉丁字母默认default for Latin alphabet) | $\mathit{0123456789}$                                        | \mathit{0123456789}                                          |
| 罗马体 Roman typeface                                 | $\mathrm{ABCDEFGHI}$                                         | \mathrm{ABCDEFGHI}                                           |
|                                                       | $\mathrm{JKLMNOPQR}$                                         | \mathrm{JKLMNOPQR}                                           |
|                                                       | $\mathrm{STUVWXYZ}$                                          | \mathrm{STUVWXYZ}                                            |
|                                                       | $\mathrm{abcdefghijklm}$                                     | \mathrm{abcdefghijklm}                                       |
|                                                       | $\mathrm{nopqrstuvwxyz}$                                     | \mathrm{nopqrstuvwxyz}                                       |
|                                                       | $\mathrm{0123456789}$                                        | \mathrm{0123456789}                                          |
| 无衬线体 Sans serif                                   | $\mathsf{ABCDEFGHI}$                                         | \mathsf{ABCDEFGHI}                                           |
|                                                       | $\mathsf{JKLMNOPQR}$                                         | \mathsf{JKLMNOPQR}                                           |
|                                                       | $\mathsf{STUVWXYZ}$                                          | \mathsf{STUVWXYZ}                                            |
|                                                       | $\mathsf{abcdefghijklm}$                                     | \mathsf{abcdefghijklm}                                       |
|                                                       | $\mathsf{nopqrstuvwxyz}$                                     | \mathsf{nopqrstuvwxyz}                                       |
|                                                       | $\mathsf{0123456789}$                                        | \mathsf{0123456789}                                          |
| 手写体 Calligraphy/花体 script                        | $\mathcal{ABCDEFGHI}$                                        | \mathcal{ABCDEFGHI}                                          |
|                                                       | $\mathcal{JKLMNOPQR}$                                        | \mathcal{JKLMNOPQR}                                          |
|                                                       | $\mathcal{STUVWXYZ}$                                         | \mathcal{STUVWXYZ}                                           |
| 德文尖角体 Fraktur typeface                           | $\mathfrak{ABCDEFGHI}$                                       | \mathfrak{ABCDEFGHI}                                         |
|                                                       | $\mathfrak{JKLMNOPQR}$                                       | \mathfrak{JKLMNOPQR}                                         |
|                                                       | $\mathfrak{STUVWXYZ}$                                        | \mathfrak{STUVWXYZ}                                          |
|                                                       | $\mathfrak{abcdefghijklm}$                                   | \mathfrak{abcdefghijklm}                                     |
|                                                       | $\mathfrak{nopqrstuvwxyz}$                                   | \mathfrak{nopqrstuvwxyz}                                     |
|                                                       | $\mathfrak{0123456789}$                                      | \mathfrak{0123456789}                                        |
| 小型手写体 Small scriptstyle text                     | ${\scriptstyle\text{abcdefghijklm}}$                         | {\scriptstyle\text{abcdefghijklm}}                           |

### 字号

| 样式                              | LaTeX                           |
| --------------------------------- | ------------------------------- |
| ${\tiny abc巨小tiny}$             | {\tiny abc巨小tiny}             |
| ${\scriptsize abc超小scriptsize}$ | {\scriptsize abc超小scriptsize} |
| ${\small abc小small}$             | {\small abc小small}             |
| ${\normalsize abc正常normal}$     | {\normalsize abc正常normal}     |
| ${\large abc大large}$             | {\large abc大large}             |
| ${\Large abc超大Large}$           | {\Large abc超大Large}           |
| ${\LARGE abc特大LARGE}$           | {\LARGE abc特大LARGE}           |
| ${\huge abc巨大huge}$             | {\huge abc巨大huge}             |
| ${\Huge abc巨无霸Huge}$           | {\Huge abc巨无霸Huge}           |

**注意**：此处的字号命令只为设置公式**相对大小**时使用，例如：

```latex
{\tiny x+y=z}x+y=z{\Huge x+y=z}
```

$$
{\tiny x+y=z}x+y=z{\Huge x+y=z}
$$

## 方程式编号

通过在行尾添加 `\tag{}` 来为方程式增加编号。

在 Ams 扩展包开启的时候，方程式可以自动编号，详见 [Ams 扩展包](latex-extensions.md\##Ams) 。