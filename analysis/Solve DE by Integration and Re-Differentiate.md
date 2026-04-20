---
tags:
  - "#math"
  - math_calculus
  - math_ideas_tools
---
## 1 Understand
在first order DE中无论是[[Linear Differential Equation]]还是[[Separable Differential Equation]]最终都还是要进行积分消除$\frac{ dy }{ dx }$
而[[Linear Differential Equation]]利用的是**导数乘法法则**，[[Separable Differential Equation]]是利用了**方程的性质&微积分基本定理**


## 2 导数乘法法则



## 3 除法法则
既然这样是是不是还能利用**导数除法法则，链式法则**做一些事情呢？？


### 3.1 具体构造思考
我们先从导数的除法法则出发
$$
\left[ \frac{f(x)}{g(x)} \right]' = \frac{ f'(x)g(x)-g'(x)f(x) }{ g^{ 2 }(x) }
$$
仿照[[Linear Differential Equation#由导数乘法公式构造？]]
$$
\frac{dy}{dx} = \frac{ f'(x)g(x)-g'(x)f(x) }{ g^{ 2 }(x) }
$$
变成方程形式
$$
\frac{dy}{dx} = Q(x)
$$
$$
\frac{ f'(x)g(x)-g'(x)f(x) }{ g^{ 2 }(x) } = Q(x)
$$
得到这个东西
$$
f'(x)g(x)-g'(x)f(x) = Q(x)g^{ 2 }(x)
$$
是否可以做一下其他处理

$$
f'(x)-\frac{g'(x)}{g(x)}f(x) = Q(x)g(x)
$$
但是这样处理会出现[[Separable Differential Equation#1st-order DE的反例]]的问题，所以如果$g(x) = 0$也是成立的
换一种写法
$$
\frac{dy}{dx}-\frac{g'(x)}{g(x)}y = Q(x)g(x)
$$
这不是??
$$
\frac{dy}{dx} + P(x)y = Q(x)
$$
怎么这么像的


### 3.2 和Bernoulli Differential Equation的练习
仔细一看，除法公式不就是[[Linear Differential Equation#Bernoulli Differential Equation]]的时候，$n=2$的情况
![[Linear Differential Equation#^BDEByUSub]]

