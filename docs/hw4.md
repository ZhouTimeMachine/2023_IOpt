# Coursework (3)

## Exercise 1

**Error Bounds(EB)**: See ppt P30, 

$$
    \| \nabla f(\bm x) \|\geqslant \mu \|\bm x - \bm x^* \|, \quad \forall \bm x \in \mathbb{R}^n
$$

## Exercise 2

The definition of Strongly Convex, see ppt P5.

!!! info "Strongly Convex"
    A **continuously differentiable** function $f(x)$ is called **strongly convex** on $\mathbb{R}^n$ (notation $f\in \mathcal{S}^1_{\mu}(\mathbb{R}^n)$) if there exists a constant $\mu>0$ s.t. $\forall$ $x, y\in\mathbb{R}^n$ we have

    $$
        f(\bm y)\geqslant f(\bm x)+ \langle \nabla f(\bm x),\; \bm y - \bm x \rangle + \frac{1}{2} \mu \|\bm y - \bm x\|^2
    $$