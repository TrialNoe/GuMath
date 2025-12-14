---
tags:
  - "#math"
  - math_advanced_algebra
---

> [!NOTE] 
> 除了$m^2$的matrix和$m$维的向量相乘，$m \times n$的matrix和$m$维向量相乘也是符合[[Linear Combination]]的

## 1.例子
### 1.1.例子1

$$
\begin{bmatrix}
1 & 5 & -2 & 0 \\
-3 & 1 & 9 & -5 \\
4 & -8 & -1 & 7 \\
\end{bmatrix}
\begin{bmatrix}
3\\-2\\0\\-4\\
\end{bmatrix}
=
\begin{bmatrix}
-7 \\
9 \\
0 \\
\end{bmatrix}
$$

> [!NOTE] 动机
> 根据[[Linear Combination]]，可以将$matrix \times vector$看成是$vector \ equation$
> $$
> 3
> \begin{bmatrix}
> 1 \\
> -3 \\
> 4
> \end{bmatrix}
> -2
> \begin{bmatrix}
> 5 \\
> 1 \\
> -8
> \end{bmatrix}
> +0
> \begin{bmatrix}
> -2 \\
> 9 \\
> -1
> \end{bmatrix}
> -4
> \begin{bmatrix}
> 0 \\
> -5 \\
> 7
> \end{bmatrix}
> =
> \begin{bmatrix}
> -7 \\
> 9 \\
> 0
> \end{bmatrix}
> $$
> 
> 


### 1.2.例子2:不适用
$$
\begin{bmatrix}
2 \\
6 \\
-1
\end{bmatrix}
\begin{bmatrix}
5 \\
-1
\end{bmatrix}
$$

> [!Warning]
> 这种是乘不了的，一个$3 \times 1$的matrix不能和一个$R^2$相乘，3行怎么乘2个entires

