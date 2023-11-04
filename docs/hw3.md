# Coursework (3)

## 可微条件

Exercise 1-3，$f$ 不一定一阶可微；Exercise 5-7，默认 $f$ 一阶连续可微。

$f$ 不一定一阶可微，则使用一般凸函数的定义：$\mathrm{dom} f$ 是凸集，且 $\forall x, y \in \mathrm{dom} f$，$\alpha \in [0, 1]$，有

$$
    f(\lambda x + (1 - \lambda)y) \leqslant \lambda f(x) + (1 - \lambda) f(y)
$$

!!! info "Alternative"
    如果能力有限，可以处理为一阶可微或者二阶可微，评分时会酌情处理。

## Exercise 1

注意 $I$ 不一定有限，甚至不一定可数，不能用 $f_1$, ..., $f_n$ 去描述，也不能用数学归纳法可数地去考虑。

!!! info "Alternative"
    如果能力有限，可以处理为可数或者有限，评分时会酌情处理。

## Exercise 3

注意分别取 $\inf$ 是可能比一起取 $\inf$ 更小的，即

$$
\inf_{y\in Y} f(x_1,y) + \inf_{y\in Y} f(x_2,y) \leqslant \inf_{y\in Y} [ f(x_1,y)+f(x_2,y) ]
$$

考虑实数域上，如果 $\inf f(x) \neq -\infty$，那么可以取到一个 non-increasing 的序列 $f(x_n)$，使得 $\lim\limits_{n\to \infty} f(x_n) = \inf f(x)$。可以参考一下。

!!! info "Alternative"
    如果能力有限，可以处理为 $\exists\; x_0$ 使得 $f(x_0) = \inf f(x)$，评分时会酌情处理。

## Exercise 4

- $|x|^{p-2}$ 在 $x=0$ 处存在问题，考虑 $p=1$
- (2)(3)(4) 自己思考的时候需要考虑 $x=0$ 处应该如何求导，但作为简化，提交的作业中可以直接写出求导结果，但不可导的情况需要考虑
- $\mathcal{F}^{1}$ 要求一阶连续可微，用其他方法证明凸性的同学需要注意一下

## Exercise 5-7

$\mathcal{F}_L^{1, 1}(\mathbb{R})$ 包含的含义有

- $f$ 处处连续可微
- $f$ 的凸性
- $\nabla f$ 以 $L$ 为系数的 Lipschitz 连续性

完整的证明需要说明以上三点，不过重点在于第三点。