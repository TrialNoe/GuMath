---
tags:
  - "#math"
  - math_
---

尝试进行证明
$$
1^{2}+2^{2}+3^{2}+\dots +n^{2} = \frac{n(n+1)(n+2)}{6}
$$


Pascal对这个进行了证明
原理使用更高次的展开式里面含有低次的
$$
\begin{align}
(k+1)^{3} = k^{3}+3k^{2}+3k+3 \\
(k+1)^{3} - k^{3} = 3k^{2}+3k +3 \\
\end{align}

$$





$$
A_{n} = \frac{1}{n}f\left( \frac{1}{n} \right) + \frac{1}{n}f\left( \frac{2}{n} \right) +\frac{1}{n} f\left( \frac{3}{n} \right)+ \dots +\frac{1}{n}f(1)
$$
```c

    const double N = 1000000;
    double count = 1 / N,
           x = 0,
           area = 0;
    // y=x^2计算[0,1]的面积
    for (int i = 0; i < N; i++)
    {
        x += count;
        area += count * (x * x);
    }
    printf("%lf", area);
    return 0;
```


