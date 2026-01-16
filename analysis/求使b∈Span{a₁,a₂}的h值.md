---
tags:
  - "#math"
  - math_advanced_algebra
---

> [!question] 
> 找一个$h$使得$\vec{b}$在$Span \{\vec{a_1},\vec{a_2}\}$里面
> $$
> \vec{a_1} = \begin{bmatrix}
> 1 \\ 4 \\ -2
> \end{bmatrix}\ 
> \quad
> \vec{a_2}=\begin{bmatrix}
> -2 \\ -3 \\ 7
> \end{bmatrix}\ 
> \quad
> \vec{b}=\begin{bmatrix}
> 4 \\
> 1 \\
> h
> \end{bmatrix}
> $$

> [!NOTE] 想法
> 根据线性方程组和Span的联系，$\vec{b}$在$Span\{\vec{a_1},\vec{a_2}\}$里面，那么augumented matrix:$[\vec{a_1} \ \vec{a_2} \ \vec{b}]$ 一定有解(有几个不知道)
通过[[高斯消元法 Gaussian Elimination]]进行Row简化，可以得到二行Prior与第三行Prior相同


$$
\
\begin{bmatrix}
1 & -2 & 4 \\
4 & -3 & 1 \\
-2 & 7 & h
\end{bmatrix}
\
\
\sim
\begin{bmatrix}
1 & -2 & 4 \\
4 & -3 & 1 \\
0 & 3 & h+8
\end{bmatrix}
\sim
\begin{bmatrix}
1 & -2 & 4 \\
0 & 5 & -15 \\
0 & 3 & h+8
\end{bmatrix}
\sim
\begin{bmatrix}
1 & -2 & 4 \\
0 & 3 & -9 \\
0 & 3 & h+8
\end{bmatrix}
$$
成立
$$
\begin{align}
h+8 = -9\\
h=-17
\end{align}
$$
