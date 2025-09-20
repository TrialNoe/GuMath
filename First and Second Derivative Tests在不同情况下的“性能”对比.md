---
tags:
  - "#math"
  - math_calculus
---

## 例子对比
### 1.0 可以因式分解的有理分式例子
> [!example]
> $$
> f(x) = \frac{x^2}{x-1}
> $$

#### 1.0.1 First derivative Tests
$$
f'(x)=\frac{2x(x-1)-1x^2}{(x-1)^2}=\frac{x^2-2x}{(x-1)^2}=\frac{x(x-2)}{(x-1)^2}
$$


| Interval        | $(x-1)^2$ | $x$ | $x-2$ | $f'(x)$ | $f(x)$     |
| --------------- | --------- | --- | ----- | ------- | ---------- |
| $(- \infty ,0)$ | $+$       | $-$ | $+$   | $-$     | $\swarrow$ |
| $(0,2)$         | $+$       | $+$ | $-$   | $-$     | $\nwarrow$ |
| $(2,\infty)$    | $+$       | $+$ | $+$   | $+$     | $\nwarrow$ |

#### 1.0.2 Second derivative Tests
$$
\begin{align}
f''(x) & =\frac{(2x-2)(x-1)^2-2(x-1)(x^2-2x)}{(x-1)^4} \\
 & =\frac{2(x-1)(x-1)^2-2(x-1)(x^2-2x)}{(x-1)^4} \cdots\cdots 提取公因式 用于约分 \\
 & =\frac{2(x-1)^2-2(x^2-2x)}{(x-1)^3} \\
 & = \frac{2x^2-4x+2-2x^2+4x}{(x-1)^3} \\
 & = \frac{2}{(x-1)^3}
\end{align}
$$

$f'(x)的零点是0,2$,现在进行检验.
$$
\begin{aligned}  
f''(0) &= -2<0 \\
f''(2) &= 2 >0
\end{aligned}
$$

所以说极大值$f(0)=0$，极小值为$f(2)=4$

#### 1.0.3 对比First and Second Derivative Tests

很明显[[First and Second Derivative Tests#First Derivative Tests|First Derivative Tests]]**明显比**[[First and Second Derivative Tests#Second Derivative Tests|Second Derivative Tests]]**,性能要好。究其原因我认为如下
1. 和[[通过导函数分解因式的方法看单调性#1 经典立方差例子]]一样，$f'(x)$已经完成了因式分解，**First Derivative Tests可以直接看出正负**
2. 因为$f'(x)$是一个分式Second Derivative Tests需要计算$f''(x)$，运算量急剧增加，导致很麻烦。