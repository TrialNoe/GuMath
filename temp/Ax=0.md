---
tags:
  - "#math"
---

> [!question]
> Find all $\mathbf{x}$ in $\mathbb{R}^{ 4 }$ that are mapped into the zero vector $\vec{0}$ by the transformation $\mathbf{x} \mapsto A\mathbf{x}$ for the given matrix $A$.
> $$
> A = \left[
> \begin{matrix}
> 1 & -4 & 7 & -5  \\
> 0 & 1 & -1 & 3 \\
> 2 & -6 & 6 & -4 
> \end{matrix}
> \right]
> $$
> 

> [!tip]+
> 想法是既然是一个linear transformation的话，对于这一大批符合条件的$\mathbf{x}$都可以满足条件$A\mathbf{x}=\mathbf{0}$，只要解出来条件就行了，那么可以想到去做[[Row Reduce及其技巧]]

$$
Given = 
\left[
\begin{matrix}
1 & 0 & -9 & 7 \\
0 & 1 & -4 & 3 \\
0 & 0 & 0 & 0
\end{matrix}
\right]
$$ 
通常会利用？？？进行表示
$$
RHS = 
\left\{
\begin{aligned}
&x_{1}=-9x_{3}+5x_{4} \\
&x_{2}=4x_{3}-3x_{4} \\
&x_{3},x_{4}\text{ is free}
\end{aligned}
\right.
$$
So
$$
\mathbf{x}=x_{3}\left[\begin{matrix}-9\\4\\1\\0\end{matrix}\right]+x_{4}\left[\begin{matrix}-7\\-3\\0\\1\end{matrix}\right]
$$

