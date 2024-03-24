# LaTeX环境 LaTeX environments

环境通常是对代码段的整体描述，用于表达此段代码的角色，如，是矩阵？单行公式？多行公式？还是对齐公式等（本页面不支持文档环境），不同的环境起到的作用不同。以 `\begin{environments}` 开始，`\end{environments}` 结束。如最常用的矩阵命令，也是环境的一种，用法如下：

```latex
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
```

$$
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
$$

具体矩阵用法可参考章节[2.4](###2.4 矩阵与多行列式 Matrices & Multilines)，下面给出几种其它常用环境的具体用法：

## equation环境

`\begin{equation}` 是单行公式环境，这意味着在此环境中只可以输入单行公式，同时 `\\` 等强制换行命令失效。如需对单行长公式进行强制换行，可使用 `\begin{split}` 环境进行嵌套，并用 `&` 字符表示对齐位置，如：

```latex
\begin{equation}
\begin{split}
e ^ { x } = & 1 + \frac { x } { 1 ! } + \frac { x ^ { 2 } } { 2 ! } + \frac { x ^ { 3 } } { 3 ! } + \cdots
\\
& - \infty < x < \infty
\end{split}
\end{equation}
```

$$
\begin{equation}
\begin{split}
e ^ { x } = & 1 + \frac { x } { 1 ! } + \frac { x ^ { 2 } } { 2 ! } + \frac { x ^ { 3 } } { 3 ! } + \cdots
\\
& - \infty < x < \infty
\end{split}
\end{equation}
$$

`\begin{equation}` 环境在排版时可能会出现重影错误，可通过对整体添加 `{}` 解决，如 `{\begin{equation}……\end{equation}}` 。

## eqnarray环境

`\begin{eqnarray}` 是多行公式环境，环境内的所有公式默认右对齐，由LaTeX内核提供。

## align环境

`\begin{align}` 是多行公式环境，环境内的所有公式默认右对齐，由 amsmath 提供，排版较为灵活，如需表示多行公式推荐使用此环境。

```latex
\begin{align}
y = x \\
y = 3x^2 + 5x + 2
\end{align}
```

$$
\begin{align}
y = x \\
y = 3x^2 + 5x + 2
\end{align}
$$

可使用 `&` 字符调整对齐位置。

```latex
\begin{align}
y & = x \\
y & = 3x^2 + 5x + 2
\end{align}
```

$$
\begin{align}
y & = x \\
y & = 3x^2 + 5x + 2
\end{align}
$$

## array环境

`\begin{array}{}` 是数组环境，需手动输入对齐参数：

```latex
\begin{array}{|c|l|r|}
a & b & S \\
\hline
0 & 0 & 1 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
1 & 1 & 0 \\
\end{array}
```

$$
\begin{array}{|c|l|r|}
a & b & S \\
\hline
0 & 0 & 1 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
1 & 1 & 0 \\
\end{array}
$$

对齐参数使用 `c l r` 分别表示居中、居左和居右，如需竖线边框可直接在对齐参数区域输入 `|` 即可，如需横线边框可使用 `\hline` 命令。

更多环境使用可参考章节[2.4](###2.4 矩阵与多行列式 Matrices & Multilines)。