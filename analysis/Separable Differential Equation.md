---
tags:
  - "#math"
  - math_calculus
---
一阶导函数来求原函数
利用了这个等价表达**Lagrange notation & Leibniz notation**不同的表述
$$
y'  = \frac{dy}{dx}
$$
^LagrangeLeibnizNotation

## 1 First-Order differential Equation
在这里更多是利用了这个核
$$
\frac{dy}{dx} = \frac{f(x)}{h(\mathbf{y})}
$$

> [!warning] 有反例
> 根据[[Separable Differential Equation#简单的反例]]进行补充，$\frac{1}{f(x)}\neq0\,\&\,\frac{1}{g(y)\neq0}$才能交叉相乘，不然的话可以直接
> 有$y=0$这样的解

进行交叉之后
$$
\begin{aligned}
g(\mathbf{y})\,dy = f(x)\,dx \\
\end{aligned}
$$
两边进行积分
$$
\int g(y)\,dy = \int f(x)\,dx
$$


### 1.1 简单的例子

> [!example] 解微分方程
> $$
> y' = \frac{x^{ 2 }}{y^{ 2 }}
> $$

根据[[Separable Differential Equation#^LagrangeLeibnizNotation]]，我们可以写作
$$
\begin{align}
\frac{dy}{dx} = &\frac{ x^{ 2 } }{ y^{ 2 } } \implies
y^{ 2 }\,dy = x^{ 2 }\,dx \implies
\int{y^{ 2 }\,dy }= \int{x^{ 2 }\,dx} 
\end{align}
$$
$$
\begin{align}
y^{ 3 }&=x^{ 3 }+C
\end{align}
$$
只能是一阶使用吗？？


## 2 Test for Second-Order Differential Eqn
不妨来一个

> [!note] Thinking
> $$
> \frac{d^{ 2 }y}{dx^{ 2 }} = \frac{f(x)}{g(y)}
> $$

仿照如上进行交叉

> [!error]
> $$
> g(y)\,d^{ 2 }y = f(x)\,d^{ 2 }x
> $$
> 这样做本身时不合法的，**只有在一阶时才具有“类分数”的操作灵活性。**
> So 只能在一阶使用

## 3 简单的反例

> [!warning]
> $$
> \frac{dy}{dx} = y
> $$

如果我们按照前面的去做
$$
\frac{1}{y}\, dy = dx \implies \ln|y| = x +C
$$
但是很明显如果$y=0$这个函数$\frac{dy}{dx} = 0$，$0=0$也是一个解，怎么就莫名其妙丢解了呢？？
原因是这个交叉相乘是有风险的$\frac{1}{y}$不一定成立

