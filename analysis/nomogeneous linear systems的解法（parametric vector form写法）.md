---
tags:
  - "#math"
  - math_advanced_algebra
---
解法
![[Pasted image 20250928221649.png]]
## 1.例子
### 1.1.例子1
> [!question]
> $$
> \begin{flalign}
> \begin{bmatrix}  
> 1 & 3 & -5 & 0 \\
> 1 & 4 & -8 & 0 \\
> -3 & -7 & 9 & 0
> \end{bmatrix}
> \end{flalign}
> $$
> 

直接硬解，边写边注释
$$
\begin{align} 
\sim
\begin{bmatrix}
1 & 3 & -5  & 0 \\
0 & 1 & -3 & 0  \\
0 & 1 & -3 & 0
\end{bmatrix} 
\sim 
\begin{bmatrix}
1 & 3 & -5 & 0 \\
0 & 1 & -3 & 0 \\
0 & 0 & 0 & 0
\end{bmatrix} 
\end{align}
$$
这里注意到$x_{3}$是自由元，要表示成$x_{3}$的parametric vector，继续用$row 2$消去$row 1$的$x_{3}$就好了
$$
\sim
\begin{align} 
\begin{bmatrix}
1 & 0 & 4 & 0 \\
0 & 1 & -3 & 0 \\
0 & 0 & 0 & 0
\end{bmatrix}
\end{align}
$$
然后$x_{3}$的位置全部取相反数
所以说就有
$$
\vec{x}=x_{3}
\begin{bmatrix}
-4 \\
3 \\
1
\end{bmatrix}
$$

### 1.2.例子2
