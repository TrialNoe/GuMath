---
tags:
  - "#math"
  - math_advanced_algebra
---
# 垂直性质的使用


> [!question] 证明
> $$
> (\mathbf{a}\times \mathbf{b}) \cdot \mathbf{b} = 0
> $$

我们知道如果两个向量相互垂直的话，他们的Dot Product为0

> [!tip]
> **又根据Cross Product的几何含义就是找到一个与原来的向量Span相互垂直的向量**

那么我们可以假设求出来的
$$
\mathbf{a}\times \mathbf{b} = \mathbf{n}
$$
根据几何含义
$$
\mathbf{n} \cdot \mathbf{b} = 0
$$


## 1 利用面积性质进行简单证明
$$
c \mathbf{a}\times \mathbf{b} = c(\mathbf{a}\times \mathbf{b}) = a \times(c \mathbf{b})
$$
根据这个
$$
c \mathbf{a} \times \mathbf{b} = |c\mathbf{a}||\mathbf{b}|\sin\alpha 
$$




$$
c(\mathbf{a}\times \mathbf{b})  = c|a||b|\sin\beta
$$


$$
a \times(c \mathbf{b}) = |a||c \mathbf{b}|\sin\gamma 
$$

如果说$c$是一个正数，那刚好，只是有其中一个向量进行了伸缩变换，不改变角度$\alpha = \beta = \gamma$。
如果说$c$是一个负数，那绝对值出来一个符号，三角函数那里也差了一个负号，也是刚好全部相等抵消了。


## 2 不好用的情况

> [!question]
> $$
> \vec{a} \times (\vec{b}+\vec{c}) = \vec{a}\times\vec{b}+\vec{a}\times \vec{c}
> $$

如果是仿照前面[[#垂直性质的使用]]的话，我们会假设
$$
\vec{a} \times (\vec{b}+\vec{c}) = \vec{n}
$$

> [!fail]
> 但是这里$\vec{b}+\vec{c}$创造出了一个新的向量，假设为$\vec{d}$
> 我们知道$\vec{n}\cdot \vec{a}=0,\vec{n}\cdot \vec{d} = 0$
> 再看右边呢，两个Cross Product，创造出了两个新的法向量假设说是$\vec{m_{1}},\vec{m_{2}}$，然后他们一加又来一个新的$\vec{m}=\vec{m_{1}}+\vec{m_{2}}$
> 这么多新的向量你怎么去找他们之间的关系？
> 总的来说创造出一个以上的向量就gg了
> 

我们更好用的方法是直接用Determinant进行计算,过程懒得抄了。。