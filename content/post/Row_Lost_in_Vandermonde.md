---
title: "Row Lost in Vandermonde"
date: "2023-11-27"
summary: "一道线性代数习题，Vandermonde Determinant"
math: true
draft: false
categories: 
- math
tags:
- notes
- linear_algebra
---

2023.11.27 week-11 TA class

Supple10 Q3

### Problem

求行列式 $D_{n}$的值（代数表达式）。

$$D_{n} =
\left|
\begin{array}{cccc}
1 & 1 & \dots & 1 \\\\
x_{1} & x_{2} & \dots & x_{n} \\\\
x_{1}^{2} & x_{2}^{2} & \dots & x_{n}^{2} \\\\
\vdots & \vdots & & \vdots \\\\
x_{1}^{n-2} & x_{2}^{n-2} & \dots & x_{n}^{n-2} \\\\
x_{1}^n & x_{2}^n & \dots & x_{n}^n
\end{array}
\right|
$$

思想：补全缺失的行和列

### A simplified example

$$ \begin{vmatrix}
1& 1 & 1 & 1  \\\\
a& b & c & d  \\\\
a^{2}& b^{2} &c^{2}  &d^{2}   \\\\
a^{4}& b^{4} &c^{4}  &d^{4}
\end{vmatrix}$$

Solution:Construct complete *Vandermonde* and compare coefficient.

构造完整范德姆行列式并比较（二项式）系数

$$ \det A=
\begin{vmatrix}
1& 1 & 1 & 1 & 1 \\\\
a& b & c & d &x \\\\
a^{2}& b^{2} &c^{2}  &d^{2} & x^2  \\\\
a^{3}& b^{3} &c^{3}  &d^{3} & x^3  \\\\
a^{4}& b^{4} &c^{4}  &d^{4} & x^4
\end{vmatrix}$$

Now we want to find the minor $M_{25}$ of Matrix A.

Define constant $S = (d-c)(b-d)(d-a)(c-b)(c-a)(b-a)$.

Calculate the Vandermonde determinant and co-factor expansion by column n;

计算范德姆行列式和列 n 的代数余子式

$$\begin{align}
|A| & =S(x-d)(x-c)(x-b)(x-a) \\\\
& =C_{15}+C_{25}x+C_{35}x^{2}+C_{45}x^{3}+C_{55}x^{4} \\\\
\end{align}$$

Compare the coefficient of x:

比较x的系数

$$C_{25}=(-abc-abd-acd-bcd)S$$

So, the original determinant is

$$M_{25}=-C_{25}=(+abc+abd+acd+bcd)S$$

### Solution

$$D_{expansion}=  
\begin{vmatrix} 1 & 1 & \dots& 1 &1\\\\
x_{1} &x_{2} &\dots &x_{n} &y \\\\
x_{1}^{2} &x_{2}^{2} &\dots &x_{n}^{2} &y^2 \\\\
\dots&\dots& &\dots  &\dots \\\\
x_{1}^{n-2} &x_{2}^{n-2} &\dots &x_{n}^{n-2} &y^{n-2}  \\\\
x_{1}^{n-1} &x_{2}^{n-1} &\dots &x_{n}^{n-1} &y^{n-1} \\\\
x_{1}^n &x_{2}^n &\dots &x_{n}^n &y^{n}
\end{vmatrix}
$$

然后按最后一列展开，我们所需要求的$D_{n}$应该会和 n 行 n+1 列（即补充的行和列，对应 $y^{n-1}$ ）的代数余子式有关，因此只看这一项。

将 $D_{e}$ 算两次即可比较得出 $D_{n}$

第一步，按最后一列展开,只看 $y^{n-1}$

$$
(-1)^{n+(n+1)}D_{n}y^{n-1}=-D_{n}y^{n-1}
$$

第二步，根据 **Vandermonde Determinant** 的性质:

（为了方便书写，我们记 $y=x_{n+1}$ ）

$$
D_{e}=\prod_{1\le j < i \le n+1} (x_{i}-x_{j})
$$

我们想要$y^{n-1}$的系数，于是改写为

$$
D_{e}=\left[ \prod_{1\le j < i \le n} (x_{i}-x_{j}) \right] \left[ \prod_{1\le i \le n} (y-x_{i}) \right]
$$

左边方括号为$D_{n}$ ，右边运用二项式定理，得$y^{n-1}$项为

$$
\sum_{i=1}^{n}(-x_i)y^{n-1}
$$

比较即得

$$
-D_{n}=\left[ \prod_{1\le j < i \le n} (x_{i}-x_{j}) \right] \left[ \sum_{i=1}^{n}(-x_i) \right]
$$

$$
D_{n}=\left[ \prod_{1\le j < i \le n} (x_{i}-x_{j}) \right] \left[ \sum_{i=1}^{n}x_i \right]
$$
