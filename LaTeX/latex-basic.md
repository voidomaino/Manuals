# LaTeX 帮助文档 Documentation

## 1 关于LaTeX公式编辑 Introduce

**LaTeX**（常被读作/ˈlɑːtɛk/或/ˈleɪtɛk/，正确读音:/ˈlɑːtɛx/音译：拉泰赫，写作 $L^AT_EX$ ），是一种基于 TeX 的排版系统，由美国计算机科学家[莱斯利·兰伯特](https://zh.wikipedia.org/wiki/莱斯利·兰波特)在20世纪80年代初期开发。**MathJax** 是一个跨浏览器的 JavaScript 库，它使用 MathML、LaTeX 和 ASCIIMathML 标记在 Web 浏览器中显示数学符号。  

### 1.1 基本使用 Basic

以下字符在LaTeX环境中是保留字符，它们具有特殊含义，只可以特定语法中起作用，所以并不能在输入框中直接输入它们（会报错或者不会渲染）

```latex
# % ^ & _ { } ~ \
        
```

如您因其他原因需要直接显示它们，请在其前面加入`\` 反斜杠或其它转义符。

```latex
\# \% ^\wedge \& \_ \{ \} \sim \backslash
        
```

$$
\# \% ^\wedge \& \_ \{ \} \sim \backslash
$$

## 2 数学公式编辑 Displaying a formula

### 2.1 符号与字母 Symbol and Alphabet

#### 2.1.1 希腊字母 Greek alphabet

| 序号 | 小写          | LaTeX       | 读音                   |
| ---- | ------------- | ----------- | ---------------------- |
| 1    | $\alpha$      | \alpha      | /ˈælfə/                |
| 2    | $\beta$       | \beta       | /ˈbiːtə/, US: /ˈbeɪtə/ |
| 3    | $\gamma$      | \gamma      | /ˈɡæmə/                |
| 4    | $\delta$      | \delta      | /ˈdɛltə/               |
| 5    | $\epsilon$    | \epsilon    | /ˈɛpsɪlɒn/             |
| 6    | $\varepsilon$ | \varepsilon | /ˈɛpsɪlɒn/             |
| 7    | $\zeta$       | \zeta       | /ˈzeɪtə/               |
| 8    | $\eta$        | \eta        | /ˈeɪtə/                |
| 9    | $\theta$      | \theta      | /ˈθiːtə/               |
| 10   | $\vartheta$   | \vartheta   | /ˈθiːtə/               |
| 11   | $\iota$       | \iota       | /aɪˈoʊtə/              |
| 12   | $\kappa$      | \kappa      | /ˈkæpə/                |
| 13   | $\lambda$     | \lambda     | /ˈlæmdə/               |
| 14   | $\mu$         | \mu         | /mjuː/                 |
| 15   | $\nu$         | \nu         | /njuː/                 |
| 16   | $\xi$         | \xi         | /zaɪ, ksaɪ/            |
| 17   | $o$           | o           | /ˈɒmɪkrɒn/             |
| 18   | $\pi$         | \pi         | /paɪ/                  |
| 19   | $\varpi$      | \varpi      | /paɪ/                  |
| 20   | $\rho$        | \rho        | /roʊ/                  |
| 21   | $\varrho$     | \varrho     | /roʊ/                  |
| 22   | $\sigma$      | \sigma      | /ˈsɪɡmə/               |
| 23   | $\varsigma$   | \varsigma   | /ˈsɪɡmə/               |
| 24   | $\tau$        | \tau        | /taʊ, tɔː/             |
| 25   | $\upsilon$    | \upsilon    | /ˈʌpsɪlɒn/             |
| 26   | $\phi$        | \phi        | /faɪ/                  |
| 27   | $\varphi$     | \varphi     | /faɪ/                  |
| 28   | $\chi$        | \chi        | /kaɪ/                  |
| 29   | $\psi$        | \psi        | /psaɪ/                 |
| 30   | $\omega$      | \omega      | /oʊˈmeɪɡə/             |
| 31   | $\Gamma$      | \Gamma      | /ˈɡæmə/                |
| 32   | $\Delta$      | \Delta      | /ˈdɛltə/               |
| 33   | $\Theta$      | \Theta      | /ˈθiːtə/               |
| 34   | $\Lambda$     | \Lambda     | /ˈlæmdə/               |
| 35   | $\Xi$         | \Xi         | /zaɪ, ksaɪ/            |
| 36   | $\Pi$         | \Pi         | /paɪ/                  |
| 37   | $\Sigma$      | \Sigma      | /ˈsɪɡmə/               |
| 38   | $\Upsilon$    | \Upsilon    | /ˈʌpsɪlɒn/             |
| 39   | $\Phi$        | \Phi        | /faɪ/                  |
| 40   | $\Psi$        | \Psi        | /psaɪ/                 |
| 41   | $\Omega$      | \Omega      | /oʊˈmeɪɡə/             |

**注意**： MathJax 支持的大写希腊字母有限，如需其他（如大写 Alpha ），可使用**罗马体**转换，如`\mathrm{A}`表示大写Alpha：$\mathrm{A}$。

#### 2.1.2 希伯来字母 Hebrew alphabet

| 序号 | 图标      | LaTeX   | 英文   |
| ---- | --------- | ------- | ------ |
| 1    | $\aleph$  | \aleph  | aleph  |
| 2    | $\beth$   | \beth   | beth   |
| 3    | $\beth$   | \beth   | gimel  |
| 4    | $\daleth$ | \daleth | daleth |

#### 2.1.3 二元运算符 Binary operations

| 序号 | 图标               | LaTeX            |
| ---- | ------------------ | ---------------- |
| 1    | $+$                | +                |
| 2    | $-$                | -                |
| 3    | $\times$           | \times           |
| 4    | $\div$             | \div             |
| 5    | $\pm$              | \pm              |
| 6    | $\mp$              | \mp              |
| 7    | $\triangleleft$    | \triangleleft    |
| 8    | $\triangleright$   | \triangleright   |
| 9    | $\cdot$            | \cdot            |
| 10   | $\setminus$        | \setminus        |
| 11   | $\star$            | \star            |
| 12   | $\ast$             | \ast             |
| 13   | $\cup$             | \cup             |
| 14   | $\cap$             | \cap             |
| 15   | $\sqcup$           | \sqcup           |
| 16   | $\sqcap$           | \sqcap           |
| 17   | $\wedge$           | \vee             |
| 18   | $\wedge$           | \wedge           |
| 19   | $\circ$            | \circ            |
| 20   | $\bullet$          | \bullet          |
| 21   | $\oplus$           | \oplus           |
| 22   | $\ominus$          | \ominus          |
| 23   | $\odot$            | \odot            |
| 24   | $\oslash$          | \oslash          |
| 25   | $\otimes$          | \otimes          |
| 26   | $\bigcirc$         | \bigcirc         |
| 27   | $\diamond$         | \diamond         |
| 28   | $\uplus$           | \uplus           |
| 29   | $\bigtriangleup$   | \bigtriangleup   |
| 30   | $\bigtriangledown$ | \bigtriangledown |
| 31   | $\lhd$             | \lhd             |
| 32   | $\rhd$             | \rhd             |
| 33   | $\unlhd$           | \unlhd           |
| 34   | $\unrhd$           | \unrhd           |
| 35   | $\amalg$           | \amalg           |
| 36   | $\wr$              | \wr              |
| 37   | $\dagger$          | \dagger          |
| 38   | $\ddagger$         | \ddagger         |

**注意**：`\div`（在 physics 扩展开启状态下为 $\nabla \cdot$ ）

#### 2.1.4 二元关系符 Binary relations

| 序号 | 图标                                     | LaTeX                                  |
| ---- | ---------------------------------------- | -------------------------------------- |
| 1    | $=$                                      | =                                      |
| 2    | $\ne$                                    | \ne                                    |
| 3    | $\neq$                                   | \neq                                   |
| 4    | $\equiv$                                 | \equiv                                 |
| 5    | $\not\equiv$                             | \not\equiv                             |
| 6    | $\doteq$                                 | \doteq                                 |
| 7    | $\doteqdot$                              | \doteqdot                              |
| 8    | $\overset{\underset{\mathrm{def}}{}}{=}$ | \overset{\underset{\mathrm{def}}{}}{=} |
| 9    | $:=$                                     | :=                                     |
| 10   | $\sim$                                   | \sim                                   |
| 11   | $\nsim$                                  | \nsim                                  |
| 12   | $\backsim$                               | \backsim                               |
| 13   | $\thicksim$                              | \thicksim                              |
| 14   | $\thicksim$                              | \simeq                                 |
| 15   | $\simeq$                                 | \backsimeq                             |
| 16   | $\eqsim$                                 | \eqsim                                 |
| 17   | $\cong$                                  | \cong                                  |
| 18   | $\ncong$                                 | \ncong                                 |
| 19   | $\approx$                                | \approx                                |
| 20   | $\thickapprox$                           | \thickapprox                           |
| 21   | $\approxeq$                              | \approxeq                              |
| 22   | $\asymp$                                 | \asymp                                 |
| 23   | $\propto$                                | \propto                                |
| 24   | $\varpropto$                             | \varpropto                             |
| 25   | $<$                                      | <                                      |
| 26   | $\nless$                                 | \nless                                 |
| 27   | $\ll$                                    | \ll                                    |
| 28   | $\not\ll$                                | \not\ll                                |
| 29   | $\lll$                                   | \lll                                   |
| 30   | $\not\lll$                               | \not\lll                               |
| 31   | $\lessdot$                               | \lessdot                               |
| 32   | $>$                                      | >                                      |
| 33   | $\ngtr$                                  | \ngtr                                  |
| 34   | $\gg$                                    | \gg                                    |
| 35   | $\not\gg$                                | \not\gg                                |
| 36   | $\ggg$                                   | \ggg                                   |
| 37   | $\not\ggg$                               | \not\ggg                               |
| 38   | $\gtrdot$                                | \gtrdot                                |
| 39   | $\le$                                    | \le                                    |
| 40   | $\leq$                                   | \leq                                   |
| 41   | $\lneq$                                  | \lneq                                  |
| 42   | $\leqq$                                  | \leqq                                  |
| 43   | $\nleq$                                  | \nleq                                  |
| 44   | $\nleqq$                                 | \nleqq                                 |
| 45   | $\lneqq$                                 | \lneqq                                 |
| 46   | $\lvertneqq$                             | \lvertneqq                             |
| 47   | $\ge$                                    | \ge                                    |
| 48   | $\geq$                                   | \geq                                   |
| 49   | $\gneq$                                  | \gneq                                  |
| 50   | $\geqq$                                  | \geqq                                  |
| 51   | $\ngeq$                                  | \ngeq                                  |
| 52   | $\ngeqq$                                 | \ngeqq                                 |
| 53   | $\gneqq$                                 | \gneqq                                 |
| 54   | $\gvertneqq$                             | \gvertneqq                             |
| 55   | $\lessgtr$                               | \lessgtr                               |
| 56   | $\lesseqgtr$                             | \lesseqgtr                             |
| 57   | $\lesseqqgtr$                            | \lesseqqgtr                            |
| 58   | $\gtrless$                               | \gtrless                               |
| 59   | $\gtreqless$                             | \gtreqless                             |
| 60   | $\gtreqqless$                            | \gtreqqless                            |
| 61   | $\leqslant$                              | \leqslant                              |
| 62   | $\nleqslant$                             | \nleqslant                             |
| 63   | $\eqslantless$                           | \eqslantless                           |
| 64   | $\geqslant$                              | \geqslant                              |
| 65   | $\ngeqslant$                             | \ngeqslant                             |
| 66   | $\eqslantgtr$                            | \eqslantgtr                            |
| 67   | $\lesssim$                               | \lesssim                               |
| 68   | $\lnsim$                                 | \lnsim                                 |
| 69   | $\lessapprox$                            | \lessapprox                            |
| 70   | $\lnapprox$                              | \lnapprox                              |
| 71   | $\gtrsim$                                | \gtrsim                                |
| 72   | $\gnsim$                                 | \gnsim                                 |
| 73   | $\gtrapprox$                             | \gtrapprox                             |
| 74   | $\gnapprox$                              | \gnapprox                              |
| 75   | $\prec$                                  | \prec                                  |
| 76   | $\nprec$                                 | \nprec                                 |
| 77   | $\preceq$                                | \preceq                                |
| 78   | $\npreceq$                               | \npreceq                               |
| 79   | $\precneqq$                              | \precneqq                              |
| 80   | $\succ$                                  | \succ                                  |
| 81   | $\nsucc$                                 | \nsucc                                 |
| 82   | $\succeq$                                | \succeq                                |
| 83   | $\nsucceq$                               | \nsucceq                               |
| 84   | $\succneqq$                              | \succneqq                              |
| 85   | $\preccurlyeq$                           | \preccurlyeq                           |
| 86   | $\curlyeqprec$                           | \curlyeqprec                           |
| 87   | $\succcurlyeq$                           | \succcurlyeq                           |
| 88   | $\curlyeqsucc$                           | \curlyeqsucc                           |
| 89   | $\precsim$                               | \precsim                               |
| 90   | $\precnsim$                              | \precnsim                              |
| 91   | $\precapprox$                            | \precapprox                            |
| 92   | $\precnapprox$                           | \precnapprox                           |
| 93   | $\succsim$                               | \succsim                               |
| 94   | $\succnsim$                              | \succnsim                              |
| 95   | $\succapprox$                            | \succapprox                            |
| 96   | $\succnapprox$                           | \succnapprox                           |

#### 2.1.5 几何符号 Geometric symbols

| 序号 | 图标                  | LaTeX               |
| ---- | --------------------- | ------------------- |
| 1    | $\parallel$           | \parallel           |
| 2    | $\nparallel$          | \nparallel          |
| 3    | $\shortparallel$      | \shortparallel      |
| 4    | $\nshortparallel$     | \nshortparallel     |
| 5    | $\perp$               | \perp               |
| 6    | $\angle$              | \angle              |
| 7    | $\sphericalangle$     | \sphericalangle     |
| 8    | $\measuredangle$      | \measuredangle      |
| 9    | $45^\circ$            | 45^\circ            |
| 10   | $\Box$                | \Box                |
| 11   | $\blacksquare$        | \blacksquare        |
| 12   | $\diamond$            | \diamond            |
| 13   | $\Diamond \lozenge$   | \Diamond \lozenge   |
| 14   | $\lozenge$            | \lozenge            |
| 15   | $\blacklozenge$       | \blacklozenge       |
| 16   | $\bigstar$            | \bigstar            |
| 17   | $\bigcirc$            | \bigcirc            |
| 18   | $\triangle$           | \triangle           |
| 19   | $\bigtriangleup$      | \bigtriangleup      |
| 20   | $\bigtriangledown$    | \bigtriangledown    |
| 21   | $\vartriangle$        | \vartriangle        |
| 22   | $\triangledown$       | \triangledown       |
| 23   | $\blacktriangle$      | \blacktriangle      |
| 24   | $\blacktriangledown$  | \blacktriangledown  |
| 25   | $\blacktriangleleft$  | \blacktriangleleft  |
| 26   | $\blacktriangleright$ | \blacktriangleright |

#### 2.1.6 逻辑符号 Logic symbols

| 序号 | 图标                   | LaTeX                |
| ---- | ---------------------- | -------------------- |
| 1    | $\forall$              | \forall              |
| 2    | $\exists$              | \exists              |
| 3    | $\nexists$             | \nexists             |
| 4    | $\therefore$           | \therefore           |
| 5    | $\because$             | \because             |
| 6    | $\And$                 | \And                 |
| 7    | $\lor$                 | \lor                 |
| 8    | $\vee$                 | \vee                 |
| 9    | $\curlyvee$            | \curlyvee            |
| 10   | $\bigvee$              | \bigvee              |
| 11   | $\land$                | \land                |
| 12   | $\wedge$               | \wedge               |
| 13   | $\curlywedge$          | \curlywedge          |
| 14   | $\bigwedge$            | \bigwedge            |
| 15   | $\bar{q}$              | \bar{q}              |
| 16   | $\bar{abc}$            | \bar{abc}            |
| 17   | $\overline{q}$         | \overline{q}         |
| 18   | $\overline{abc}$       | \overline{abc}       |
| 19   | $\lnot$                | \lnot                |
| 20   | $\neg$                 | \neg                 |
| 21   | $\not\operatorname{R}$ | \not\operatorname{R} |
| 22   | $\bot$                 | \bot                 |
| 23   | $\top$                 | \top                 |
| 24   | $\vdash$               | \vdash               |
| 25   | $\dashv$               | \dashv               |
| 26   | $\vDash$               | \vDash               |
| 27   | $\Vdash$               | \Vdash               |
| 28   | $\Vdash$               | \models              |
| 29   | $\Vvdash$              | \Vvdash              |
| 30   | $\nvdash$              | \nvdash              |
| 31   | $\nVdash$              | \nVdash              |
| 32   | $\nvDash$              | \nvDash              |
| 33   | $\nVDash$              | \nVDash              |
| 34   | $\ulcorner$            | \ulcorner            |
| 35   | $\urcorner$            | \urcorner            |
| 36   | $\llcorner$            | \llcorner            |
| 37   | $\lrcorner$            | \lrcorner            |

#### 2.1.7 集合 Sets

| 序号 | 图标             | LaTeX          |
| ---- | ---------------- | -------------- |
| 1    | $\{\}$           | {}             |
| 2    | $\emptyset$      | \emptyset      |
| 3    | $\varnothing$    | \varnothing    |
| 4    | $\in$            | \in            |
| 5    | $\notin$         | \notin         |
| 6    | $\ni$            | \ni            |
| 7    | $\cap$           | \cap           |
| 8    | $\Cap$           | \Cap           |
| 9    | $\sqcap$         | \sqcap         |
| 10   | $\bigcap$        | \bigcap        |
| 11   | $\cup$           | \cup           |
| 12   | $\Cup$           | \Cup           |
| 13   | $\sqcup$         | \sqcup         |
| 14   | $\bigcup$        | \bigcup        |
| 15   | $\bigsqcup$      | \bigsqcup      |
| 16   | $\uplus$         | \uplus         |
| 17   | $\biguplus$      | \biguplus      |
| 18   | $\setminus$      | \setminus      |
| 19   | $\smallsetminus$ | \smallsetminus |
| 20   | $\times$         | \times         |
| 21   | $\subset$        | \subset        |
| 22   | $\Subset$        | \Subset        |
| 23   | $\sqsubset$      | \sqsubset      |
| 24   | $\supset$        | \supset        |
| 25   | $\Supset$        | \Supset        |
| 26   | $\sqsupset$      | \sqsupset      |
| 27   | $\subseteq$      | \subseteq      |
| 28   | $\nsubseteq$     | \nsubseteq     |
| 29   | $\subsetneq$     | \subsetneq     |
| 30   | $\varsubsetneq$  | \varsubsetneq  |
| 31   | $\sqsubseteq$    | \sqsubseteq    |
| 32   | $\supseteq$      | \supseteq      |
| 33   | $\nsupseteq$     | \nsupseteq     |
| 34   | $\supsetneq$     | \supsetneq     |
| 35   | $\varsupsetneq$  | \varsupsetneq  |
| 36   | $\sqsupseteq$    | \sqsupseteq    |
| 37   | $\subseteqq$     | \subseteqq     |
| 38   | $\nsubseteqq$    | \nsubseteqq    |
| 39   | $\subsetneqq$    | \subsetneqq    |
| 40   | $\varsubsetneqq$ | \varsubsetneqq |
| 41   | $\supseteqq$     | \supseteqq     |
| 42   | $\nsupseteqq$    | \nsupseteqq    |
| 43   | $\supsetneqq$    | \supsetneqq    |
| 44   | $\varsupsetneqq$ | \varsupsetneqq |

#### 2.1.8 箭头 Arrows

| 序号 | 图标                   | LaTeX                |
| ---- | ---------------------- | -------------------- |
| 1    | $\Rrightarrow$         | \Rrightarrow         |
| 2    | $\Lleftarrow$          | \Lleftarrow          |
| 3    | $\Rightarrow$          | \Rightarrow          |
| 4    | $\nRightarrow$         | \nRightarrow         |
| 5    | $\Longrightarrow$      | \Longrightarrow      |
| 6    | $\implies$             | \implies             |
| 7    | $\Leftarrow$           | \Leftarrow           |
| 8    | $\nLeftarrow$          | \nLeftarrow          |
| 9    | $\Longleftarrow$       | \Longleftarrow       |
| 10   | $\Leftrightarrow$      | \Leftrightarrow      |
| 11   | $\nLeftrightarrow$     | \nLeftrightarrow     |
| 12   | $\Longleftrightarrow$  | \Longleftrightarrow  |
| 13   | $\iff$                 | \iff                 |
| 14   | $\Uparrow$             | \Uparrow             |
| 15   | $\Downarrow$           | \Downarrow           |
| 16   | $\Updownarrow$         | \Updownarrow         |
| 17   | $\rightarrow$          | \rightarrow          |
| 18   | $\to$                  | \to                  |
| 19   | $\nrightarrow$         | \nrightarrow         |
| 20   | $\longrightarrow$      | \longrightarrow      |
| 21   | $\leftarrow$           | \leftarrow           |
| 22   | $\gets$                | \gets                |
| 23   | $\nleftarrow$          | \nleftarrow          |
| 24   | $\longleftarrow$       | \longleftarrow       |
| 25   | $\leftrightarrow$      | \leftrightarrow      |
| 26   | $\nleftrightarrow$     | \nleftrightarrow     |
| 27   | $\longleftrightarrow$  | \longleftrightarrow  |
| 28   | $\uparrow$             | \uparrow             |
| 29   | $\downarrow$           | \downarrow           |
| 30   | $\updownarrow$         | \updownarrow         |
| 31   | $\nearrow$             | \nearrow             |
| 32   | $\swarrow$             | \swarrow             |
| 33   | $\nwarrow$             | \nwarrow             |
| 34   | $\searrow$             | \searrow             |
| 35   | $\mapsto$              | \mapsto              |
| 36   | $\longmapsto$          | \longmapsto          |
| 37   | $\rightharpoonup$      | \rightharpoonup      |
| 38   | $\rightharpoondown$    | \rightharpoondown    |
| 39   | $\leftharpoonup$       | \leftharpoonup       |
| 40   | $\leftharpoondown$     | \leftharpoondown     |
| 41   | $\upharpoonleft$       | \upharpoonleft       |
| 42   | $\upharpoonright$      | \upharpoonright      |
| 43   | $\downharpoonleft$     | \downharpoonleft     |
| 44   | $\downharpoonright$    | \downharpoonright    |
| 45   | $\rightleftharpoons$   | \rightleftharpoons   |
| 46   | $\leftrightharpoons$   | \leftrightharpoons   |
| 47   | $\curvearrowleft$      | \curvearrowleft      |
| 48   | $\circlearrowleft$     | \circlearrowleft     |
| 49   | $\Lsh$                 | \Lsh                 |
| 50   | $\upuparrows$          | \upuparrows          |
| 51   | $\rightrightarrows$    | \rightrightarrows    |
| 52   | $\rightleftarrows$     | \rightleftarrows     |
| 53   | $\rightarrowtail$      | \rightarrowtail      |
| 54   | $\looparrowright$      | \looparrowright      |
| 55   | $\curvearrowright$     | \curvearrowright     |
| 56   | $\circlearrowright$    | \circlearrowright    |
| 57   | $\Rsh$                 | \Rsh                 |
| 58   | $\downdownarrows$      | \downdownarrows      |
| 59   | $\leftleftarrows$      | \leftleftarrows      |
| 60   | $\leftrightarrows$     | \leftrightarrows     |
| 61   | $\leftarrowtail$       | \leftarrowtail       |
| 62   | $\looparrowleft$       | \looparrowleft       |
| 63   | $\hookrightarrow$      | \hookrightarrow      |
| 64   | $\hookleftarrow$       | \hookleftarrow       |
| 65   | $\multimap$            | \multimap            |
| 66   | $\leftrightsquigarrow$ | \leftrightsquigarrow |
| 67   | $\rightsquigarrow$     | \rightsquigarrow     |
| 68   | $\twoheadrightarrow$   | \twoheadrightarrow   |
| 69   | $\twoheadleftarrow$    | \twoheadleftarrow    |

#### 2.1.9 特殊 Special

| 序号 | 图标                | LaTeX             |
| ---- | ------------------- | ----------------- |
| 1    | $\infty$            | \infty            |
| 2    | $\aleph$            | \aleph            |
| 3    | $\complement$       | \complement       |
| 4    | $\backepsilon$      | \backepsilon      |
| 5    | $\eth$              | \eth              |
| 6    | $\Finv$             | \Finv             |
| 7    | $\hbar$             | \hbar             |
| 8    | $\Im$               | \Im               |
| 9    | $\imath$            | \imath            |
| 10   | $\jmath$            | \jmath            |
| 11   | $\Bbbk$             | \Bbbk             |
| 12   | $\ell$              | \ell              |
| 13   | $\mho$              | \mho              |
| 14   | $\wp$               | \wp               |
| 15   | $\Re$               | \Re               |
| 16   | $\circledS$         | \circledS         |
| 17   | $\amalg$            | \amalg            |
| 18   | $\%$                | \%                |
| 19   | $\dagger$           | \dagger           |
| 20   | $\ddagger$          | \ddagger          |
| 21   | $\ldots$            | \ldots            |
| 22   | $\cdots$            | \cdots            |
| 23   | $\smile$            | \smile            |
| 24   | $\frown$            | \frown            |
| 25   | $\wr$               | \wr               |
| 26   | $\triangleleft$     | \triangleleft     |
| 27   | $\triangleright$    | \triangleright    |
| 28   | $\diamondsuit$      | \diamondsuit      |
| 29   | $\heartsuit$        | \heartsuit        |
| 30   | $\clubsuit$         | \clubsuit         |
| 31   | $\spadesuit$        | \spadesuit        |
| 32   | $\Game$             | \Game             |
| 33   | $\flat$             | \flat             |
| 34   | $\natural$          | \natural          |
| 35   | $\sharp$            | \sharp            |
| 36   | $\diagup$           | \diagup           |
| 37   | $\diagdown$         | \diagdown         |
| 38   | $\centerdot$        | \centerdot        |
| 39   | $\ltimes$           | \ltimes           |
| 40   | $\rtimes$           | \rtimes           |
| 41   | $\leftthreetimes$   | \leftthreetimes   |
| 42   | $\rightthreetimes$  | \rightthreetimes  |
| 43   | $\eqcirc$           | \eqcirc           |
| 44   | $\circeq$           | \circeq           |
| 45   | $\triangleq$        | \triangleq        |
| 46   | $\bumpeq$           | \bumpeq           |
| 47   | $\Bumpeq$           | \Bumpeq           |
| 48   | $\doteqdot$         | \doteqdot         |
| 49   | $\risingdotseq$     | \risingdotseq     |
| 50   | $\fallingdotseq$    | \fallingdotseq    |
| 51   | $\intercal$         | \intercal         |
| 52   | $\barwedge$         | \barwedge         |
| 53   | $\veebar$           | \veebar           |
| 54   | $\doublebarwedge$   | \doublebarwedge   |
| 55   | $\between$          | \between          |
| 56   | $\pitchfork$        | \pitchfork        |
| 57   | $\vartriangleleft$  | \vartriangleleft  |
| 58   | $\ntriangleleft$    | \ntriangleleft    |
| 59   | $\vartriangleright$ | \vartriangleright |
| 60   | $\ntriangleright$   | \ntriangleright   |
| 61   | $\trianglelefteq$   | \trianglelefteq   |
| 62   | $\ntrianglelefteq$  | \ntrianglelefteq  |
| 63   | $\trianglerighteq$  | \trianglerighteq  |
| 64   | $\ntrianglerighteq$ | \ntrianglerighteq |

### 2.2 运算与函数 Operations & Functions

#### 2.2.1 分数 Fractions

| 类型                                                         | 样式                                                         | LaTeX                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 分数 Fractions                                               | $\frac{2}{4}x=0.5x$                                          | \frac{2}{4}x=0.5x or {2 \over 4}x=0.5x                       |
| 小型分数 Small fractions (force \textstyle)                  | $\tfrac{2}{4}x = 0.5x$                                       | \tfrac{2}{4}x = 0.5x                                         |
| 大型分数（不嵌套） Large (normal) fractions (force \displaystyle) | $\dfrac{2}{4} = 0.5 \qquad \dfrac{2}{c + \dfrac{2}{d + \dfrac{2}{4}}} = a$ | \dfrac{2}{4} = 0.5 \qquad \dfrac{2}{c + \dfrac{2}{d + \dfrac{2}{4}}} = a |
| 大型分数（嵌套） Large (nested) fractions                    | $\cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} = a$             | \cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} = a               |
| 约分线的使用 Cancellations in fractions                      | $\cfrac{x}{1 + \cfrac{\cancel{y}}{\cancel{y}}} = \cfrac{x}{2}$ | \cfrac{x}{1 + \cfrac{\cancel{y}}{\cancel{y}}} = \cfrac{x}{2} |

**注意**：其中 `\cancel` 命令需要 **cancel 扩展包**支持，**cancel 扩展包**是一款自定义宏包。

#### 2.2.2 标准数值函数 Standard numerical functions

| 样式                                                         | LaTeX                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| $\exp_a b = a^b, \exp b = e^b, 10^m$                         | \exp_a b = a^b, \exp b = e^b, 10^m                           |
| $\ln c, \lg d = \log e, \log_{10} f$                         | \ln c, \lg d = \log e, \log_{10} f                           |
| $\sin a, \cos b, \tan c, \cot d, \sec e, \csc f$             | \sin a, \cos b, \tan c, \cot d, \sec e, \csc f               |
| $\arcsin a, \arccos b, \arctan c$                            | \arcsin a, \arccos b, \arctan c                              |
| $\operatorname{arccot} d, \operatorname{arcsec} e, \operatorname{arccsc} f$ | \operatorname{arccot} d, \operatorname{arcsec} e, \operatorname{arccsc} f |
| $\sinh a, \cosh b, \tanh c, \coth d$                         | \sinh a, \cosh b, \tanh c, \coth d                           |
| $\operatorname{sh}k, \operatorname{ch}l, \operatorname{th}m, \operatorname{coth}n$ | \operatorname{sh}k, \operatorname{ch}l, \operatorname{th}m, \operatorname{coth}n |
| $\operatorname{argsh}o, \operatorname{argch}p, \operatorname{argth}q$ | \operatorname{argsh}o, \operatorname{argch}p, \operatorname{argth}q |
| $\operatorname{sgn}r, \left\vert s \right\vert$              | \operatorname{sgn}r, \left\vert s \right\vert                |
| $\min(x,y), \max(x,y)$                                       | \min(x,y), \max(x,y)                                         |

**注意**：LaTeX 和 MathJax 支持的操作符有限，如有特殊操作符，可以使用 `\operatorname{}` 命令自定义，例如

```latex
\operatorname{mydefine}x
```

$$
\operatorname{mydefine}x
$$

#### 2.2.3 根式 Radicals

| 样式            | LaTeX                       |
| --------------- | --------------------------- |
| $\surd$         | \surd                       |
| $\sqrt{\pi}$    | \sqrt{\pi}                  |
| $\sqrt[n]{\pi}$ | \sqrt[n]{\pi}               |
| $\sqrt[n]{\pi}$ | \sqrt[3]{\frac{x^3+y^3}{2}} |

#### 2.2.4 微分与导数 Differentials and derivatives

| 样式                                                         | LaTeX                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| $dt, \mathrm{d}t, \partial t, \nabla\psi$                    | dt, \mathrm{d}t, \partial t, \nabla\psi                      |
| $\mathrm{d}y/\mathrm{d}x, \mathrm{d}y/\mathrm{d}x, \frac{\mathrm{d}y}{\mathrm{d}x}, \frac{\mathrm{d}y}{\mathrm{d}x},\frac{\partial^2}{\partial x_1\partial x_2}y$ | \mathrm{d}y/\mathrm{d}x, \mathrm{d}y/\mathrm{d}x, \frac{\mathrm{d}y}{\mathrm{d}x}, \frac{\mathrm{d}y}{\mathrm{d}x}, \frac{\partial^2}{\partial x_1\partial x_2}y |
| $\prime, \backprime, f^\prime, f', f'', f^{(3)}, \dot y, \ddot y$ | \prime, \backprime, f^\prime, f', f'', f^{(3)}, \dot y, \ddot y |

#### 2.2.5 同余与模算术 Modular arithmetic

| 样式                                   | LaTeX                                |
| -------------------------------------- | ------------------------------------ |
| $s_k \equiv 0 \pmod{m}$                | s_k \equiv 0 \pmod{m}                |
| $a \bmod b$                            | a \bmod b                            |
| $\gcd(m, n), \operatorname{lcm}(m, n)$ | \gcd(m, n), \operatorname{lcm}(m, n) |
| $\mid, \nmid, \shortmid, \nshortmid$   | \mid, \nmid, \shortmid, \nshortmid   |

#### 2.2.6 极限 Limits

| 样式                                | LaTeX                             |
| ----------------------------------- | --------------------------------- |
| $\lim_{n \to \infty}x_n$            | \lim_{n \to \infty}x_n            |
| $\textstyle \lim_{n \to \infty}x_n$ | \textstyle \lim_{n \to \infty}x_n |

#### 2.2.7 界限与投影 Bounds and Projections

| 样式                                     | LaTeX                                  |
| ---------------------------------------- | -------------------------------------- |
| $\min x, \max y, \inf s, \sup t$         | \min x, \max y, \inf s, \sup t         |
| $\lim u, \liminf v, \limsup w$           | \lim u, \liminf v, \limsup w           |
| $\dim p, \deg q, \det m, \ker\phi$       | \dim p, \deg q, \det m, \ker\phi       |
| $\Pr j, \hom l, \lVert z \rVert, \arg z$ | \Pr j, \hom l, \lVert z \rVert, \arg z |

#### 2.2.8 积分 Integral

| 样式                                                         | LaTeX                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| $\int\limits_{1}^{3}\frac{e^3/x}{x^2}\, \mathrm{d}x$         | \int\limits_{1}^{3}\frac{e^3/x}{x^2}\, \mathrm{d}x           |
| $\int_{1}^{3}\frac{e^3/x}{x^2}\, \mathrm{d}x$                | \int_{1}^{3}\frac{e^3/x}{x^2}\, \mathrm{d}x                  |
| $\textstyle \int\limits_{-N}^{N} e^x \mathrm{d}x$            | \textstyle \int\limits_{-N}^{N} e^x \mathrm{d}x              |
| $\textstyle \int_{-N}^{N} e^x \mathrm{d}x$                   | \textstyle \int_{-N}^{N} e^x \mathrm{d}x                     |
| $\iint\limits_D \mathrm{d}x\,\mathrm{d}y$                    | \iint\limits_D \mathrm{d}x\,\mathrm{d}y                      |
| $\iiint\limits_E \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z$      | \iiint\limits_E \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z        |
| $\iiiint\limits_F \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t$ | \iiiint\limits_F \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t |
| $\int_{(x,y)\in C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y$   | \int_{(x,y)\in C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y     |
| $\oint_{(x,y)\in C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y$  | \oint_{(x,y)\in C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y    |

**注意**：积分符号可以使用 `\int_{}^{}` 命令调用，如需双重积分符号只需将 `int` 替换成 `iint` 即可，以此类推，最高支持四重。曲线积分可使用 `\oint` 命令调用，但曲面积分符号在 MathJax 环境中并不支持 `\oiint` 的用法，但仍可通过 `\unicode{}` 命令，即 Unicode 代码的方式进行调用（前提是您需要在设置中打开 Unicode 扩展），具体使用方法如下：

```latex
\unicode{8751} \unicode{x222F}_C
```

$$
\unicode{8751}\qquad \unicode{x222F}_C
$$

曲面积分符号的 Unicode 码十进制为 8751，十六进制为 x222F （注意 x 标识符）

```latex
\unicode{8752} \unicode{x2230}_C
```

$$
\unicode{8752}\qquad \unicode{x2230}_C
$$

三维曲面积分符号的 Unicode 码十进制为 8752，十六进制为 x2230

其他积分符号：

```latex
\unicode{8753} 
\unicode{x2231}_c 
\unicode{8754} 
\unicode{x2232}_c 
\unicode{8755} 
\unicode{x2233}_c
```

$$
\unicode{8753} \qquad
\unicode{x2231}_c \qquad
\unicode{8754} \qquad
\unicode{x2232}_c \qquad
\unicode{8755} \qquad
\unicode{x2233}_c
$$

#### 2.2.9 其他大型运算 Large operators

| 类别              | 样式                           | LaTeX                        |
| ----------------- | ------------------------------ | ---------------------------- |
| 求和 Summation    | $\sum\limits_{a}^{b}$          | \sum\limits_{a}^{b}          |
| 求和 Summation    | $\textstyle \sum_{a}^{b}$      | \textstyle \sum_{a}^{b}      |
| 连乘积 Product    | $\prod\limits_{a}^{b}$         | \prod\limits_{a}^{b}         |
| 连乘积 Product    | $\textstyle \prod_{a}^{b}$     | \textstyle \prod_{a}^{b}     |
| 余积 Coproduct    | $\coprod\limits_{a}^{b}$       | \coprod\limits_{a}^{b}       |
| 余积 Coproduct    | $\textstyle \coprod_{a}^{b}$   | \textstyle \coprod_{a}^{b}   |
| 并集 Union        | $\bigcup\limits_{a}^{b}$       | \bigcup\limits_{a}^{b}       |
| 并集 Union        | $\textstyle \bigcup_{a}^{b}$   | \textstyle \bigcup_{a}^{b}   |
| 交集 Intersection | $\bigcap\limits_{a}^{b}$       | \bigcap\limits_{a}^{b}       |
| 交集 Intersection | $\textstyle \bigcap_{a}^{b}$   | \textstyle \bigcap_{a}^{b}   |
| 析取 Disjunction  | $\bigvee\limits_{a}^{b}$       | \bigvee\limits_{a}^{b}       |
| 析取 Disjunction  | $\textstyle \bigvee_{a}^{b}$   | \textstyle \bigvee_{a}^{b}   |
| 合取 Conjunction  | $\bigwedge\limits_{a}^{b}$     | \bigwedge\limits_{a}^{b}     |
| 合取 Conjunction  | $\textstyle \bigwedge_{a}^{b}$ | \textstyle \bigwedge_{a}^{b} |

### 2.3 上下标 Sub & Super

| 类型                                                         | 样式                                                         | 代码                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 上标 Superscript                                             | $a^2, a^{x+3}$                                               | a^2, a^{x+3}                                                 |
| 下标 Subscript                                               | $a_2$                                                        | a_2                                                          |
| 组合 Grouping                                                | $10^{30} a^{2+2}$                                            | 10^{30} a^{2+2}                                              |
|                                                              | $a_{i,j} b_{f'}$                                             | a\_{i,j} b\_{f'}                                             |
| 上下标混合 Combining sub & super                             | $x_2^3$                                                      | x_2^3                                                        |
|                                                              | ${x_2}^3$                                                    | {x_2}^3                                                      |
| 上标的上标 Super super                                       | $10^{10^{8}}$                                                | 10^{10^{8}}                                                  |
| 混合标识 Preceding and/or additional sub & super             | $\sideset{_1^2}{_3^4}X_a^b$                                  | \sideset{\_1^2}{\_3^4}X_a^b                                  |
|                                                              | ${}_1^2\Omega_3^4$                                           | {}_1^2\Omega_3^4                                             |
| 顶标底标 Stacking                                            | $\overset{\alpha}{\omega}$                                   | \overset{\alpha}{\omega}                                     |
|                                                              | $\underset{\alpha}{\omega}$                                  | \underset{\alpha}{\omega}                                    |
|                                                              | $\overset{\alpha}{\underset{\gamma}{\omega}}$                | \overset{\alpha}{\underset{\gamma}{\omega}}                  |
|                                                              | $\stackrel{\alpha}{\omega}$                                  | \stackrel{\alpha}{\omega}                                    |
| 导数 Derivatives                                             | $x', y'', f', f''$                                           | x', y'', f', f''                                             |
|                                                              | $x^\prime, y^{\prime\prime}$                                 | x^\prime, y^{\prime\prime}                                   |
| 导数 Derivative dots                                         | $\dot{x}, \ddot{x}$                                          | \dot{x}, \ddot{x}                                            |
| 下划线、上划线与向量 Underlines, overlines, vectors          | $\hat a \, \bar b \, \vec c$                                 | \hat a  \bar b  \vec c                                       |
|                                                              | $\overrightarrow{a b} \, \overleftarrow{c d} \, \widehat{d e f}$ | \overrightarrow{a b}  \overleftarrow{c d}  \widehat{d e f}   |
|                                                              | $\overline{g h i} \, \underline{j k l}$                      | \overline{g h i}  \underline{j k l}                          |
| 弧度 Arc (workaround)                                        | $\overset{\frown} {AB}$                                      | \overset{\frown} {AB}                                        |
| 箭头 Arrows                                                  | $A \xleftarrow{n+\mu-1} B \xrightarrow[T]{n\pm i-1} C$       | A \xleftarrow{n+\mu-1} B \xrightarrow[T]{n\pm i-1} C         |
| 大括号 Overbraces                                            | $\overbrace{ 1+2+\cdots+100 }^{5050}$                        | \overbrace{ 1+2+\cdots+100 }^{5050}                          |
| 底部大括号 Underbraces                                       | $\underbrace{ a+b+\cdots+z }_{26}$                           | \underbrace{ a+b+\cdots+z }_{26}                             |
| 求和运算 Sum                                                 | $\sum\limits_{k=1}^N k^2$                                    | \sum\limits_{k=1}^N k^2                                      |
| 文本模式下的求和运算 Sum (force \textstyle)                  | $\textstyle \sum_{k=1}^N k^2$                                | \textstyle \sum_{k=1}^N k^2                                  |
| 分式中的求和运算 Sum in a fraction (default \textstyle)      | $\frac{\sum_{k=1}^N k^2}{a}$                                 | \frac{\sum_{k=1}^N k^2}{a}                                   |
| 分式中的求和运算 Sum in a fraction (force \displaystyle)     | $\frac{\displaystyle \sum\limits_{k=1}^N k^2}{a}$            | \frac{\displaystyle \sum\limits_{k=1}^N k^2}{a}              |
| 分式中的求和运算 Sum in a fraction (alternative limits style) | $\frac{\sum\limits^{^N}_{k=1} k^2}{a}$                       | \frac{\sum\limits^{^N}_{k=1} k^2}{a}                         |
| 乘积运算 Product                                             | $\prod\limits_{i=1}^N x_i$                                   | \prod\limits_{i=1}^N x_i                                     |
| 乘积运算 Product (force \textstyle)                          | $\textstyle \prod_{i=1}^N x_i$                               | \textstyle \prod_{i=1}^N x_i                                 |
| 副乘运算 Coproduct                                           | $\coprod\limits_{i=1}^N x_i$                                 | \coprod\limits_{i=1}^N x_i                                   |
| 副乘运算 Coproduct (force \textstyle)                        | $\textstyle \coprod_{i=1}^N x_i$                             | \textstyle \coprod_{i=1}^N x_i                               |
| 极限 Limit                                                   | $\lim\limits_{n \to \infty}x_n$                              | \lim\limits_{n \to \infty}x_n                                |
| 极限 Limit (force \textstyle)                                | $\textstyle \lim_{n \to \infty}x_n$                          | \textstyle \lim_{n \to \infty}x_n                            |
| 积分 Integral                                                | $\int\limits_{1}^{3}\frac{e^3/x}{x^2}\, \mathrm{d}x$         | \int\limits_{1}^{3}\frac{e^3/x}{x^2}\, \mathrm{d}x           |
| 积分 Integral (alternative limits style)                     | $\int_{1}^{3}\frac{e^3/x}{x^2}\, \mathrm{d}x$                | \int_{1}^{3}\frac{e^3/x}{x^2}\, \mathrm{d}x                  |
| 积分 Integral (force \textstyle)                             | $\textstyle \int\limits_{-N}^{N} e^x \mathrm{d}x$            | \textstyle \int\limits_{-N}^{N} e^x \mathrm{d}x              |
| 积分 Integral (force \textstyle, alternative limits style)   | $\textstyle \int_{-N}^{N} e^x \,\mathrm{d}x$                 | \textstyle \int_{-N}^{N} e^x \, \mathrm{d}x                  |
| 双重积分 Double integral                                     | $\iint\limits_D \mathrm{d}x\, \mathrm{d}y$                   | \iint\limits_D \mathrm{d}x\, \mathrm{d}y                     |
| 三重积分 Triple integral                                     | $\iiint\limits_E \mathrm{d}x\, \mathrm{d}y\, \mathrm{d}z$    | \iiint\limits_E \mathrm{d}x\, \mathrm{d}y\, \mathrm{d}z      |
| 四重积分 Quadruple integral                                  | $\iiiint\limits_F \mathrm{d}x\, \mathrm{d}y\, \mathrm{d}z\, \mathrm{d}t$ | \iiiint\limits_F \mathrm{d}x\, \mathrm{d}y\, \mathrm{d}z\, \mathrm{d}t |
| 路径积分 Line or path integral                               | $\int_{(x,y)\in C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y$   | \int_{(x,y)\in C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y     |
| 环路积分 Closed line or path integral                        | $\oint_{(x,y)\in C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y$  | \oint_{(x,y)\in C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y    |
| 交集 Intersections                                           | $\bigcap\limits_{i=1}^n E_i$                                 | \bigcap\limits_{i=1}^n E_i                                   |
| 并集 Unions                                                  | $\bigcup\limits_{i=1}^n E_i$                                 | \bigcup\limits_{i=1}^n E_i                                   |

### 2.4 矩阵与多行列式 Matrices & Multilines

| 类型                                                         | 样式                                                         | LaTeX                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 二项式系数 Binomial coefficients                             | $\binom{n}{k}$                                               | \binom{n}{k}                                                 |
| 小型二项式系数 Small binomial coefficients (force \textstyle) | $\tbinom{n}{k}$                                              | \tbinom{n}{k}                                                |
| 大型二项式系数 Large (normal) binomial coefficients (force \displaystyle) | $\dbinom{n}{k}$                                              | \dbinom{n}{k}                                                |
| 矩阵 Matrices                                                | $\begin{matrix} x & y \\  z & v \end{matrix}$                | \begin{matrix} x & y \\  z & v \end{matrix}                  |
|                                                              | $\begin{vmatrix} x & y \\ z & v \end{vmatrix}$               | \begin{vmatrix} x & y \\ z & v \end{vmatrix}                 |
|                                                              | $\begin{Vmatrix} x & y \\ z & v \end{Vmatrix}$               | \begin{Vmatrix} x & y \\ z & v \end{Vmatrix}                 |
|                                                              | $\begin{bmatrix} 0 & \cdots & 0 \\ \vdots & \ddots & \vdots                \\ 0 & \cdots & 0 \end{bmatrix}$ | \begin{bmatrix} 0 & \cdots & 0 \\ \vdots & \ddots & \vdots                \\ 0 & \cdots & 0 \end{bmatrix} |
|                                                              | $\begin{Bmatrix} x & y \\ z & v \end{Bmatrix}$               | \begin{Bmatrix} x & y \\ z & v \end{Bmatrix}                 |
|                                                              | $\begin{pmatrix} x & y \\ z & v \end{pmatrix}$               | \begin{pmatrix} x & y \\ z & v \end{pmatrix}                 |
|                                                              | $\bigl( \begin{smallmatrix} a&b\\  c&d \end{smallmatrix} \bigr)   $ | \bigl( \begin{smallmatrix} a&b\\  c&d \end{smallmatrix} \bigr) |
| 条件定义 Case distinctions                                   | $f(n) = \begin{cases} n/2, & \text{if }n\text{ is even} \\ 3n+1, &                \text{if }n\text{ is odd} \end{cases}$ | f(n) = \begin{cases} n/2, & \text{if }n\text{ is even} \\ 3n+1, &                \text{if }n\text{ is odd} \end{cases} |
| 多行等式 Multiline equations                                 | $\begin{align}  f(x) & = (a+b)^2\\ & = a^2+2ab+b^2  \end{align}            $ | \begin{align}  f(x) & = (a+b)^2\\ & = a^2+2ab+b^2  \end{align} |
|                                                              | $\begin{alignat}{2} f(x) & = (a-b)^2 \\ & = a^2-2ab+b^2                 \end{alignat}      $ | \begin{alignat}{2} f(x) & = (a-b)^2 \\ & = a^2-2ab+b^2                 \end{alignat} |
|                                                              | $\begin{array}{lcl} z & = & a \\ f(x,y,z) & = & x + y +                z \end{array}$ | \begin{array}{lcl} z & = & a \\ f(x,y,z) & = & x + y +                z \end{array} |
|                                                              | $\begin{array}{lcr} z & = & a \\ f(x,y,z) & = & x + y +                z \end{array}$ | \begin{array}{lcr} z & = & a \\ f(x,y,z) & = & x + y +                z \end{array} |
| 方程组 Simultaneous equations                                | $\begin{cases} 3x + 5y + z \\ 7x - 2y + 4z \\ -6x + 3y +                2z \end{cases}$ | \begin{cases} 3x + 5y + z \\ 7x - 2y + 4z \\ -6x + 3y +                2z \end{cases} |
| 数组 Arrays                                                  | $\begin{array}{ | c | c | c} a & b & S \\ \hline 0 & 0 & 1 \\ 0 & 1 & 1 \\ 1 & 0 & 1 \\ 1 & 1 & 0\end{array}$ | \begin{array}{ \| c \| c \| c \| }  a & b & S \\ \hline 0 & 0 & 1 \\\ 0 & 1 & 1 \\\ 1 & 0 & 1 \\\ 1 & 1 & 0  \end{array} |

### 2.5 括号 Brackets

常用的括号符号例如 `( )[ ]{ }……` 这些也可以在输入环境中直接使用：

```latex
2(x+y)=z
```

$$
2(x+y)=z
$$

但如果是在较大的表达式中这些符号就显得不合适了

```latex
( \frac{\pi}{2} )^n
```

$$
( \frac{\pi}{2} )^n
$$

正确用法应配合 `\left` 和 `\right` 命令使用。

```latex
\left ( \frac{\pi}{2} \right )^n
```

$$
\left ( \frac{\pi}{2} \right )^n
$$

具体可参考下表。

| 类型                                                         | 样式                                                         | LaTeX                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 圆括号、小括号 Parentheses                                   | $\left ( \frac{a}{b} \right )$                               | \left ( \frac{a}{b} \right )                                 |
| 方括号、中括号 Brackets                                      | $\left [ \frac{a}{b} \right ] \quad \left \lbrack \frac{a}{b} \right \rbrack$ | \left [ \frac{a}{b} \right ] \quad \left \lbrack \frac{a}{b} \right \rbrack |
| 花括号、大括号 Braces                                        | $ \left\lbrace \frac{a}{b} \right\rbrace$                    | \left \lbrace \frac{a}{b} \right \rbrace                     |
| 角括号 Angle brackets                                        | $\left \langle \frac{a}{b} \right \rangle$                   | \left \langle \frac{a}{b} \right \rangle                     |
| 单竖线和双竖线 Bars and double bars                          | $\left \vert \frac{a}{b} \right \vert \quad \left \Vert \frac{c}{d} \right \Vert$ | \left \vert \frac{a}{b} \right \vert \quad \left \Vert \frac{c}{d} \right \Vert |
| 取整函数与取顶函数 Floor and ceiling functions:              | $\left \lfloor \frac{a}{b} \right \rfloor \quad \left \lceil \frac{c}{d} \right \rceil$ | \left \lfloor \frac{a}{b} \right \rfloor \quad \left \lceil \frac{c}{d} \right \rceil |
| 斜线与反斜线 Slashes and backslashes                         | $\left / \frac{a}{b} \right \backslash$                      | \left / \frac{a}{b} \right \backslash                        |
| 上下箭头 Up, down, and up-down arrows                        | $\left \uparrow \frac{a}{b} \right \downarrow \quad \left \Uparrow \frac{a}{b} \right                \Downarrow \quad \left \updownarrow \frac{a}{b} \right \Updownarrow$ | \left \uparrow \frac{a}{b} \right \downarrow \quad \left \Uparrow \frac{a}{b} \right                \Downarrow \quad \left \updownarrow \frac{a}{b} \right \Updownarrow |
| 混合括号 Delimiters can be mixed,as long as \left and \right match | $\left [ 0,1 \right ) \left \langle \psi \right\vert $       | \left [ 0,1 \right ) \left \langle \psi \right \|            |
| 如果您不希望某一侧括号显示，可以使用\left. 和 \right.（带有英文句号） Use \left. and \right. if you do not want a delimiter to appear | $\left . \frac{A}{B} \right \rbrace \to X$                   | \left . \frac{A}{B} \right } \to X                           |
| 括号的大小 Size of the delimiters (add "l" or "r" to indicate the side for proper spacing) | $( \bigl( \Bigl( \biggl( \Biggl( \dots \Biggr] \biggr] \Bigr] \bigr] ]$ | ( \bigl( \Bigl( \biggl( \Biggl( \dots \Biggr] \biggr] \Bigr] \bigr] ] |
|                                                              | $\lbrace \bigl\lbrace \Bigl\lbrace \biggl\lbrace \Biggl\lbrace \dots\Biggr\rangle\biggr\rangle\Bigr\rangle \bigr\rangle \rangle$ | \lbrace \bigl\lbrace \Bigl\lbrace \biggl\lbrace \Biggl\lbrace \dots \Biggr\rangle \biggr\rangle \Bigr\rangle\bigr\rangle \rangle |
|                                                              | $\vert \big\vert \Big\vert \bigg\vert \Bigg\vert \dots \Bigg \vert \bigg \vert \Big \vert \big \vert$ | \vert \big\vert \Big\vert \bigg\vert \Bigg\vert \dots \Bigg \vert \bigg \vert \Big \vert \big \vert |
|                                                              | $\lfloor \bigl\lfloor \Bigl\lfloor \biggl\lfloor \Biggl\lfloor \dots \Biggr\rceil                \biggr\rceil \Bigr\rceil \bigr\rceil \rceil$ | \lfloor \bigl\lfloor \Bigl\lfloor \biggl\lfloor \Biggl\lfloor \dots \Biggr\rceil \biggr\rceil \Bigr\rceil \bigr\rceil \rceil |
|                                                              | $\uparrow \big\uparrow \Big\uparrow \bigg\uparrow \Bigg\uparrow \dots \Bigg\Downarrow                \bigg\Downarrow \Big\Downarrow \big\Downarrow \Downarrow$ | \uparrow \big\uparrow \Big\uparrow \bigg\uparrow \Bigg\uparrow \dots \Bigg\Downarrow\bigg\Downarrow \Big\Downarrow \big\Downarrow \Downarrow |
|                                                              | $\updownarrow \big\updownarrow \Big\updownarrow \bigg\updownarrow \Bigg\updownarrow                \dots \Bigg\Updownarrow \bigg\Updownarrow \Big\Updownarrow \big\Updownarrow \Updownarrow$ | \updownarrow \big\updownarrow \Big\updownarrow \bigg\updownarrow \Bigg\updownarrow\dots \Bigg\Updownarrow \bigg\Updownarrow \Big\Updownarrow \big\Updownarrow \Updownarrow |
|                                                              | $/ \big/ \Big/ \bigg/ \Bigg/ \dots  \Bigg\backslash \bigg\backslash \Big\backslash                \big\backslash \backslash$ | / \big/ \Big/ \bigg/ \Bigg/ \dots  \Bigg\backslash \bigg\backslash \Big\backslash\big\backslash \backslash |

### 2.6 空格与换行 Spacing & Line breaking

#### 2.6.1 空格 Spacing

MathJax 能够自动处理大多数空格间距的大小，但如果您需要自己控制，可参考下表。

| 序号 | 样式           | LaTeX                     | 中文说明                   |
| ---- | -------------- | ------------------------- | -------------------------- |
| 1    | $a \qquad b$   | a \qquad b                | 双空格                     |
| 2    | $a \quad b$    | a \quad b                 | 单空格                     |
| 3    | $a\ b$         | a\ b                      | 字符空格                   |
| 4    | $a \text{ } b$ | a \text{ } b              | 文本模式中的字符空格       |
| 5    | $a\;b$         | a\;b                      | 大空格                     |
| 6    | $a\,b$         | a\,b or a\thinspace b     | 小空格                     |
| 7    | $ab$           | ab                        | 极小空格(用于乘因子)       |
| 8    | $a b$          | a b                       | 极小空格(用于区分其它语法) |
| 9    | $\mathit{ab}$  | \mathit{ab}               | 没有空格(用于多字母变量)   |
| 10   | $a\!b$         | a\\!b or a\negthinspace b | 负空格                     |

#### 2.6.2 换行 Line breaking

在 MathJax3.0 中取消了使用 `\\` 进行强制换行的功能，因此本页面也采取同样的逻辑，默认为单行公式环境。`\\` 强制换行命令只在支持多行编辑的数学环境中才起作用，如 `eqnarray` 环境、`align` 环境、`array` 环境、`matrix` 环境等等。如您需要显示多行公式，建议在此类环境中输入公式，具体用法参见章节[2.10](###2.10 LaTeX环境 LaTeX environments)。

或者您可直接在 `\displaylines{}` 显示行命令中使用 `\\` 强制换行命令，例如：

```latex
\displaylines{y=1729x \\ y=1729-x}
```

$$
\displaylines{y=1729x \\ y=1729-x}
$$



## 3 参考文献 Reference

[1. LaTeX公式编辑器](https://www.latexlive.com/home)

[2. MathJax Documentation](https://docs.mathjax.org/en/latest/index.html)

[3. Displaying a formula](https://en.wikipedia.org/wiki/Help:Displaying_a_formula)

[4. mathjax/MathJax: Beautiful math in all browsers - GitHub](https://github.com/mathjax/MathJax)

[5. mhchem for MathJax](https://mhchem.github.io/MathJax-mhchem/)
