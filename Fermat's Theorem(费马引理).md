---
tags:
  - "#math"
  - math_calculus
---

## 内容
> [!cite] 定理的内容
>如果$f$在$c$处取得极值，并且$f'(c)$存在，那么$f'(c)=0$

## 证明
### 想法

> [!NOTE] 想法
> 由于$f$在$c$处取得极值，并且$f'(c)$存在
> **极值有极大值和极小值两种情况，两种情况的符号规则有些许不一样，不能一概而论，那么就可以分类讨论**

^b36631

### 证明操作
先假设$c$处是**极大值**
根据极值的定义，我们有
$$
\begin{align}
f(c) \ge f(c +h) \qquad \text{(where x approaches 0)}
\end{align}
$$
移项
$$
\begin{align}
f(c)-f(c+h) \ge 0
\end{align}
$$

> [!NOTE] 动机
> 这里我们只有原函数的差，要想往$f'(c)$即导数靠，那么结合极值的定义，将其放大，可以通过构造法构造微分式，除以$h$是一个不错的选择

^b1d8b6

当$h \to 0^{+}$
$$
\begin{align}
\frac{f(c)-f(c+h)}{h} \ge 0  
\Rightarrow \lim_{h \to 0^{+}}{\frac{f(c)-f(c+h)}{h}} \ge 0 
\Rightarrow f'(c) \ge 0
\end{align}
$$
同样的当$h \to 0^{-}$
$$
\begin{align}
\frac{f(c)-f(c+h)}{h} \ge 0 
\Rightarrow \lim_{h \to 0^{+}}{\frac{f(c)-f(c+h)}{h}} \le 0 
\Rightarrow f'(c) \le 0
\end{align}
$$

> [!note] 逻辑
> 这个符号又大于等于，又小于等于的，要想同时满足两个不等式

那么只能是$f'(c)=0$


极小值的证明是同理的，不再叙述