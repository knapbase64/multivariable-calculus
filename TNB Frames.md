Let $\vec r:I\to\mathbb R^3$ be a $C^3$ regular curve ($\vec r'(t)\neq \vec 0$). The unit tangent is
$$
\vec T(t)=\frac{\vec r'(t)}{\|\vec r'(t)\|}.
$$
Define arc length $s(t)=\int_{t_0}^t \|\vec r'(u)\|\,du$. When the curve is re-parameterized by arc length (unit speed), derivatives are taken with respect to $s$.

The principal normal and bi-normal are
$$
\vec N=\frac{d\vec T/ds}{\|d\vec T/ds\|},\qquad
\vec B=\vec T\times \vec N.
$$
Equivalently,
$$
\vec B=\frac{\vec r'\times \vec r''}{\|\vec r'\times \vec r''\|}\quad\text{whenever }\vec r'\times \vec r''\neq \vec 0.
$$
The ordered triple $(\vec T,\vec N,\vec B)$ is ortho-normal. 

Since $\|\vec T\|=1$, differentiating $\vec T\cdot \vec T=1$ gives $\vec T\cdot \tfrac{d\vec T}{ds}=0$, so $\tfrac{d\vec T}{ds}$ is orthogonal to $\vec T$ and thus parallel to $\vec N$. 

The curvature is
$$
\kappa=\Big\|\frac{d\vec T}{ds}\Big\|\ge 0.
$$
For a general parameter $t$,
$$
\frac{d\vec T}{dt}=\frac{d\vec T}{ds}\,\frac{ds}{dt}=\kappa\,\|\vec r'(t)\|\,\vec N,
$$
hence
$$
\kappa=\frac{\|\vec T'(t)\|}{\|\vec r'(t)\|}=\frac{\|\vec r'(t)\times \vec r''(t)\|}{\|\vec r'(t)\|^3}.
$$
In the plane $z\equiv 0$ with $y=y(x)$, one recovers
$$
\kappa(x)=\frac{|y''(x)|}{\big(1+(y'(x))^2\big)^{3/2}}.
$$
The osculating circle at a point (when $\kappa>0$) has radius $R=1/\kappa$ and lies in the osculating plane spanned by $\vec T$ and $\vec N$.

The torsion measures deviation from planarity:
$$
\tau=-\frac{d\vec B}{ds}\cdot \vec N.
$$
An equivalent formula in terms of $\vec r$ is
$$
\tau=\frac{\big(\vec r'(t)\times \vec r''(t)\big)\cdot \vec r'''(t)}{\|\vec r'(t)\times \vec r''(t)\|^{2}},
$$
valid when $\vec r'\times \vec r''\neq \vec 0$. Planar curves have $\tau\equiv 0$.

With derivatives taken with respect to arc length,
$$
\frac{d\vec T}{ds}=\kappa\,\vec N,\qquad
\frac{d\vec N}{ds}=-\kappa\,\vec T+\tau\,\vec B,\qquad
\frac{d\vec B}{ds}=-\tau\,\vec N.
$$

The osculating plane is spanned by $\vec T,\vec N$ (normal $\vec B$); the normal plane by $\vec N,\vec B$ (normal $\vec T$); the rectifying plane by $\vec T,\vec B$ (normal $\vec N$).
