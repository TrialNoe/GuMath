---
tags:
  - "#math"
  - math_calculus
  - math_ideas_tools
---

## 表示方法
$$
f(x)=
f(x_{0})
+(x-x_{0})^1\frac{f'(x_{0})}{1!}
+(x-x_{0})^2\frac{f^{(2)}(x_{0})}{2!}
+(x-x_{0})^3\frac{f^{(3)}(x_{0})}{3!}
+\dots 
+(x-x_{0})^n\frac{f^{(n)}(x_{0})}{n!}
$$
使用Sigma notation就是
$$
f(x) = \sum ^{N}_{n=1} {(x-x_{0})^{n}\frac{f^{(n)}(x_{0})}{n!}}
$$
## 与Linear Approximation的关系

[[Linear Approximation]]是[[Taylor Polynomial]]的特例即$n=1$时的情况