# 数学公式输入

!!! info "建议自行查询相关资料学习，这里提供常用的内容"

## 数学环境
对于数学环境排版，这里简单介绍两种环境：`aligned` 和 `gathered`

`aligned` 环境常用于公式的对齐，`\\` 用于换行，`&` 标注对齐的位置。
=== "效果"
    $$
    \begin{aligned}
        \int_0^1 x^2\mathrm{d}x
        &= \frac{1}{3}x^3\bigg|_0^1\\
        &= \frac{1}{3}
    \end{aligned}
    $$

=== "LaTeX 源码"
    ```latex
    $$
    \begin{aligned}
        \int_0^1 x^2\mathrm{d}x
        &= \frac{1}{3}x^3\bigg|_0^1\\
        &= \frac{1}{3}
    \end{aligned}
    $$
    ```

`gathered` 环境常用于居中排列多行公式，`\\` 用于换行。
=== "效果"
    $$
    \begin{gathered}
        \int_0^1 x^2\mathrm{d}x = \frac{1}{3}\\
        a^2+b^2=c^2
    \end{gathered}
    $$

=== "LaTeX 源码"
    ```latex
    $$
    \begin{gathered}
        \int_0^1 x^2\mathrm{d}x = \frac{1}{3}\\
        a^2+b^2=c^2
    \end{gathered}
    $$
    ```

可以将 `aligned` 改成 `align`, `gathered` 改成 `gather`, 这样就可以让每一行公式在右侧出现自动编号，可以根据需求自行选择。

## 常用数学符号

给出在课程作业中可能会用到但是可能不知道的数学符号：

- 大于等于 $\geqslant$，小于等于 $\leqslant$：`\geqslant`, `\leqslant`
- 内积的尖括号 $\langle\rangle$：`\langle`, `\rangle`
- 偏导符号 $\partial$：`\partial`
- 微分的 $\mathrm{d}$：建议使用 `\mathrm{d}`
- 范数 $\|a\|$：可以写作 `\| a \|`
    - 当范数内部高度比较大（例如有分式 `\frac{a}{x}` 时）可以使用 `\left\| \frac{a}{x} \right\|` 使其得到适配。
    - 这种 `\left \right` 的方法也同理可应用于 `() [] ||` 等
- 梯度算子 $\nabla$：`\nabla`
- 正三角形 $\Delta$：`\Delta`

## 快捷输入常用数学符号

有的数学符号比较长，但是经常会输入，比如说 `\mathrm{d}`，每次都打一遍太浪费时间。

这时候常常使用自定义命令的方法，类似于 C 语言中的 `#define`，我们可以把 `\mathrm{d}` 定义为 `\di`。在所有 `\usepackage` 的后面，加入如下命令

```latex
\newcommand{\di}{\mathrm{d}}
```

这样就可以使用 `\di` 来代替 `\mathrm{d}` 了，注意自己起的名字不要和已有的命令重复，否则编译会无法通过。

下面给出一些我使用的缩写：
```latex
\newcommand{\inprod}[1]{\left\langle#1\right\rangle}
\newcommand{\norm}[1]{\left\|#1\right\|}
\newcommand{\dif}[2]{\frac{\mathrm{d} #1}{\mathrm{d} #2}}
\newcommand{\pard}[2]{\frac{\partial #1}{\partial #2}}
\newcommand{\trans}{^{\top}}
\newcommand{\di}{\mathrm{d}}
\newcommand{\R}{\mathbb{R}}
\newcommand{\F}{\mathcal{F}}
\newcommand{\Sc}{\mathcal{S}}
\newcommand{\xB}{\bm{x}}
\newcommand{\yB}{\bm{y}}
\newcommand{\gB}{\bm{g}}
\newcommand{\dom}{\mathrm{dom}}
\newcommand{\epi}{\mathrm{epi}}
```

这里还有一种带参数的命令，例如 `\pard`，可以示例使用为 `\pard{f}{x_1}`，显示效果为

$$
    \frac{\partial f}{\partial x_1}
$$