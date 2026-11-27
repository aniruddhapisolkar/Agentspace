---
title: Vector-Valued Functions
source: https://algebrica.org/vector-valued-functions/
license: CC BY-NC 4.0
tags:
  - arc-length
  - curvature
  - multivariable-calculus
  - parametric-curves
  - space-curves
  - vector-valued-functions
---

## A function whose values are vectors

A real-valued function assigns a number to each point of its domain. A vector-valued function assigns a vector. When the domain is an interval of real numbers, the values trace a curve: the parameter selects a position, and the vector records that position relative to the origin. This is the setting in which differentiation and integration of curves are developed.

Let $I\subseteq\mathbb{R}$ be an interval. A vector-valued function in space is a map

$$\mathbf{r}:I\to\mathbb{R}^3$$

written in components as

$$\mathbf{r}(t)=f(t)\,\mathbf{i}+g(t)\,\mathbf{j}+h(t)\,\mathbf{k}$$

or, equivalently,

$$\mathbf{r}(t)=\langle f(t),g(t),h(t)\rangle \tag{1}$$

The real-valued functions $f,$ $g$ and $h$ are the component functions. In the plane the third component is omitted and $\mathbf{r}(t)=\langle f(t),g(t)\rangle.$ The domain of $\mathbf{r}$ is the intersection of the domains of its components, since all three components must be defined at the same parameter value.

The parameter need not represent time. It may be an angle, an arc length or any quantity that distinguishes points of the curve. The image

$$C=\{\mathbf{r}(t):t\in I\}$$

is a parametric curve, and the equations

$$x=f(t) \qquad y=g(t) \qquad z=h(t)$$

are its parametric equations. The same curve admits infinitely many parameterizations. The function $\mathbf{r}$ carries more information than the set $C,$ because it also fixes an orientation: the direction in which $t$ increases.

A vector-valued function is not a vector field. A vector field assigns a vector to each point of a region in space, so its domain is a subset of $\mathbb{R}^2$ or $\mathbb{R}^3.$ A vector-valued function of one parameter assigns a vector to each parameter value, so its domain is an interval. The distinction becomes important when line integrals and differential operators are introduced.

## Space curves

The graph of a vector-valued function is drawn by plotting the terminal point of the position vector $\mathbf{r}(t)$ as $t$ varies. The result is a curve in the plane or in space, not a surface.

The standard example is the helix

$$\mathbf{r}(t)=\langle a\cos t,\,a\sin t,\,bt\rangle \qquad t\in\mathbb{R} \tag{2}$$

with $a>0$ and $b\neq0.$ Its projection onto the $xy$-plane is the circle $x^2+y^2=a^2,$ traversed counterclockwise, while $z=bt$ increases linearly. The parameter $t$ is the angle of the projection, and $2\pi b$ is the vertical rise after one complete turn, called the pitch. At $t=0$ the point is $(a,0,0).$

Two familiar plane curves illustrate how the parameter changes the description. The circle

$$\mathbf{r}(t)=\langle R\cos t,R\sin t\rangle \qquad 0\le t\le2\pi$$

is traversed once counterclockwise. The same set is described by $\mathbf{r}(t)=\langle R\cos 2t,R\sin 2t\rangle$ for $0\le t\le\pi,$ but now the speed is doubled. A curve is therefore a geometric object, while a parameterization is a way of traversing it.

A parameterization can fail to be one-to-one. The curve $\mathbf{r}(t)=\langle\cos t,\sin t\rangle$ with $t\in[0,4\pi]$ traces the unit circle twice. Such a curve is still a parametric curve, but statements about length and integrals must account for the repetition. A curve is called simple if it does not intersect itself except possibly at the endpoints, and closed if its initial and terminal points coincide.

## Limits and continuity

Limits and continuity are defined componentwise. Let $\mathbf{r}(t)=\langle f(t),g(t),h(t)\rangle$ and let $L=\langle L_1,L_2,L_3\rangle.$ Then

$$\lim_{t\to t_0}\mathbf{r}(t)=L$$

if and only if

$$\lim_{t\to t_0}f(t)=L_1 \qquad \lim_{t\to t_0}g(t)=L_2 \qquad \lim_{t\to t_0}h(t)=L_3$$

Each component limit is an ordinary limit of a real function. Consequently, the usual limit laws hold for vector-valued functions: limits of sums, scalar multiples, dot products and cross products are computed from the corresponding limits, provided they exist.

The function $\mathbf{r}$ is continuous at $t_0$ if

$$\lim_{t\to t_0}\mathbf{r}(t)=\mathbf{r}(t_0)$$

which holds exactly when each component is continuous at $t_0.$ A curve is called continuous if its parameterization is continuous on the whole interval. Continuity of the parameterization does not prevent corners or cusps in the image; it only prevents jumps.

For example,

$$\lim_{t\to0}\left\langle \frac{\sin t}{t},\,e^{2t},\,\frac{1-\cos t}{t}\right\rangle=\left\langle1,1,0\right\rangle$$

because the three scalar limits are $1,$ $1$ and $0.$ The vector limit exists even though the first and third components are undefined at $t=0,$ since the limit ignores the value at the point.

## Derivatives and tangent vectors

The derivative of $\mathbf{r}$ at $t$ is defined by the same difference quotient as in one variable:

$$\mathbf{r}'(t)=\lim_{h\to0}\frac{\mathbf{r}(t+h)-\mathbf{r}(t)}{h} \tag{3}$$

provided the limit exists. Applying the definition to each component gives

$$\mathbf{r}'(t)=\langle f'(t),g'(t),h'(t)\rangle=f'(t)\,\mathbf{i}+g'(t)\,\mathbf{j}+h'(t)\,\mathbf{k} \tag{4}$$

so differentiation is performed componentwise. Higher derivatives are defined in the same way, and $\mathbf{r}''(t)=\langle f''(t),g''(t),h''(t)\rangle.$

Geometrically, $\mathbf{r}'(t)$ is tangent to the curve at $\mathbf{r}(t)$ and points in the direction of increasing $t.$ The vector $\mathbf{r}'(t)$ is the velocity of a particle whose position is $\mathbf{r}(t),$ and its magnitude is the speed. If $\mathbf{r}'(t_0)\neq\mathbf{0},$ the tangent line at $t_0$ is

$$\mathbf{L}(s)=\mathbf{r}(t_0)+s\,\mathbf{r}'(t_0) \qquad s\in\mathbb{R} \tag{5}$$

The unit tangent vector is defined when $\mathbf{r}'(t)\neq\mathbf{0}$ by

$$\mathbf{T}(t)=\frac{\mathbf{r}'(t)}{\lVert\mathbf{r}'(t)\rVert} \tag{6}$$

A parameterization is smooth on an interval if $\mathbf{r}'$ is continuous and never vanishes there. The nonvanishing condition is essential: it guarantees a well-defined tangent direction at every point.

Consider $\mathbf{r}(t)=\langle t,t^2,t^3\rangle.$ Then

$$\mathbf{r}'(t)=\langle1,2t,3t^2\rangle \qquad \mathbf{r}''(t)=\langle0,2,6t\rangle$$

At $t=1$ the point is $(1,1,1)$ and a tangent direction is $\langle1,2,3\rangle,$ so the tangent line is

$$\mathbf{L}(s)=\langle1+s,\,1+2s,\,1+3s\rangle$$

The curve $\mathbf{r}(t)=\langle t^2,t^3\rangle$ shows why the nonvanishing condition matters. Its derivative is $\langle2t,3t^2\rangle,$ which vanishes at $t=0.$ The image has a cusp at the origin: as $t\to0^+,$ the unit tangent tends to $\langle1,0\rangle,$ while as $t\to0^-$ it tends to $\langle-1,0\rangle.$ There is no single tangent direction at the cusp, although the curve is continuous there.

## Differentiation rules

Because differentiation is componentwise, the linear rules carry over without change. For differentiable vector-valued functions $\mathbf{r}$ and $\mathbf{s}$ and a differentiable scalar function $u,$

$$(\mathbf{r}\pm\mathbf{s})'=\mathbf{r}'\pm\mathbf{s}' \qquad (u\mathbf{r})'=u'\mathbf{r}+u\mathbf{r}'$$

The dot and cross products satisfy product rules:

$$(\mathbf{r}\cdot\mathbf{s})'=\mathbf{r}'\cdot\mathbf{s}+\mathbf{r}\cdot\mathbf{s}' \tag{7}$$

$$(\mathbf{r}\times\mathbf{s})'=\mathbf{r}'\times\mathbf{s}+\mathbf{r}\times\mathbf{s}' \tag{8}$$

The order of the factors in the cross-product rule must be preserved, since the cross product is not commutative. The chain rule takes the form

$$\frac{d}{dt}\,\mathbf{r}(u(t))=u'(t)\,\mathbf{r}'(u(t)) \tag{9}$$

Two consequences of (7) are worth separating. First,

$$\frac{d}{dt}\lVert\mathbf{r}(t)\rVert^2=2\,\mathbf{r}(t)\cdot\mathbf{r}'(t)$$

so the distance from the origin is constant exactly when $\mathbf{r}\cdot\mathbf{r}'=0.$ This describes motion on a sphere centred at the origin: the velocity is tangent to the sphere and therefore perpendicular to the radius. Second, applying the same rule to $\mathbf{v}\cdot\mathbf{v}$ gives

$$\frac{d}{dt}\lVert\mathbf{v}(t)\rVert^2=2\,\mathbf{v}(t)\cdot\mathbf{a}(t)$$

so the speed is constant exactly when the velocity is orthogonal to the acceleration.

The second condition does not say that constant speed implies zero acceleration. For a particle moving on a circle at constant speed, the velocity has constant magnitude but changing direction, so the acceleration is nonzero and points toward the centre. What vanishes is the component of acceleration along the velocity, not the acceleration itself.

## Speed, arc length and curvature

The speed of a parameterized curve is

$$v(t)=\lVert\mathbf{r}'(t)\rVert=\sqrt{f'(t)^2+g'(t)^2+h'(t)^2} \tag{10}$$

The arc length of the curve between $t=a$ and $t=b$ is the integral of speed:

$$L=\int_a^b\lVert\mathbf{r}'(t)\rVert\,dt \tag{11}$$

This formula comes from approximating the curve by short chords. A chord over $[t,t+\Delta t]$ has length approximately $\lVert\mathbf{r}'(t)\rVert\Delta t,$ and the sum of chord lengths tends to the integral as the partition is refined. The arc-length function

$$s(t)=\int_a^t\lVert\mathbf{r}'(u)\rVert\,du \tag{12}$$

measures distance along the curve from $\mathbf{r}(a).$ By the fundamental theorem of calculus, $ds/dt=\lVert\mathbf{r}'(t)\rVert.$ If the parameter is chosen so that $\lVert\mathbf{r}'(t)\rVert=1$ everywhere, the curve is parameterized by arc length, and then the parameter value equals the distance travelled.

For the helix (2),

$$\mathbf{r}'(t)=\langle-a\sin t,\,a\cos t,\,b\rangle \qquad \lVert\mathbf{r}'(t)\rVert=\sqrt{a^2\sin^2t+a^2\cos^2t+b^2}=\sqrt{a^2+b^2}$$

The speed is constant. One turn has length

$$L=\int_0^{2\pi}\sqrt{a^2+b^2}\,dt=2\pi\sqrt{a^2+b^2}$$

which is the length of the hypotenuse of a right triangle with legs $2\pi a$ and $2\pi b.$ Unrolling one turn of the helix onto a plane makes this evident: the turn becomes a straight segment with those components.

Curvature measures how quickly the tangent direction turns. It is defined by

$$\kappa=\left\lVert\frac{d\mathbf{T}}{ds}\right\rVert \tag{13}$$

where $s$ is arc length. Since $d\mathbf{T}/ds=(d\mathbf{T}/dt)/(ds/dt),$ this becomes

$$\kappa=\frac{\lVert\mathbf{T}'(t)\rVert}{\lVert\mathbf{r}'(t)\rVert} \tag{14}$$

A direct computation gives the practical formula

$$\kappa=\frac{\lVert\mathbf{r}'(t)\times\mathbf{r}''(t)\rVert}{\lVert\mathbf{r}'(t)\rVert^3} \tag{15}$$

For the helix, $\mathbf{r}''(t)=\langle-a\cos t,-a\sin t,0\rangle$ and

$$\mathbf{r}'\times\mathbf{r}''=\langle ab\sin t,\,-ab\cos t,\,a^2\rangle$$

so

$$\lVert\mathbf{r}'\times\mathbf{r}''\rVert=a\sqrt{b^2+a^2}$$

and therefore

$$\kappa=\frac{a\sqrt{a^2+b^2}}{(a^2+b^2)^{3/2}}=\frac{a}{a^2+b^2}$$

The curvature is constant. When $b=0$ the helix is a circle of radius $a,$ and the formula gives $\kappa=1/a,$ as expected. As $|b|$ grows with $a$ fixed, the helix stretches and its curvature decreases.

## Integrals

A vector-valued function is integrated componentwise. If $\mathbf{r}(t)=\langle f(t),g(t),h(t)\rangle$ is continuous on $[a,b],$ then

$$\int_a^b\mathbf{r}(t)\,dt=\left\langle\int_a^b f(t)\,dt,\ \int_a^b g(t)\,dt,\ \int_a^b h(t)\,dt\right\rangle \tag{16}$$

The fundamental theorem of calculus holds in the form

$$\int_a^b\mathbf{r}'(t)\,dt=\mathbf{r}(b)-\mathbf{r}(a) \tag{17}$$

For example,

$$\int_0^{\pi/2}\langle\cos t,\,t,\,e^t\rangle\,dt=\left\langle1,\,\frac{\pi^2}{8},\,e^{\pi/2}-1\right\rangle$$

Each component is evaluated separately. The result is a vector, not a scalar; an integral of a vector-valued function can therefore represent a total displacement, a total impulse or another vector quantity.

## Motion in space

When $t$ is time, the derivatives of position have physical names:

$$\mathbf{v}(t)=\mathbf{r}'(t) \qquad \mathbf{a}(t)=\mathbf{v}'(t)=\mathbf{r}''(t)$$

The speed is $v=\lVert\mathbf{v}\rVert,$ and the distance travelled between $t=a$ and $t=b$ is the arc length (11). The acceleration need not be tangent to the curve. It decomposes into a tangential part, which changes speed, and a normal part, which changes direction:

$$\mathbf{a}=a_T\,\mathbf{T}+a_N\,\mathbf{N} \qquad a_T=\frac{\mathbf{v}\cdot\mathbf{a}}{\lVert\mathbf{v}\rVert} \qquad a_N=\frac{\lVert\mathbf{v}\times\mathbf{a}\rVert}{\lVert\mathbf{v}\rVert} \tag{18}$$

where $\mathbf{N}$ is the principal unit normal. The normal component is related to curvature by $a_N=\kappa v^2.$ For motion at constant speed, $a_T=0$ and the acceleration is entirely normal.

Consider the circular helix

$$\mathbf{r}(t)=\langle\cos t,\,\sin t,\,t\rangle$$

Then

$$\mathbf{v}(t)=\langle-\sin t,\,\cos t,\,1\rangle \qquad \lVert\mathbf{v}(t)\rVert=\sqrt2$$

and

$$\mathbf{a}(t)=\langle-\cos t,\,-\sin t,\,0\rangle$$

The acceleration is horizontal and points toward the $z$-axis. Since $\mathbf{v}\cdot\mathbf{a}=0,$ the tangential acceleration vanishes and the speed is constant. The curvature is $\kappa=1/2,$ so $a_N=\kappa v^2=(1/2)(2)=1,$ which agrees with $\lVert\mathbf{a}\rVert=1.$

A parameterized curve can therefore be studied through its position, velocity and acceleration without introducing a separate theory for each component. The vector notation keeps the geometry visible: velocity is tangent, acceleration records both the change of speed and the bending of the path.

## What the definitions do not say

Several distinctions prevent common errors.

+ A vector-valued function is not the same object as its image curve. Different parameterizations of the same set generally have different derivatives, speeds and arc-length functions.
+ The derivative $\mathbf{r}'(t)$ is a vector attached to a parameter value, not a vector field. It is not defined at points of space that the curve does not pass through.
+ Continuity does not imply differentiability, and differentiability does not imply a nonvanishing derivative. The cusp $\langle t^2,t^3\rangle$ is differentiable everywhere but has no tangent direction at the origin.
+ The formula for arc length requires a continuously differentiable parameterization. A merely continuous curve can have infinite length, and a parameterization that retraces a segment counts that segment more than once.
+ Curvature is nonnegative and is independent of the orientation of the curve, while the unit tangent changes sign when the orientation is reversed.

## Related notions

The derivative of a vector-valued function leads to the tangent line and the unit tangent vector, and its integral leads to arc length and to the [line integral](../line-integrals/) of a scalar function. When a vector is assigned to every point of a region rather than to every parameter value, the object is a [vector field](../vector-fields/), and the derivatives of that field are the [divergence](../divergence/) and the [curl](../curl/). The [arc length of a curve](../arc-length-of-a-curve/) is the one-dimensional case of the formula above.
