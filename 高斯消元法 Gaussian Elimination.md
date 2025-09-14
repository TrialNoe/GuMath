---
tags:
  - "#math"
  - math_ideas_tools
  - math_advanced_algebra
---

> [!NOTE] 方法介绍
> 使用高斯消元法可以通解一般的增广矩阵，解法是程序化的，无脑的。
## 流程-例子
> [!NOTE] Template
> 因为流程是固定的，相当于一个模板，压根就不用很多例子就能总结出来
> 该方法的步骤如下:
> 第一步用第一行的倍数去减其他行
> 第二步用第二行的倍数去减其他行
> ....
> 最后代入消元
> 

在运算过程中遵循对调化简，约分原则，见：[[通过对换，约分简化高斯求解的计算量]]


### 例子:
解下列线性方程组
$$
A=
\begin{pmatrix}
1 & -3 & -2 & 3\\
-2 & 1 & -4 & -9\\
-1 & 4 &-1 & -7
\end{pmatrix}
$$
$$
\begin{align}
\begin{pmatrix}
1 &0 &0\\
2 &1 &0\\
1 &0 &1 
\end{pmatrix}
\begin{pmatrix}
1 & -3 & -2 & 3\\
-2 & 1 & -4 & -9\\
-1 & 4 &-1 & -7
\end{pmatrix}
=
\begin{pmatrix}
1 & -3 & -2 & 3\\
0 & -5 & -8 & -3\\
0 & 1  & -3 & -4
\end{pmatrix}
\end{align}
$$
$$
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}
\begin{pmatrix}
1 & -3 & -2 & 3\\
0 & -5 & -8 & -3\\
0 & 1  & -3 & -4
\end{pmatrix}
=
\begin{pmatrix}
1 & -3 & -2 & 3\\
0 & -5 & -8 & -3\\
0 &  0 & -23 & -23
\end{pmatrix}
=
\begin{pmatrix}
1 & -3 & -2 & 3\\
0 & -5 & -8 & -3\\
0 &  0 & 1 & 1
\end{pmatrix}
$$
代回消元
$$
\begin{pmatrix}
1 & -3 & -2 & 3\\
0 & -5 & -8 & -3\\
0 &  0 & 1 & 1
\end{pmatrix}
=
\begin{pmatrix}
1 & 0 & 0 & 2\\
0 & 1 & 0 & -1\\
0 &  0 & 1 & 1
\end{pmatrix}
$$
## 小技巧
我们在[[通过对换，约分简化高斯求解的计算量]]中发现两个小规律：
1. 在Prior系数为1是操作是更简便的。
2. 数据小往往比数据大好算得多得多