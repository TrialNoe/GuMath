---
tags:
  - "#math"
  - math_calculus
  - Math_source_material
---

> [!question]
> 计算积分
> $$
> \int_{1}^{3} (x^{3}+5x^{2})dx
> $$

先算$\Delta x,\Delta x = \frac{ 3-1 }{ n } = \frac{2}{n}$
再算一下$x_{i} = 1+\frac{2i}{n}$(看起点 不然会错)

$$
\begin{aligned}
\int_{1}^{3} (x^{3} + 5x^{2})dx 
& =  \lim_{ n\to \infty }{ \Delta x \sum_{i=1}^{n} f(x_{i})} \\
& = \lim_{ n\to \infty }{ \frac{2}{n} \sum_{i=1}^{n} \left[ \left(1+\frac{2i}{n}\right)^{3} +5 \left( 1+\frac{2i}{n} \right)^{2} \right] } \\ 
& = \lim_{ n\to \infty }{ \frac{2}{n} \sum_{i=1}^{n} \left[ \left( 1+\frac{6i}{n} + \frac{12i^{2}}{n^{2}} + \frac{8i^{3}}{n^{3}} + 5\left( 1+\frac{4i}{n} + \frac{4i^{2}}{n^{2}} \right) \right) \right]}  \\
& = \lim_{ n\to \infty }{ \frac{2}{n} \sum_{i=1}^{n} \left( 1+\frac{6i}{n} + \frac{12i^{2}}{n^{2}} + \frac{8i^{3}}{n^{3}} + 5 + \frac{20i}{n} + \frac{20i^{2}}{n^{2}} \right) } \\
& = \lim_{ n\to \infty }{ \frac{2}{n} \sum_{i=1}^{n} \left( 6 + \frac{26i}{n} + \frac{32i^{2}}{n^{2}} + \frac{8i^{3}}{n^{3}} \right) } \\
& = \lim_{ n\to \infty }{ \frac{4}{n} \sum_{i=1}^{n} \left( 3 + \frac{13i}{n} + \frac{16i^{2}}{n^{2}} + \frac{4i^{3}}{n^{3}} \right)}
\end{aligned} 
$$
使用一些公式进行求和
$$
\begin{aligned}
&\lim_{ n\to \infty }{ \frac{4}{n} \sum_{i=1}^{n} \left( 3 + \frac{13i}{n} + \frac{16i^{2}}{n^{2}} + \frac{4i^{3}}{n^{3}} \right)} \\
& = \lim_{ n\to \infty }{ \frac{4}{n} \left[ 3n + \frac{13}{n}\left( \frac{n(n+1)}{2} \right) + \frac{16}{n^{2}}  \frac{n(n+1)(2n+1)}{6}  + \frac{4}{n^{3}}\left( \frac{n(n+1)}{2} \right)^{2} \right] } \\
& = \lim_{ n \to \infty }{ \frac{4}{n} \left[ 3n  + \frac{13n+13}{2}  + \frac{11\left( 1+\frac{1}{n} \right)(2n+1)}{3} + \frac{4}{n}\frac{(n+1)^{2}}{4} \right]} \\
& = \lim_{ n\to \infty }{ \left[ \frac{4}{n} \cdot 3n + \frac{4}{n} \cdot \frac{13n+13}{2} + \frac{4}{n} \cdot \frac{11\left( 1+\frac{1}{n} \right)(2n+1)}{3} + \frac{4}{n} \cdot \frac{4}{n} \cdot \frac{(n+1)^{2}}{4} \right] } \quad\text{这种时候你就不要跳步了}\\
& = \lim_{ n\to \infty }{ \left[ \frac{12}{n} + \frac{26}{n}+26 + \frac{32\left( 1+\frac{1}{n} \right)\left( 2+\frac{1}{n} \right)}{3}+4\left( 1+\frac{1}{n} \right)^{2} \right] } \\

\end{aligned}
$$