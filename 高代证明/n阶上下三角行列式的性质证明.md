---
tags:
  - "#math"
  - math_advanced_algebra
---
%% 先来一个可以随便复制的上下三角行列式
n阶行列式
$$
\left[
\begin{array}{ccc}
 & a_{11}, & a_{12}, & a_{13},  & \cdots   &   a_{1n} \\
 & a_{21}, & a_{22}, & a_{23}, & \cdots & a_{2n} \\
 & a_{31}, & a_{32}, & a_{33}, & \cdots & a_{3n} \\
 & \vdots & \vdots & \vdots & \ddots & \vdots\\
 & a_{n1}, & a_{n2}, & a_{n3}, & \cdots &  a_{nn}
\end{array}
\right]
$$
上三角行列式
$$
\left[
\begin{array}{ccc}
 & a_{11}, & a_{12}, & a_{13},  & \cdots   &   a_{1n} \\
 & 0, & a_{22}, & a_{23}, & \cdots & a_{2n} \\
 & 0, & 0, & a_{33}, & \cdots & a_{3n} \\
 & \vdots & \vdots & \vdots & \ddots & \vdots\\
 & 0, & 0, & 0, & \cdots &  a_{nn}
\end{array}
\right]
$$
下三角行列式
$$
\left[
\begin{array}{ccc}
 & a_{11},  & 0, & 0, & \cdots & 0 \\
 & a_{21}, & a_{22}, & 0, & \cdots & 0\\
 & a_{31}, & a_{32}, & a_{33}, & \cdots & a_{3n} \\
 & \vdots & \vdots & \vdots & \ddots & \vdots\\
 & a_{n1}, & a_{n2}, & a_{n3}, & \cdots &  a_{nn}
\end{array}
\right]
$$
%%


## 值的性质的证明：等于对角线的乘积
### 对上三角行列式进行证明
$$
\left[
\begin{array}{ccc}
 & a_{11}, & a_{12}, & a_{13},  & \cdots   &   a_{1n} \\
 & 0, & a_{22}, & a_{23}, & \cdots & a_{2n} \\
 & 0, & 0, & a_{33}, & \cdots & a_{3n} \\
 & \vdots & \vdots & \vdots & \ddots & \vdots\\
 & 0, & 0, & 0, & \cdots &  a_{nn}
\end{array}
\right]
$$
$$
\begin{align}
|A|  & = a_{11}\cdot A_{11}+0\cdot A_{21}+\dots+0\\ 
 & =a_{11\cdot}A_{11}
\end{align}
$$
我们看一下Algebra Cofactor$A_{11}$，去掉$a_{11}$之后不就是一个$n-1$阶上三角行列式吗？？
$$
|A_{11}| = a_{22}\cdot A^{'}_{22}
$$
那$A^{'}_{22}$肯定是一个$n-2$阶的上三角行列式了，一直做到$1$阶行列式只剩$a_{nn}$
由归纳假设可以知道$$|A|=a_{11}\cdot a_{22}\cdot a_{33}\cdot \dots \cdot a_{nn}$$

### 2.对下三角行列式进行证明
$$
\left[
\begin{array}{ccc}
 & a_{11},  & 0, & 0, & \cdots & 0 \\
 & a_{21}, & a_{22}, & 0, & \cdots & 0\\
 & a_{31}, & a_{32}, & a_{33}, & \cdots & a_{3n} \\
 & \vdots & \vdots & \vdots & \ddots & \vdots\\
 & a_{n1}, & a_{n2}, & a_{n3}, & \cdots &  a_{nn}
\end{array}
\right]
$$
$$
|A| = a_{11}\cdot A_{11}+a_{21}\cdot A_{21}+a_{31}\cdot A_{31}\dots+a_{n1}\cdot A_{n1}
$$
对于一个代数余子式
$$
A_{ij} = (-1)^{i+j}M_{ij}
$$
考虑$M_{k1}(1\leq k\leq n)$
假设这个行列式这么表示：$M_{k1}=(b_{ij})_{(n-1),(n-1)}$(说的是这是一个n-1,n-1的矩阵)
这里有点难懂
![[上下三角行列式性质证明1.png]]
$$
b_{ij} = 
\left\{
\begin{align}
 & a_{i,j+1}, & 1< i <k \\
 & a_{i+1,j+1}, & k<i<n-1
\end{align}
\right.
$$
由原来的下三角行列式我们可以知道**当$i<j$行指标小于列指标的时候**,$a_{ij}=0$那么$a_{i,j+1}<0,a_{i+1,j+1}<0\Rightarrow b_{ij}=0$
落下来的时候肯定有主对角线上的元肯定有等于0的
简单证明一下当$k\geq2$的时候,$M_{k1}$相当于是把原来的$\det(A)$去掉了第一行
肯定有一个
$$
b_{ij} = b_{k-1,k} = 0
$$
道理和[[n阶上下三角行列式的性质证明#对上三角行列式进行证明]]是一样的
$$
|A| = a_{11}\cdot A_{11} = a_{11}\cdot a_{22}\cdot a_{33}\cdot \dots \cdot a_{nn}
$$