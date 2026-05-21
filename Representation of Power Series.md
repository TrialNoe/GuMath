## 1 T0
> [!question]
> $$
> f(x) = \frac{x}{1+x}
> $$

$$
\frac{x}{1+x} =  \frac{ 1+x  - 1 }{ 1+x } = 1 - \frac{1}{1- (-x)} = 1 - \sum^{\infty}_{n=0} (-1)^{ n }x^{ n }
$$

还有一种提出$x$的做法，相当于幂级数整体乘以$x$，等于每一项都乘上$x$
$$
f(x) = x \frac{ 1 }{ 1-(-x) } = x \sum^{\infty}_{n=0} (-x)^{ n } = \sum^{\infty}_{n=0} (-1)^{ n }x^{ n+1 }
$$
$\left\lvert x \right\rvert<1\implies-1<x<1$





## 2 T1
来个难度大的
$$
f(x) = \frac{x+a}{x^{ 2 }+a^{ 2 }} (a>0)
$$


$$
f(x) = (x+a) \frac{1}{x^{ 2 }+a^{ 2 }}
$$
这个常数要变成1才能满足需求

$$
RHS = \frac{ x+a }{ a^{ 2 } } \frac{1}{1 - \left[ -\left( \frac{x}{a} \right)^{ 2 } \right]} = \frac{ x+a }{ a^{ 2 } } \sum^{\infty}_{n=} (-1)^{ n }\left( \frac{x}{a} \right)^{ 2n }
$$

所以
$$
\left\lvert \left( \frac{x}{a} \right)^{ 2 } \right\rvert < 1\implies -a < x < a  
$$


