---
tags:
  - "#math"
---
## 1 Introduction to Directional Derivative
一元函数中我们也有类似的导数，导数（变化率）可以衡量 在某个点处 函数的变化快慢。

类似的在 多元函数中 我们也需要这样的工具 来衡量函数的变化情况，但是又带来了一个问题**不同方向的导数是无法比较norm的**。

但是我们可以回顾 对于二元函数$z=f(x,y)$，计算他的变化率的话，可以用$\frac{\Delta z}{h}$，因此我们希望的是对于任意一个一个$n$元函数，引入一个新的维度$m$，使得
$$x_{m}=f(\vec{x}), rate=\lim_{ h \to \infty }\frac{ f(\vec{x_{1}}) - f(\vec{x_{2}}) }{ h }=\lim_{ h \to \infty }\frac{\Delta x_{m}}{h}$$
![[Snipaste_2026-05-30_18-49-09.png]]




## 2 参考资料
1. James Stewart, Daniel K. Clegg, Saleem Watson - Instructor’s Solutions Manuals for Calculus Early Transcendentals 9th Edition