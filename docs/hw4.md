# Coursework (4)

## Exercise 1

**Error Bounds(EB)**: See ppt page 30, 

$$
    \| \nabla f(\bm x) \|\geqslant \mu \|\bm x - \bm x^* \|, \quad \forall \bm x \in \mathbb{R}^n
$$

!!! warning "The following method is wrong"

Some Students want to prove 

$$
f\text{ is strongly convex(SC) } \Rightarrow \text{Polyak-Lojasiewicz(PL) condition}
$$

and then use the property $(EB)\equiv (PL)$ on ppt page 30.

However, $(EB)\equiv (PL)$ requires $f\in \mathcal{F}_L^{1, 1}$, namely the **Lipschitz continuous gradient**. But (SC) does not imply Lipschitz continuous gradient.

You can learn more about conditions like (EB) and (PL) in the following links:

- [Linear Convergence of Gradient and Proximal-Gradient Methods Under the Polyak- Lojasiewicz Condition](https://arxiv.org/pdf/1608.04636.pdf)(ECML-PKDD 2016), Appendix A
- [ppt of the above paper](https://www.cs.ubc.ca/~jnutini/documents/PL_talk.pdf), page 18-27
- [old ppt of the above paper](https://optml.lehigh.edu/files/2016/06/ICML2016_Schmidt.pdf), page 16-28

## Exercise 2

The definition of Strongly Convex, see ppt page 5.

!!! info "Strongly Convex"
    A **continuously differentiable** function $f(x)$ is called **strongly convex** on $\mathbb{R}^n$ (notation $f\in \mathcal{S}^1_{\mu}(\mathbb{R}^n)$) if there exists a constant $\mu>0$ s.t. $\forall$ $x, y\in\mathbb{R}^n$ we have

    $$
        f(\bm y)\geqslant f(\bm x)+ \langle \nabla f(\bm x),\; \bm y - \bm x \rangle + \frac{1}{2} \mu \|\bm y - \bm x\|^2
    $$