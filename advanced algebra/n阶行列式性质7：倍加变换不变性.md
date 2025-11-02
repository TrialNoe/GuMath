---
tags:
  - "#math"
  - math_advanced_algebra
---
## 0.内容
$$
\begin{aligned}
& \left|
\begin{array}{ccc}
a_{11} & \cdots  & a_{r1} & \cdots & a_{s1}+ ca_{r1}& \cdots  & a_{n1} \\
a_{21}  & \cdots & a_{r2} & \cdots  & a_{s2}+ca_{r2}& \cdots & a_{n2} \\
\vdots  & \ddots  & \vdots & \ddots & \vdots  & \ddots & \vdots\\
a_{n1} & \cdots & a_{rn} & \cdots & a_{sn}+ca_{rn} & \cdots &  a_{nn}
\end{array}
\right|
 \\ \\ =& 
\left|
\begin{array}{ccc}
a_{11} & \cdots  & a_{r1} & \cdots & a_{s1}& \cdots  & a_{n1} \\
a_{21}  & \cdots & a_{r2} & \cdots  & a_{s2}& \cdots & a_{n2} \\
\vdots  & \ddots  & \vdots & \ddots & \vdots  & \ddots & \vdots\\
a_{n1} & \cdots & a_{rn} & \cdots & a_{sn} & \cdots &  a_{nn}
\end{array}
\right|
\end{aligned}
$$

## 1.证明

> [!thinking]+
> 有一行是成比例的，又学了拆分法，刚好都能用得上。


由拆分法（[[n阶行列式性质6(拆分法)：行列式的（列）线性可加性质]]）
$$
\begin{aligned}
& \quad
\left|
\begin{array}{ccc}
a_{11} & \cdots  & a_{r1} & \cdots & a_{s1}+ ca_{r1}& \cdots  & a_{n1} \\
a_{21}  & \cdots & a_{r2} & \cdots  & a_{s2}+ca_{r2}& \cdots & a_{n2} \\
\vdots  & \ddots  & \vdots & \ddots & \vdots  & \ddots & \vdots\\
a_{n1} & \cdots & a_{rn} & \cdots & a_{sn}+ca_{rn} & \cdots &  a_{nn}
\end{array}
\right| \\ \\
&=
\left|
\begin{array}{ccc}
a_{11} & \cdots  & a_{r1} & \cdots & a_{s1}& \cdots  & a_{n1} \\
a_{21}  & \cdots & a_{r2} & \cdots  & a_{s2}& \cdots & a_{n2} \\
\vdots  & \ddots  & \vdots & \ddots & \vdots  & \ddots & \vdots\\
a_{n1} & \cdots & a_{rn} & \cdots & a_{sn} & \cdots &  a_{nn}
\end{array}
\right|
+
\left|
\begin{array}{ccc}
a_{11} & \cdots  & a_{r1} & \cdots &  ca_{r1}& \cdots  & a_{n1} \\
a_{21}  & \cdots & a_{r2} & \cdots  & ca_{r2}& \cdots & a_{n2} \\
\vdots  & \ddots  & \vdots & \ddots & \vdots  & \ddots & \vdots\\
a_{n1} & \cdots & a_{rn} & \cdots & ca_{rn} & \cdots &  a_{nn}
\end{array}
\right|
\\ \\ 
&=  \left|
\begin{array}{ccc}
a_{11} & \cdots  & a_{r1} & \cdots & a_{s1}& \cdots  & a_{n1} \\
a_{21}  & \cdots & a_{r2} & \cdots  & a_{s2}& \cdots & a_{n2} \\
\vdots  & \ddots  & \vdots & \ddots & \vdots  & \ddots & \vdots\\
a_{n1} & \cdots & a_{rn} & \cdots & a_{sn} & \cdots &  a_{nn}
\end{array}
\right| 
+ 0 \\ \\
& = \left|
\begin{array}{ccc}
a_{11} & \cdots  & a_{r1} & \cdots & a_{s1}& \cdots  & a_{n1} \\
a_{21}  & \cdots & a_{r2} & \cdots  & a_{s2}& \cdots & a_{n2} \\
\vdots  & \ddots  & \vdots & \ddots & \vdots  & \ddots & \vdots\\
a_{n1} & \cdots & a_{rn} & \cdots & a_{sn} & \cdots &  a_{nn}
\end{array}
\right|
\end{aligned}
$$
