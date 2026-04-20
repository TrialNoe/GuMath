---
tags:
  - "#math"
  - math_calculus
  - math_analysis
---
> [!abstract] **Theorem 2**
> 
> If $f$ has a local maximum or minimum at $(a, b)$ and the first-order partial derivatives of $f$ exist there, then $f_x(a, b) = 0$ and $f_y(a, b) = 0$.

## 1 Proof

Let $g(x) = f(x, b)$. If $f$ has a local maximum (or minimum) at $(a, b)$, then $g$ has a local maximum (or minimum) at $a$, so $g'(a) = 0$ by [[Fermat's Theorem(费马引理)]]
But $g'(a) = f_x(a, b)$ and so $f_x(a, b) = 0$. Similarly, by applying [[Fermat's Theorem(费马引理)]] to the function $G(y) = f(a, y)$, we obtain $f_y(a, b) = 0$. 

这样就是很经典的固定一个值成为一元函数来达成降维的目的


---

## 2 几何解释 (Geometric Interpretation)

If we put $f_x(a, b) = 0$ and $f_y(a, b) = 0$ in the equation of a tangent plane, we get $z = z_0$.

Thus, the geometric interpretation of **Theorem 2** is that if the graph of $f$ has a tangent plane at a local maximum or minimum, then the **tangent plane must be horizontal**.

---

## 3 关键定义：临界点 (Critical Point)

> [!info] **Definition**
> 
> A point $(a, b)$ is called a **critical point** (or stationary point) of $f$ if:
> 
> 1. $f_x(a, b) = 0$ and $f_y(a, b) = 0$, **OR**
>     
> 2. One of these partial derivatives does not exist.
>     

**Note:** Theorem 2 says that if $f$ has a local maximum or minimum at $(a, b)$, then $(a, b)$ is a critical point of $f$. However, as in single-variable calculus, **not all critical points give rise to maxima or minima.**