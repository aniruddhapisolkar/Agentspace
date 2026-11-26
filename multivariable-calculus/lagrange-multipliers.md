---
title: Lagrange Multipliers
source: https://algebrica.org/lagrange-multipliers/
license: CC BY-NC 4.0
tags:
  - constrained-optimization
  - gradient
  - lagrange-multiplier
  - level-sets
  - multivariable-calculus
---

## The constrained problem

Many optimisation problems do not allow the variables to move freely. A production plan must satisfy a budget, a geometric design must fit a surface, and a point on a curve must remain on that curve. In each case the objective is a function $f$, while the admissible points form a set described by one or more equations.

Let $U\subseteq\mathbb{R}^n$ be open and let $f,g:U\to\mathbb{R}$ be of class $C^1$. The constraint set is

$$S=\{x\in U:g(x)=0\}$$

A point $p\in S$ is a local constrained maximum of $f$ if there is $r>0$ such that

$$f(x)\le f(p) \qquad\text{for every }x\in S\cap B(p,r)$$

Local constrained minima are defined by reversing the inequality. The comparison is made only among points that satisfy the constraint, so a constrained maximum need not be a local maximum of $f$ on the whole open set $U$.

The method of Lagrange multipliers converts the constrained problem into a system of equations for the gradients. It identifies the possible locations of constrained extrema; it does not, by itself, prove that an extremum exists or decide which candidate is a maximum.

## Tangency of level sets

Consider the level curves of $f$ and the constraint curve $g=0$ in the plane, and assume for the moment that both gradients are nonzero. At a constrained extremum, the level curve of $f$ through $p$ is tangent to the constraint curve. If the two curves crossed transversally, then moving a small distance along the constraint would enter a region where $f$ is larger and also a region where $f$ is smaller, so $p$ could not be an extremum.

The gradient gives the normal direction to a level set. If $\nabla f(p)\neq0$, then $\nabla f(p)$ is normal to the level curve $\{f=f(p)\}$ at $p$. If $\nabla g(p)\neq0$, then $\nabla g(p)$ is normal to the constraint curve $\{g=0\}$ at $p$. Tangency means that the two normals are parallel, so there is a scalar $\lambda$ with

$$\nabla f(p)=\lambda\nabla g(p) \tag{1}$$

The scalar $\lambda$ is the Lagrange multiplier. The equation is a vector equation: in $\mathbb{R}^n$ it represents $n$ scalar equations, which together with $g(p)=0$ form a system of $n+1$ equations in the $n+1$ unknowns $p_1,\ldots,p_n,\lambda$.

The tangency picture is a guide, not a proof. A curve can have a corner, a constraint can degenerate to a point, and the level set of $f$ can fail to be smooth where $\nabla f$ vanishes. The theorem below states the precise hypotheses.

## The multiplier theorem

+ **Theorem.** Let $U\subseteq\mathbb{R}^n$ be open, let $f,g:U\to\mathbb{R}$ be of class $C^1$, and let $p\in U$ satisfy $g(p)=0$ and $\nabla g(p)\neq0$. If the restriction of $f$ to $S=\{g=0\}$ has a local maximum or a local minimum at $p$, then there exists $\lambda\in\mathbb{R}$ such that $\nabla f(p)=\lambda\nabla g(p)$.

The proof uses the tangent directions of the constraint. Let $\gamma:(-\varepsilon,\varepsilon)\to S$ be a $C^1$ curve with $\gamma(0)=p$. Then $t\mapsto f(\gamma(t))$ has a local extremum at $t=0$, so

$$\frac{d}{dt}f(\gamma(t))\bigg|_{t=0}=\nabla f(p)\cdot\gamma'(0)=0 \tag{2}$$

Every vector $v=\gamma'(0)$ obtained in this way is tangent to $S$ at $p$. The regularity condition $\nabla g(p)\neq0$ ensures that, near $p$, the set $S$ is a smooth hypersurface and that its tangent space is exactly

$$T_pS=\{v\in\mathbb{R}^n:\nabla g(p)\cdot v=0\}$$

This is the content of the [implicit function theorem](../implicit-function-theorem/): one may solve $g(x)=0$ locally for one variable as a function of the others, and the derivative of that function gives the tangent directions. Equation (2) says that $\nabla f(p)$ is orthogonal to every vector in $T_pS$. The orthogonal complement of the hyperplane $T_pS$ is the one-dimensional space spanned by $\nabla g(p)$. Hence $\nabla f(p)$ is a scalar multiple of $\nabla g(p)$, which is (1).

Two features of the statement deserve emphasis. First, the condition is necessary, not sufficient: every constrained extremum at a regular point of the constraint must satisfy (1), but a solution of (1) may be neither a maximum nor a minimum. For example, $f(x,y)=x^3$ on the constraint $y=0$ satisfies the Lagrange condition at the origin with $\lambda=0$, yet $x^3$ changes sign there and the origin is not a constrained extremum. Second, the hypothesis $\nabla g(p)\neq0$ is essential. It is called a constraint qualification, and it excludes constraints that collapse or have a singular point at the candidate.

## Several constraints

Suppose that the admissible set is defined by $m$ equations,

$$g_1(x)=0,\qquad\ldots,\qquad g_m(x)=0$$

with $g=(g_1,\ldots,g_m):U\to\mathbb{R}^m$ of class $C^1$. Let $Dg(p)$ be the $m\times n$ Jacobian matrix of $g$ at $p$. The constraint qualification is now

$$\operatorname{rank}Dg(p)=m$$

so the gradients $\nabla g_1(p),\ldots,\nabla g_m(p)$ are linearly independent. Under this condition, $S$ is locally a smooth submanifold of codimension $m$, and its tangent space is the intersection of the kernels of the gradients.

If $f|_S$ has a local extremum at $p$, the same curve argument shows that $\nabla f(p)$ annihilates every tangent vector. The orthogonal complement of the intersection of the kernels is the span of the constraint gradients. Therefore there exist multipliers $\lambda_1,\ldots,\lambda_m$ such that

$$\nabla f(p)=\lambda_1\nabla g_1(p)+\cdots+\lambda_m\nabla g_m(p) \tag{3}$$

Together with the $m$ constraints, this gives $n+m$ equations for the $n$ coordinates of $p$ and the $m$ multipliers. The rank condition is again essential: without it, the constraint gradients do not describe all the normal directions of $S$.

## The method

The following procedure applies to equality constraints at regular points.

+ Write the objective $f$ and the constraints $g_j=0$. Check that the constraint gradients are linearly independent at the points where the constraints hold.
+ Form the Lagrangian

$$\mathcal{L}(x,\lambda)=f(x)-\sum_{j=1}^{m}\lambda_j g_j(x)$$

+ Solve the system $\nabla_x\mathcal{L}=0$ together with $g_1=\cdots=g_m=0$. Equivalently, solve (1) or (3) together with the constraints.
+ Evaluate $f$ at every solution. Compare the values, taking into account any boundary of the constraint set and any points where the constraint qualification fails.
+ Separately verify that a maximum or minimum exists. On a compact constraint set with continuous $f$, existence follows from the extreme value theorem; on a non-compact set, the candidates may all be saddles or the extremum may fail to be attained.

The multiplier $\lambda$ is an auxiliary unknown. It is often eliminated while solving, and its value is not needed to identify the point. In applications it frequently has an interpretation as a sensitivity or shadow price, discussed below.

## A first example

Maximise and minimise

$$f(x,y)=xy \qquad\text{subject to}\qquad x^2+y^2=1$$

Here $g(x,y)=x^2+y^2-1$, so

$$\nabla f=(y,x) \qquad \nabla g=(2x,2y)$$

The Lagrange equations are

$$y=2\lambda x \qquad x=2\lambda y \qquad x^2+y^2=1$$

If $\lambda=0$, the first two equations give $x=y=0$, which violates the constraint. Hence $\lambda\neq0$. Multiplying the first equation by $y$ and the second by $x$ gives

$$xy=2\lambda x^2 \qquad xy=2\lambda y^2$$

so $2\lambda(x^2-y^2)=0$ and therefore $x^2=y^2$. The constraint then gives $2x^2=1$, so $x=\pm1/\sqrt2$ and $y=\pm1/\sqrt2$ with the same sign or opposite signs. The four candidates are

$$\left(\frac{1}{\sqrt2},\frac{1}{\sqrt2}\right),\quad \left(-\frac{1}{\sqrt2},-\frac{1}{\sqrt2}\right),\quad \left(\frac{1}{\sqrt2},-\frac{1}{\sqrt2}\right),\quad \left(-\frac{1}{\sqrt2},\frac{1}{\sqrt2}\right)$$

At the first two points $xy=\frac12$; at the last two $xy=-\frac12$. Since the circle is compact and $f$ is continuous, both extrema are attained. The maximum is $\frac12$ at the two points with equal signs, and the minimum is $-\frac12$ at the two points with opposite signs.

## Distance to a plane

Find the point of the plane $x+2y+2z=9$ closest to $(1,2,3)$. Minimising the distance is equivalent to minimising the squared distance

$$f(x,y,z)=(x-1)^2+(y-2)^2+(z-3)^2$$

subject to

$$g(x,y,z)=x+2y+2z-9=0$$

The gradients are

$$\nabla f=(2(x-1),2(y-2),2(z-3)) \qquad \nabla g=(1,2,2)$$

The Lagrange equations are

$$2(x-1)=\lambda \qquad 2(y-2)=2\lambda \qquad 2(z-3)=2\lambda$$

so

$$x=1+\frac{\lambda}{2} \qquad y=2+\lambda \qquad z=3+\lambda$$

Substituting into the constraint gives

$$\left(1+\frac{\lambda}{2}\right)+2(2+\lambda)+2(3+\lambda)=9$$

that is,

$$11+\frac{9\lambda}{2}=9 \qquad\text{hence}\qquad \lambda=-\frac49$$

Therefore

$$x=\frac79 \qquad y=\frac{14}{9} \qquad z=\frac{23}{9}$$

and

$$f\left(\frac79,\frac{14}{9},\frac{23}{9}\right)=\left(-\frac29\right)^2+\left(-\frac49\right)^2+\left(-\frac49\right)^2=\frac{4}{9}$$

The distance is $\frac23$. The distance formula for a plane gives the same value:

$$\frac{|1+2(2)+2(3)-9|}{\sqrt{1^2+2^2+2^2}}=\frac{2}{3}$$

The plane is not compact, but the squared distance tends to infinity as the point recedes in the plane, so the minimum is attained. The single Lagrange candidate is therefore the global minimum.

## Two constraints

Minimise

$$f(x,y,z)=x^2+y^2+z^2 \qquad\text{subject to}\qquad x+y+z=1,\quad x-y=0$$

Write

$$g_1=x+y+z-1 \qquad g_2=x-y$$

The gradients are

$$\nabla f=(2x,2y,2z) \qquad \nabla g_1=(1,1,1) \qquad \nabla g_2=(1,-1,0)$$

The constraint gradients are linearly independent, since $(1,1,1)$ and $(1,-1,0)$ are not multiples. The Lagrange system is

$$2x=\lambda+\mu \qquad 2y=\lambda-\mu \qquad 2z=\lambda$$

together with $x+y+z=1$ and $x=y$. The last constraint gives $\mu=0$, so the first two equations give $x=y=\lambda/2$, and the third gives $z=\lambda/2$. Hence $x=y=z$, and the first constraint gives $3x=1$. The only candidate is

$$\left(\frac13,\frac13,\frac13\right) \qquad f=\frac13$$

The feasible set is the line obtained by intersecting the plane $x+y+z=1$ with the plane $x=y$, and $f$ is the squared distance from the origin. The point found is the orthogonal projection of the origin onto that line, so it is the global minimum.

## The multiplier as a sensitivity

The value of $\lambda$ has a meaning beyond the algebra. Consider a family of constraints

$$g(x)=c$$

and let $M(c)$ be the optimal value of $f$ on the constraint set, for $c$ near the value at which the extremum is known. Suppose that the optimal point $p(c)$ depends differentiably on $c$ and that the constraint qualification holds. Differentiating $g(p(c))=c$ gives

$$\nabla g(p(c))\cdot p'(c)=1 \tag{4}$$

If $p(c)$ is a constrained maximum or minimum, it satisfies $\nabla f(p(c))=\lambda(c)\nabla g(p(c))$. Therefore

$$M'(c)=\nabla f(p(c))\cdot p'(c)=\lambda(c)\nabla g(p(c))\cdot p'(c)=\lambda(c) \tag{5}$$

Thus $\lambda$ is the rate at which the optimal value changes as the constraint level changes. In the plane example, the optimal squared distance is

$$M(c)=\frac{(c-11)^2}{9}$$

for $c$ near $9$, and $M'(9)=-4/9$, which is the multiplier found above.

The numerical value of $\lambda$ depends on how the constraint is scaled. Replacing $g$ by $2g$ changes $\lambda$ to $\lambda/2$, while the constraint set and the optimal point remain the same. The product $\lambda\,dc$ is invariant under such a rescaling, because $dc$ is rescaled in the opposite way.

## When the hypothesis fails

The constraint qualification $\nabla g(p)\neq0$ cannot be omitted. Consider

$$f(x,y)=x+y \qquad\text{subject to}\qquad g(x,y)=x^2+y^2=0$$

The constraint set is the single point $(0,0)$, so $f$ has both a constrained maximum and a constrained minimum there. But $\nabla g(0,0)=(0,0)$, and the equation

$$(1,1)=\lambda(0,0)$$

has no solution. The Lagrange condition therefore fails at a genuine constrained extremum. The reason is that the constraint set is not a smooth curve at the origin; it collapses to a point, and the tangent-space argument does not apply.

A different failure is a constraint set with a corner. At a corner, the tangent space may not be a single hyperplane, and the multiplier equation may hold with different multipliers on the two branches. Such problems require a separate analysis of the non-smooth constraint.

The method also says nothing about inequality constraints. For a constraint $g(x)\le0$, the boundary $g=0$ is only part of the admissible set, and the interior $g<0$ must be examined separately. The Karush-Kuhn-Tucker conditions extend the multiplier idea to inequalities, with non-negative multipliers and a complementary slackness condition, but that theory is outside the scope of this entry.

## A summary of the logic

Lagrange multipliers rest on three statements. At a constrained extremum, the derivative of $f$ along every admissible curve vanishes. At a regular point of the constraint, the admissible tangent directions are exactly the vectors orthogonal to the constraint gradients. Therefore the gradient of $f$ lies in the span of the constraint gradients. The resulting equations are necessary conditions; existence, sufficiency and the global comparison remain separate questions.
