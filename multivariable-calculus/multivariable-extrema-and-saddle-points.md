---
title: Multivariable Extrema and Saddle Points
source: https://algebrica.org/multivariable-extrema-and-saddle-points/
license: CC BY-NC 4.0
tags:
  - extrema
  - hessian-matrix
  - multivariable-calculus
  - saddle-point
  - second-derivative-test
---

## Local and global extrema

Let $A\subseteq\mathbb{R}^n$ be open and let $f:A\to\mathbb{R}$. A point $a\in A$ is a local maximum of $f$ if there is $r>0$ such that

$$f(x)\le f(a) \qquad\text{for every }x\in A\cap B(a,r)$$

where $B(a,r)$ is the open ball of radius $r$ centred at $a$. The point is a strict local maximum if the inequality is strict for every $x\neq a$ in that ball. A local minimum is defined by reversing the inequality, and a local extremum is either a local maximum or a local minimum. The point is a global maximum, or absolute maximum, if $f(x)\le f(a)$ for every $x\in A$; global minima are defined analogously. A global extremum at an interior point is necessarily local, but a local extremum need not be global.

The distinction between interior and boundary points is essential. The definitions above use a full ball around $a$, so they apply to interior points of the domain. If $f$ is defined on a set with boundary, a point of the boundary can be the location of a global extremum without being a local extremum in the sense of the full ball. The search for extrema therefore has two separate parts: interior critical points and the boundary.

For a function of one variable, a local extremum at an interior point forces the derivative to vanish. The same argument applies in each coordinate direction.

## Critical points

Let $f$ be defined on an open set containing $a$. The point $a$ is a critical point of $f$ if $\nabla f(a)=0$, or if at least one of the first partial derivatives of $f$ does not exist at $a$. A critical point at which the gradient exists and vanishes is also called a stationary point.

+ **Fermat's theorem for several variables.** Let $f$ be defined on an open set containing $a$ and differentiable at $a$. If $f$ has a local extremum at $a$, then $\nabla f(a)=0$.

The proof reduces the statement to one variable. Fix a coordinate direction $e_i$ and define

$$g(t)=f(a+te_i)$$

for $t$ in a small interval around $0$. Since $a$ is an interior point and $f$ has a local extremum at $a$, the function $g$ has a local extremum at $0$. It is differentiable at $0$, with $g'(0)=\partial f/\partial x_i(a)$. Fermat's theorem in one variable gives $g'(0)=0$, hence $\partial f/\partial x_i(a)=0$. Repeating this for $i=1,\ldots,n$ gives $\nabla f(a)=0$.

The converse is false. The function $f(x,y)=xy$ has $\nabla f(0,0)=(0,0)$, but $f$ takes both positive and negative values in every neighbourhood of the origin: $f(t,t)=t^2>0$ and $f(t,-t)=-t^2<0$ for $t\neq0$. The origin is neither a local maximum nor a local minimum. A critical point of this kind is a saddle point.

A saddle point is a critical point at which the function is neither a local maximum nor a local minimum. Equivalently, every neighbourhood of the point contains points at which $f$ is larger than $f(a)$ and points at which $f$ is smaller. The term describes the graph of $z=x^2-y^2$: along the $x$-axis the surface rises from the origin, and along the $y$-axis it falls.

Fermat's theorem shows that differentiability moves every interior local extremum into the list of critical points. It does not distinguish maxima from minima, and it does not say that every critical point is an extremum. The second derivatives supply that information when they are available.

## The second derivative test

Let $f$ be of class $C^2$ on an open set $A\subseteq\mathbb{R}^n$ and let $a\in A$ be a critical point. The Hessian matrix at $a$ is the symmetric matrix

$$H_f(a)=\left(\frac{\partial^2 f}{\partial x_i\partial x_j}(a)\right)_{i,j=1}^{n}$$

A symmetric matrix is positive definite if $h^{T}Hh>0$ for every nonzero $h\in\mathbb{R}^n$, negative definite if $h^{T}Hh<0$ for every nonzero $h$, and indefinite if the quadratic form takes both positive and negative values. Equivalently, the matrix is positive definite when all its eigenvalues are positive, negative definite when all are negative, and indefinite when it has eigenvalues of both signs.

The second-order Taylor expansion, proved in the entry on [multivariable Taylor expansions](../multivariable-taylor-expansions/), gives

$$f(a+h)=f(a)+\nabla f(a)\cdot h+\frac{1}{2}h^{T}H_f(a)h+o\bigl(\lVert h\rVert^2\bigr) \qquad h\to0 \tag{1}$$

Since $\nabla f(a)=0$, the sign of $f(a+h)-f(a)$ for small nonzero $h$ is controlled by the quadratic term, provided that term does not vanish.

+ **Second derivative test.** Let $f$ be of class $C^2$ near a critical point $a$.
+ If $H_f(a)$ is positive definite, then $a$ is a strict local minimum.
+ If $H_f(a)$ is negative definite, then $a$ is a strict local maximum.
+ If $H_f(a)$ is indefinite, then $a$ is a saddle point.
+ If $H_f(a)$ is positive semidefinite or negative semidefinite with a zero eigenvalue, the test is inconclusive.

The definite cases follow from the eigenvalues. Suppose that $H=H_f(a)$ is positive definite, and let $\lambda_1>0$ be its smallest eigenvalue. For every $h$,

$$h^{T}Hh\ge\lambda_1\lVert h\rVert^2$$

By the definition of the little-o term, for every $\varepsilon>0$ there is $\delta>0$ such that

$$\bigl|f(a+h)-f(a)-\tfrac{1}{2}h^{T}Hh\bigr|\le\varepsilon\lVert h\rVert^2 \qquad\text{whenever }\lVert h\rVert<\delta$$

Choose $\varepsilon=\lambda_1/4$. Then, for $0<\lVert h\rVert<\delta$,

$$f(a+h)-f(a)\ge\frac{\lambda_1}{2}\lVert h\rVert^2-\frac{\lambda_1}{4}\lVert h\rVert^2=\frac{\lambda_1}{4}\lVert h\rVert^2>0$$

Hence $f(a+h)>f(a)$ for every sufficiently small nonzero $h$, and $a$ is a strict local minimum. Applying the same argument to $-f$ gives the negative definite case.

For the indefinite case, let $u$ and $v$ be unit eigenvectors of $H$ with eigenvalues $\alpha>0$ and $\beta<0$. Along the line $h=tu$,

$$f(a+tu)-f(a)=\frac{\alpha}{2}t^2+o(t^2)>0$$

for all sufficiently small nonzero $t$. Along $h=tv$,

$$f(a+tv)-f(a)=\frac{\beta}{2}t^2+o(t^2)<0$$

for all sufficiently small nonzero $t$. Every ball around $a$ therefore contains points where $f$ is larger than $f(a)$ and points where it is smaller, so $a$ is a saddle point.

When the Hessian is only semidefinite, the quadratic term vanishes in some directions and the higher-order terms decide the outcome. The test then gives no conclusion, and the point may be a minimum, a maximum or a saddle.

## The two-variable determinant form

For $f(x,y)$, write

$$H_f(a)=\begin{pmatrix}f_{xx}(a)&f_{xy}(a)\\ f_{xy}(a)&f_{yy}(a)\end{pmatrix} \qquad \Delta=f_{xx}(a)f_{yy}(a)-f_{xy}(a)^2 \tag{2}$$

The determinant $\Delta$ is the product of the eigenvalues, and the trace $f_{xx}+f_{yy}$ is their sum. The classification follows from these two quantities.

+ If $\Delta>0$ and $f_{xx}(a)>0$, then both eigenvalues are positive and $a$ is a local minimum.
+ If $\Delta>0$ and $f_{xx}(a)<0$, then both eigenvalues are negative and $a$ is a local maximum.
+ If $\Delta<0$, then the eigenvalues have opposite signs and $a$ is a saddle point.
+ If $\Delta=0$, then at least one eigenvalue is zero and the test is inconclusive.

The condition $\Delta>0$ forces $f_{xx}$ and $f_{yy}$ to have the same sign, so $f_{xx}$ may be replaced by $f_{yy}$ in the first two cases. The determinant alone does not distinguish a maximum from a minimum; the sign of $f_{xx}$ does.

## A worked example

Consider

$$f(x,y)=x^3+y^3-3xy$$

The first derivatives are

$$f_x=3x^2-3y \qquad f_y=3y^2-3x$$

At a critical point, $y=x^2$ and $x=y^2$. Substituting the first relation into the second gives $x=x^4$, hence $x(x^3-1)=0$. The real solutions are $x=0$ and $x=1$, which produce the critical points

$$(0,0) \qquad\text{and}\qquad (1,1)$$

The Hessian is

$$H_f(x,y)=\begin{pmatrix}6x&-3\\ -3&6y\end{pmatrix}$$

At $(0,0)$,

$$H_f(0,0)=\begin{pmatrix}0&-3\\ -3&0\end{pmatrix} \qquad \Delta=0\cdot0-(-3)^2=-9<0$$

so the origin is a saddle point. At $(1,1)$,

$$H_f(1,1)=\begin{pmatrix}6&-3\\ -3&6\end{pmatrix} \qquad \Delta=36-9=27>0$$

and $f_{xx}(1,1)=6>0$, so $(1,1)$ is a local minimum. The value there is

$$f(1,1)=1+1-3=-1$$

The example also shows why both critical points must be examined. The gradient vanishes at both, but the Hessian assigns them different characters.

## When the determinant vanishes

The case $\Delta=0$ requires a separate argument. The following functions all have a critical point at the origin and a zero Hessian there, yet their behaviour is different.

| Function | Hessian at the origin | Behaviour at the origin |
|---|---|---|
| $x^4+y^4$ | zero matrix | strict local minimum |
| $-x^4-y^4$ | zero matrix | strict local maximum |
| $x^4-y^4$ | zero matrix | saddle point |
| $x^2+y^3$ | $\operatorname{diag}(2,0)$ | saddle point |

For $x^4+y^4$, the function is non-negative and vanishes only at the origin, so the origin is a strict minimum. For $-x^4-y^4$ the same argument with the sign reversed gives a strict maximum. For $x^4-y^4$, the value is positive on the $x$-axis and negative on the $y$-axis, so the origin is a saddle point. For $x^2+y^3$, the Hessian is positive semidefinite, but the function is positive on the $x$-axis and negative on the negative $y$-axis; the origin is again a saddle point. A positive semidefinite Hessian therefore does not by itself imply a minimum.

## Extrema on a compact set

A continuous function on a closed and bounded subset of $\mathbb{R}^n$ attains a global maximum and a global minimum. This is the multivariable form of [Weierstrass' theorem](../weierstrass-theorem/). The theorem guarantees existence, but it does not identify the points. The following procedure does.

+ Find the critical points of $f$ in the interior of the set and evaluate $f$ there.
+ Find the maximum and minimum of $f$ on the boundary. On a smooth boundary this is a constrained problem, treated in the entry on [Lagrange multipliers](../lagrange-multipliers/); on a polygon or a circle it may be reduced to one variable.
+ Compare all the values obtained. The largest is the global maximum and the smallest is the global minimum.

Consider

$$f(x,y)=x^2+y^2-xy$$

on the closed unit disk $D=\{(x,y):x^2+y^2\le1\}$. The gradient is

$$\nabla f=(2x-y,2y-x)$$

and $\nabla f=0$ forces $y=2x$ and $x=2y$, hence $x=y=0$. The only interior critical point is the origin, where $f(0,0)=0$. The Hessian there is

$$H_f(0,0)=\begin{pmatrix}2&-1\\ -1&2\end{pmatrix}$$

with $\Delta=3>0$ and $f_{xx}=2>0$, so the origin is a local minimum.

On the boundary, write $x=\cos t$ and $y=\sin t$. Then

$$f(\cos t,\sin t)=1-\cos t\sin t=1-\frac{1}{2}\sin 2t$$

As $t$ varies, $\sin 2t$ ranges over $[-1,1]$. Hence the boundary values range from $1-\frac{1}{2}=\frac{1}{2}$ to $1+\frac{1}{2}=\frac{3}{2}$. The global maximum is $\frac{3}{2}$, attained where $\sin 2t=-1$, namely at the two points $\left(\frac{1}{\sqrt2},-\frac{1}{\sqrt2}\right)$ and $\left(-\frac{1}{\sqrt2},\frac{1}{\sqrt2}\right)$. The global minimum is $0$ at the origin.

The example also illustrates a general point: the global minimum can be an interior critical point while the global maximum lies on the boundary. A search that considers only the gradient misses the maximum.

## Convexity and global minima

The second derivative test is local. A global conclusion is available when the Hessian has a fixed sign everywhere.

+ **Convexity criterion.** Let $A\subseteq\mathbb{R}^n$ be convex and let $f:A\to\mathbb{R}$ be of class $C^2$. If $H_f(x)$ is positive semidefinite for every $x\in A$, then $f$ is convex. If $H_f(x)$ is positive definite for every $x\in A$, then $f$ is strictly convex.

To see this, fix $a,x\in A$ and define $g(t)=f(a+t(x-a))$ for $0\le t\le1$. The segment lies in $A$ because $A$ is convex. The chain rule gives

$$g''(t)=(x-a)^{T}H_f(a+t(x-a))(x-a)$$

If the Hessian is positive semidefinite, then $g''(t)\ge0$, so $g$ is convex on $[0,1]$. Hence

$$g(1)\ge g(0)+g'(0)=f(a)+\nabla f(a)\cdot(x-a)$$

If $a$ is a critical point, the last term vanishes and $f(x)\ge f(a)$ for every $x\in A$. Thus every critical point of a convex function is a global minimum. If the Hessian is positive definite and $x\neq a$, then $g''(t)>0$ on $(0,1)$, the inequality is strict, and the global minimum is unique.

For example, the function $f(x,y)=x^2+y^2+xy$ has Hessian

$$H_f=\begin{pmatrix}2&1\\ 1&2\end{pmatrix}$$

whose eigenvalues are $1$ and $3$. The Hessian is positive definite everywhere, so $f$ is strictly convex on $\mathbb{R}^2$. Its only critical point is the origin, which is therefore the unique global minimum.

Convexity is a sufficient condition for a critical point to be global, not a necessary one. A non-convex function may still have a global minimum at a critical point, and a convex function may fail to attain its minimum if its domain is not closed or not bounded.
