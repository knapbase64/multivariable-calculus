A curvilinear coordinate system is just a change of variables from Cartesian $(x,y,z)$ to $(u,v,w)$, given by
$$
x=x(u,v,w),\qquad y=y(u,v,w),\qquad z=z(u,v,w),
$$
or, in vector form, $\mathbf{r}(u,v,w)=\langle x(u,v,w),y(u,v,w),z(u,v,w)\rangle$. The three coordinate curves are obtained by varying one variable while holding the other two fixed; their tangent vectors at a point are
$$
\mathbf{a}_u=\frac{\partial\mathbf{r}}{\partial u},\qquad
\mathbf{a}_v=\frac{\partial\mathbf{r}}{\partial v},\qquad
\mathbf{a}_w=\frac{\partial\mathbf{r}}{\partial w}.
$$
Define the scale factors as the lengths of these tangents,
$$
h_u=\|\mathbf{a}_u\|,\qquad h_v=\|\mathbf{a}_v\|,\qquad h_w=\|\mathbf{a}_w\|,
$$
and the corresponding unit vectors
$$
\hat{\mathbf{e}}_u=\frac{\mathbf{a}_u}{h_u},\qquad
\hat{\mathbf{e}}_v=\frac{\mathbf{a}_v}{h_v},\qquad
\hat{\mathbf{e}}_w=\frac{\mathbf{a}_w}{h_w}.
$$
In an orthogonal coordinate system the coordinate curves meet at right angles, so $\hat{\mathbf{e}}_u,\hat{\mathbf{e}}_v,\hat{\mathbf{e}}_w$ are mutually perpendicular at each point.

The differential displacement (line element) and its length are
$$
\begin{aligned}
d\boldsymbol{\ell}=d\mathbf{r}=\mathbf{a}_u\,du+\mathbf{a}_v\,dv+\mathbf{a}_w\,dw
=h_u\,du\,\hat{\mathbf{e}}_u+h_v\,dv\,\hat{\mathbf{e}}_v+h_w\,dw\,\hat{\mathbf{e}}_w,
\\
ds^2=h_u^2\,du^2+h_v^2\,dv^2+h_w^2\,dw^2.
\end{aligned}
$$
The oriented area element on the coordinate surface $u=\text{const}$ (spanned by the $(v,w)$-curves) is
$$
d\mathbf{a}_u=\big(\mathbf{a}_v\times\mathbf{a}_w\big)\,dv\,dw=h_v h_w\,dv\,dw\,\hat{\mathbf{e}}_u,
$$
and similarly
$$
d\mathbf{a}_v=h_w h_u\,dw\,du\,\hat{\mathbf{e}}_v,\qquad
d\mathbf{a}_w=h_u h_v\,du\,dv\,\hat{\mathbf{e}}_w.
$$
The volume element is the triple product of the tangent vectors,
$$
d\tau=\big(\mathbf{a}_u\cdot(\mathbf{a}_v\times\mathbf{a}_w)\big)\,du\,dv\,dw=h_u h_v h_w\,du\,dv\,dw.
$$

The Jacobian matrix of the change of variables and its determinant are
$$
\frac{\partial(x,y,z)}{\partial(u,v,w)}=
\begin{pmatrix}
\displaystyle \frac{\partial x}{\partial u} & \displaystyle \frac{\partial x}{\partial v} & \displaystyle \frac{\partial x}{\partial w}\\
\displaystyle \frac{\partial y}{\partial u} & \displaystyle \frac{\partial y}{\partial v} & \displaystyle \frac{\partial y}{\partial w}\\
\displaystyle \frac{\partial z}{\partial u} & \displaystyle \frac{\partial z}{\partial v} & \displaystyle \frac{\partial z}{\partial w}
\end{pmatrix},
\qquad
J=\det\!\left(\frac{\partial(x,y,z)}{\partial(u,v,w)}\right)=\mathbf{a}_u\cdot(\mathbf{a}_v\times\mathbf{a}_w).
$$
Thus the change–of–variables rule for triple integrals is
$$
\iiint_E f(x,y,z)\,d\tau=\iiint_U f(\mathbf{r}(u,v,w))\,|J(u,v,w)|\,du\,dv\,dw
=\iiint_U f(\mathbf{r}(u,v,w))\,h_u h_v h_w\,du\,dv\,dw.
$$

Vector operators in orthogonal curvilinear coordinates (write $\mathbf{A}=A_u\,\hat{\mathbf{e}}_u+A_v\,\hat{\mathbf{e}}_v+A_w\,\hat{\mathbf{e}}_w$ and $f=f(u,v,w)$) are
$$
\nabla f=\hat{\mathbf{e}}_u\,\frac{1}{h_u}\frac{\partial f}{\partial u}
+\hat{\mathbf{e}}_v\,\frac{1}{h_v}\frac{\partial f}{\partial v}
+\hat{\mathbf{e}}_w\,\frac{1}{h_w}\frac{\partial f}{\partial w},
$$
$$
\nabla\cdot\mathbf{A}=\frac{1}{h_u h_v h_w}\!\left[
\frac{\partial}{\partial u}\!\big(h_v h_w A_u\big)+
\frac{\partial}{\partial v}\!\big(h_w h_u A_v\big)+
\frac{\partial}{\partial w}\!\big(h_u h_v A_w\big)\right],
$$
$$
\nabla\times\mathbf{A}=\frac{1}{h_u h_v h_w}
\begin{vmatrix}
h_u\hat{\mathbf{e}}_u & h_v\hat{\mathbf{e}}_v & h_w\hat{\mathbf{e}}_w\\
\displaystyle \frac{\partial}{\partial u} & \displaystyle \frac{\partial}{\partial v} & \displaystyle \frac{\partial}{\partial w}\\
h_u A_u & h_v A_v & h_w A_w
\end{vmatrix},
\qquad
\nabla^2 f=\frac{1}{h_u h_v h_w}\sum_{\alpha\in\{u,v,w\}}
\frac{\partial}{\partial \alpha}\!\left(\frac{h_u h_v h_w}{h_\alpha^2}\,\frac{\partial f}{\partial \alpha}\right).
$$
Line, flux, and volume integrals are computed by inserting the elements above:
$$
\int_C \mathbf{A}\cdot d\boldsymbol{\ell},\qquad
\iint_S \mathbf{A}\cdot d\mathbf{a},\qquad
\iiint_V \rho\,d\tau,
$$
with the sign/orientation fixed by the right–hand rule.

Cartesian coordinates $(x,y,z)$ are the special case $u=x,\ v=y,\ w=z$ with
$$
h_x=h_y=h_z=1,\qquad
d\boldsymbol{\ell}=dx\,\hat{\mathbf{x}}+dy\,\hat{\mathbf{y}}+dz\,\hat{\mathbf{z}},\qquad
d\tau=dx\,dy\,dz,
$$
$$
d\mathbf{a}_x=dy\,dz\,\hat{\mathbf{x}},\quad
d\mathbf{a}_y=dz\,dx\,\hat{\mathbf{y}},\quad
d\mathbf{a}_z=dx\,dy\,\hat{\mathbf{z}},\qquad
J=1,
$$
and the usual formulas for $\nabla f,\ \nabla\cdot\mathbf{A},\ \nabla\times\mathbf{A},\ \nabla^2 f$.

## Cylindrical Coordinates

Cylindrical coordinates $(\rho,\phi,z)$ are defined by $x=\rho\cos\phi$, $y=\rho\sin\phi$, $z=z$, with
$$
h_\rho=1,\qquad h_\phi=\rho,\qquad h_z=1,\qquad
d\boldsymbol{\ell}=d\rho\,\hat{\boldsymbol{\rho}}+\rho\,d\phi\,\hat{\boldsymbol{\phi}}+dz\,\hat{\mathbf{z}},
$$
$$
d\mathbf{a}_\rho=\rho\,d\phi\,dz\,\hat{\boldsymbol{\rho}},\qquad
d\mathbf{a}_\phi=d\rho\,dz\,\hat{\boldsymbol{\phi}},\qquad
d\mathbf{a}_z=\rho\,d\rho\,d\phi\,\hat{\mathbf{z}},\qquad
d\tau=\rho\,d\rho\,d\phi\,dz,\qquad
J=\rho,
$$
Unit vectors: 

$$
\begin{aligned}
\hat{\boldsymbol \rho}&=\cos\phi\,\hat{\mathbf x}+\sin\phi\,\hat{\mathbf y},&
\hat{\boldsymbol \phi}&=-\sin\phi\,\hat{\mathbf x}+\cos\phi\,\hat{\mathbf y},&
\hat{\mathbf z}&=\hat{\mathbf z},\\
\hat{\mathbf x}&=\cos\phi\,\hat{\boldsymbol \rho}-\sin\phi\,\hat{\boldsymbol \phi},&
\hat{\mathbf y}&=\sin\phi\,\hat{\boldsymbol \rho}+\cos\phi\,\hat{\boldsymbol \phi},&
\hat{\mathbf z}&=\hat{\mathbf z}.
\end{aligned}
$$

Differential element $dS$:
$$
\begin{aligned}
\rho=\text{const}:&\quad dS=\rho\,d\phi\,dz,\\
\phi=\text{const}:&\quad dS=d\rho\,dz,\\
z=\text{const}:&\quad dS=\rho\,d\rho\,d\phi.
\end{aligned}
$$
$$
\nabla f=\hat{\boldsymbol{\rho}}\,\frac{\partial f}{\partial \rho}
+\hat{\boldsymbol{\phi}}\,\frac{1}{\rho}\frac{\partial f}{\partial \phi}
+\hat{\mathbf{z}}\,\frac{\partial f}{\partial z},
$$
$$
\nabla\cdot\mathbf{A}=\frac{1}{\rho}\frac{\partial}{\partial \rho}(\rho A_\rho)
+\frac{1}{\rho}\frac{\partial A_\phi}{\partial \phi}
+\frac{\partial A_z}{\partial z},
\qquad
\nabla^2 f=\frac{1}{\rho}\frac{\partial}{\partial \rho}\!\left(\rho\,\frac{\partial f}{\partial \rho}\right)
+\frac{1}{\rho^2}\frac{\partial^2 f}{\partial \phi^2}
+\frac{\partial^2 f}{\partial z^2},
$$
$$
\nabla\times\mathbf{A}=\hat{\boldsymbol{\rho}}\,\frac{1}{\rho}\!\left(\frac{\partial A_z}{\partial \phi}-\frac{\partial A_\phi}{\partial z}\right)
+\hat{\boldsymbol{\phi}}\!\left(\frac{\partial A_\rho}{\partial z}-\frac{\partial A_z}{\partial \rho}\right)
+\hat{\mathbf{z}}\,\frac{1}{\rho}\!\left(\frac{\partial(\rho A_\phi)}{\partial \rho}-\frac{\partial A_\rho}{\partial \phi}\right).
$$

For a surface given by $\rho=R(\phi, z)$, 

$$
d\textbf{a}
=\Big(R\,\hat{\boldsymbol{\rho}}
- R_\phi\,\hat{\boldsymbol{\phi}}
- R R_z\,\hat{\mathbf z}\Big)\,d\phi\,dz,
\qquad
dS=\sqrt{\,R^{2}+R_\phi^{2}+(R R_z)^{2}\,}\;d\phi\,dz.
$$

## Spherical Coordinates

Spherical coordinates $(r,\theta,\phi)$ are defined by $x=r\sin\theta\cos\phi$, $y=r\sin\theta\sin\phi$, $z=r\cos\theta$ (with $\theta$ the polar angle from $+z$ and $\phi$ the azimuth), with 
$$
\begin{aligned}
h_r=1,\qquad h_\theta=r,\qquad h_\phi=r\sin\theta,\\
d\boldsymbol{\ell}=dr\,\hat{\mathbf{r}}+r\,d\theta\,\hat{\boldsymbol{\theta}}+r\sin\theta\,d\phi\,\hat{\boldsymbol{\phi}},
\end{aligned}
$$
$$
\begin{aligned}
d\mathbf{a}_r=r^2\sin\theta\,d\theta\,d\phi\,\hat{\mathbf{r}},\\
d\mathbf{a}_\theta=r\sin\theta\,dr\,d\phi\,\hat{\boldsymbol{\theta}},\\
d\mathbf{a}_\phi=r\,dr\,d\theta\,\hat{\boldsymbol{\phi}},\\
d\tau=r^2\sin\theta\,dr\,d\theta\,d\phi,\\
J=r^2\sin\theta, 
\end{aligned}
$$
Unit vectors: 

$$
\begin{aligned}
\hat{\mathbf r}&=\sin\theta\cos\phi\,\hat{\mathbf x}
+\sin\theta\sin\phi\,\hat{\mathbf y}
+\cos\theta\,\hat{\mathbf z},\\
\hat{\boldsymbol \theta}&=\cos\theta\cos\phi\,\hat{\mathbf x}
+\cos\theta\sin\phi\,\hat{\mathbf y}
-\sin\theta\,\hat{\mathbf z},\\
\hat{\boldsymbol \phi}&=-\sin\phi\,\hat{\mathbf x}
+\cos\phi\,\hat{\mathbf y},
\end{aligned}
\qquad
\begin{aligned}
\hat{\mathbf x}&=\sin\theta\cos\phi\,\hat{\mathbf r}
+\cos\theta\cos\phi\,\hat{\boldsymbol \theta}
-\sin\phi\,\hat{\boldsymbol \phi},\\
\hat{\mathbf y}&=\sin\theta\sin\phi\,\hat{\mathbf r}
+\cos\theta\sin\phi\,\hat{\boldsymbol \theta}
+\cos\phi\,\hat{\boldsymbol \phi},\\
\hat{\mathbf z}&=\cos\theta\,\hat{\mathbf r}
-\sin\theta\,\hat{\boldsymbol \theta}.
\end{aligned}
$$

Differential element $dS$:
$$
\begin{aligned}
r=\text{const}:&\quad dS=r^{2}\sin\theta\,d\theta\,d\phi,\\
\theta=\text{const}:&\quad dS=r\sin\theta\,dr\,d\phi,\\
\phi=\text{const}:&\quad dS=r\,dr\,d\theta.
\end{aligned}
$$
$$
\nabla f=\hat{\mathbf{r}}\,\frac{\partial f}{\partial r}
+\hat{\boldsymbol{\theta}}\,\frac{1}{r}\frac{\partial f}{\partial \theta}
+\hat{\boldsymbol{\phi}}\,\frac{1}{r\sin\theta}\frac{\partial f}{\partial \phi},
$$
$$
\begin{aligned}
\nabla\cdot\mathbf{A}=\frac{1}{r^2}\frac{\partial}{\partial r}(r^2 A_r)
+\frac{1}{r\sin\theta}\frac{\partial}{\partial \theta}(\sin\theta\,A_\theta)
+\frac{1}{r\sin\theta}\frac{\partial A_\phi}{\partial \phi},
\\
\nabla^2 f=\frac{1}{r^2}\frac{\partial}{\partial r}\!\left(r^2\frac{\partial f}{\partial r}\right)
+\frac{1}{r^2\sin\theta}\frac{\partial}{\partial \theta}\!\left(\sin\theta\,\frac{\partial f}{\partial \theta}\right)
+\frac{1}{r^2\sin^2\theta}\frac{\partial^2 f}{\partial \phi^2},
\end{aligned}
$$
$$
\begin{aligned}
(\nabla\times\mathbf{A})_r=\frac{1}{r\sin\theta}\!\left(\frac{\partial}{\partial \theta}(\sin\theta\,A_\phi)-\frac{\partial A_\theta}{\partial \phi}\right),\\
(\nabla\times\mathbf{A})_\theta=\frac{1}{r}\!\left(\frac{1}{\sin\theta}\frac{\partial A_r}{\partial \phi}-\frac{\partial}{\partial r}(r A_\phi)\right),\\
(\nabla\times\mathbf{A})_\phi=\frac{1}{r}\!\left(\frac{\partial}{\partial r}(r A_\theta)-\frac{\partial A_r}{\partial \theta}\right).
\end{aligned}
$$

For a surface given by $r=R(\theta, \phi)$, 
$$
d\textbf{a}=((R^2\sin{\theta})\hat{\textbf{r}} - (RR_\theta \sin{\theta}) \hat{\boldsymbol{\theta}}+(RR_\phi) \hat{\boldsymbol{\phi}}) \cdot d\theta \cdot d\phi
$$
$$dS=||d\textbf{a}|| = \sqrt{R^4 \sin^2{\theta} + R^2 R_\theta^2 \sin^2\theta + R^2 R_\phi^2} \cdot d\theta \cdot d\phi$$

In two dimensions the same ideas give polar coordinates $(r,\theta)$ with
$$
\begin{aligned}
d\boldsymbol{\ell}=dr\,\hat{\mathbf{r}}+r\,d\theta\,\hat{\boldsymbol{\theta}},\\
dA=r\,dr\,d\theta,\\
J=r,\\
\nabla f=\hat{\mathbf{r}}\,\frac{\partial f}{\partial r}+\hat{\boldsymbol{\theta}}\,\frac{1}{r}\frac{\partial f}{\partial \theta},\\
\nabla^2 f=\frac{1}{r}\frac{\partial}{\partial r}\!\left(r\frac{\partial f}{\partial r}\right)+\frac{1}{r^2}\frac{\partial^2 f}{\partial \theta^2}.
\end{aligned}
$$

---

## Derivations

### Cylindrical Coordinates

Start from the position vector written as a function of cylindrical coordinates,
$$
\mathbf r(\rho,\phi,z)=x\,\hat{\mathbf x}+y\,\hat{\mathbf y}+z\,\hat{\mathbf k}
=\rho\cos\phi\,\hat{\mathbf x}+\rho\sin\phi\,\hat{\mathbf y}+z\,\hat{\mathbf k}.
$$
The scale factors are the magnitudes of the coordinate tangent vectors $\mathbf r_\rho=\partial\mathbf r/\partial\rho$, $\mathbf r_\phi=\partial\mathbf r/\partial\phi$, and $\mathbf r_z=\partial\mathbf r/\partial z$. Differentiating gives
$$
\mathbf r_\rho=\cos\phi\,\hat{\mathbf x}+\sin\phi\,\hat{\mathbf y},\qquad
\mathbf r_\phi=-\rho\sin\phi\,\hat{\mathbf x}+\rho\cos\phi\,\hat{\mathbf y},\qquad
\mathbf r_z=\hat{\mathbf k}.
$$
Their magnitudes are
$$
h_\rho=|\mathbf r_\rho|=\sqrt{\cos^2\phi+\sin^2\phi}=1,\qquad
h_\phi=|\mathbf r_\phi|=\rho,\qquad
h_z=|\mathbf r_z|=1.
$$
The associated unit vectors follow by normalization,
$$
\hat{\boldsymbol\rho}=\frac{\mathbf r_\rho}{h_\rho}=\cos\phi\,\hat{\mathbf x}+\sin\phi\,\hat{\mathbf y},\quad
\hat{\boldsymbol\phi}=\frac{\mathbf r_\phi}{h_\phi}=-\sin\phi\,\hat{\mathbf x}+\cos\phi\,\hat{\mathbf y},\quad
\hat{\mathbf z}=\hat{\mathbf k}.
$$
The differential displacement is the linear combination of the coordinate tangents with the differentials,
$$
d\boldsymbol\ell=\mathbf r_\rho\,d\rho+\mathbf r_\phi\,d\phi+\mathbf r_z\,dz
=\hat{\boldsymbol\rho}\,d\rho+\rho\,\hat{\boldsymbol\phi}\,d\phi+\hat{\mathbf z}\,dz.
$$
Differential area vectors on the coordinate surfaces come from the appropriate cross products of tangents spanning those surfaces, with the order chosen so that the vector points along the outward normal. On a surface of constant $z$ (a disk), the patch is spanned by $\mathbf r_\rho$ and $\mathbf r_\phi$; thus
$$
d\mathbf a_z=(\mathbf r_\rho\times\mathbf r_\phi)\,d\rho\,d\phi
=\Big(\rho\,\hat{\mathbf k}\Big)\,d\rho\,d\phi
=\rho\,d\rho\,d\phi\,\hat{\mathbf z}.
$$
On a surface of constant $\rho$ (the cylindrical side), the patch is spanned by $\mathbf r_\phi$ and $\mathbf r_z$; hence
$$
d\mathbf a_\rho=(\mathbf r_\phi\times\mathbf r_z)\,d\phi\,dz
=\Big(\rho\cos\phi\,\hat{\mathbf x}+\rho\sin\phi\,\hat{\mathbf y}\Big)\,d\phi\,dz
=\rho\,d\phi\,dz\,\hat{\boldsymbol\rho}.
$$
On a surface of constant $\phi$ (a vertical half-plane), the patch is spanned by $\mathbf r_\rho$ and $\mathbf r_z$; using the order that yields the $\hat{\boldsymbol\phi}$ normal gives
$$
d\mathbf a_\phi=(\mathbf r_z\times\mathbf r_\rho)\,dz\,d\rho
=\hat{\boldsymbol\phi}\,dz\,d\rho
=d\rho\,dz\,\hat{\boldsymbol\phi}.
$$
The differential volume element is the scalar triple product of the three coordinate tangents,
$$
d\tau=\big(\mathbf r_\rho\times\mathbf r_\phi\big)\cdot\mathbf r_z\,d\rho\,d\phi\,dz
=\big(\rho\,\hat{\mathbf k}\big)\cdot\hat{\mathbf k}\,d\rho\,d\phi\,dz
=\rho\,d\rho\,d\phi\,dz.
$$
Equivalently, the Jacobian determinant of the transformation $(\rho,\phi,z)\mapsto(x,y,z)$ is
$$
J=\det\!\begin{pmatrix}
\partial x/\partial\rho & \partial x/\partial\phi & \partial x/\partial z\\
\partial y/\partial\rho & \partial y/\partial\phi & \partial y/\partial z\\
\partial z/\partial\rho & \partial z/\partial\phi & \partial z/\partial z
\end{pmatrix}
=\det\!\begin{pmatrix}
\cos\phi & -\rho\sin\phi & 0\\
\sin\phi & \ \rho\cos\phi & 0\\
0&0&1
\end{pmatrix}
=\rho,
$$
so $d\tau=J\,d\rho\,d\phi\,dz=\rho\,d\rho\,d\phi\,dz$. 

### Spherical Coordinates

Start from the position vector written in terms of spherical coordinates with the polar angle $\theta$ measured from $+z$ and the azimuth $\phi$ about $z$:
$$
\mathbf r(r,\theta,\phi)=x\,\hat{\mathbf x}+y\,\hat{\mathbf y}+z\,\hat{\mathbf z}
=r\sin\theta\cos\phi\,\hat{\mathbf x}+r\sin\theta\sin\phi\,\hat{\mathbf y}+r\cos\theta\,\hat{\mathbf z}.
$$
The coordinate tangent vectors are $\mathbf r_r=\partial\mathbf r/\partial r$, $\mathbf r_\theta=\partial\mathbf r/\partial\theta$, and $\mathbf r_\phi=\partial\mathbf r/\partial\phi$. Differentiating gives
$$
\mathbf r_r=\sin\theta\cos\phi\,\hat{\mathbf x}+\sin\theta\sin\phi\,\hat{\mathbf y}+\cos\theta\,\hat{\mathbf z},\qquad
\mathbf r_\theta=r\cos\theta\cos\phi\,\hat{\mathbf x}+r\cos\theta\sin\phi\,\hat{\mathbf y}-r\sin\theta\,\hat{\mathbf z},
$$
$$
\mathbf r_\phi=-r\sin\theta\sin\phi\,\hat{\mathbf x}+r\sin\theta\cos\phi\,\hat{\mathbf y}.
$$
The scale factors are the magnitudes of these tangents, namely $h_r=\lVert\mathbf r_r\rVert=1$, $h_\theta=\lVert\mathbf r_\theta\rVert=r$, and $h_\phi=\lVert\mathbf r_\phi\rVert=r\sin\theta$. Normalizing the tangents produces the spherical unit vectors,
$$
\hat{\mathbf r}=\frac{\mathbf r_r}{h_r}=\sin\theta\cos\phi\,\hat{\mathbf x}+\sin\theta\sin\phi\,\hat{\mathbf y}+\cos\theta\,\hat{\mathbf z},\qquad
\hat{\boldsymbol\theta}=\frac{\mathbf r_\theta}{h_\theta}=\cos\theta\cos\phi\,\hat{\mathbf x}+\cos\theta\sin\phi\,\hat{\mathbf y}-\sin\theta\,\hat{\mathbf z},
$$
$$
\hat{\boldsymbol\phi}=\frac{\mathbf r_\phi}{h_\phi}=-\sin\phi\,\hat{\mathbf x}+\cos\phi\,\hat{\mathbf y}.
$$
Because the $(\hat{\mathbf r},\hat{\boldsymbol\theta},\hat{\boldsymbol\phi})$ triad is orthonormal, the inverse relations follow by the transpose of the same rotation, giving
$$
\begin{aligned}
\hat{\mathbf x}=\sin\theta\cos\phi\,\hat{\mathbf r}+\cos\theta\cos\phi\,\hat{\boldsymbol\theta}-\sin\phi\,\hat{\boldsymbol\phi},\quad \\
\hat{\mathbf y}=\sin\theta\sin\phi\,\hat{\mathbf r}+\cos\theta\sin\phi\,\hat{\boldsymbol\theta}+\cos\phi\,\hat{\boldsymbol\phi},\quad \\
\hat{\mathbf z}=\cos\theta\,\hat{\mathbf r}-\sin\theta\,\hat{\boldsymbol\theta}.
\end{aligned}
$$
The differential displacement is the linear combination of tangents weighted by differentials,
$$
d\boldsymbol\ell=\mathbf r_r\,dr+\mathbf r_\theta\,d\theta+\mathbf r_\phi\,d\phi
=dr\,\hat{\mathbf r}+r\,d\theta\,\hat{\boldsymbol\theta}+r\sin\theta\,d\phi\,\hat{\boldsymbol\phi}.
$$
Area elements on the coordinate surfaces come from the appropriate cross products. On $r=$ const (a sphere), the patch is spanned by $\mathbf r_\theta$ and $\mathbf r_\phi$, and
$$
d\mathbf a_r=(\mathbf r_\theta\times\mathbf r_\phi)\,d\theta\,d\phi
=r^2\sin\theta\,d\theta\,d\phi\,\hat{\mathbf r}.
$$
On $\theta=$ const (a cone), choose the order that yields the $\hat{\boldsymbol\theta}$ normal, for instance $\mathbf r_\phi\times\mathbf r_r$, to obtain
$$
d\mathbf a_\theta=(\mathbf r_\phi\times\mathbf r_r)\,d\phi\,dr
=r\sin\theta\,dr\,d\phi\,\hat{\boldsymbol\theta}.
$$
On $\phi=$ const (a half-plane), take $\mathbf r_r\times\mathbf r_\theta$ to get
$$
d\mathbf a_\phi=(\mathbf r_r\times\mathbf r_\theta)\,dr\,d\theta
=r\,dr\,d\theta\,\hat{\boldsymbol\phi}.
$$
The differential volume element equals the scalar triple product of the three tangents,
$$
d\tau=(\mathbf r_r\times\mathbf r_\theta)\cdot\mathbf r_\phi\,dr\,d\theta\,d\phi
=r^2\sin\theta\,dr\,d\theta\,d\phi.
$$
Equivalently, the Jacobian determinant of the transformation $(r,\theta,\phi)\mapsto(x,y,z)$ computed from
$$
\frac{\partial(x,y,z)}{\partial(r,\theta,\phi)}=
\begin{pmatrix}
\sin\theta\cos\phi & r\cos\theta\cos\phi & -r\sin\theta\sin\phi\\
\sin\theta\sin\phi & r\cos\theta\sin\phi & \ \,r\sin\theta\cos\phi\\
\cos\theta & -r\sin\theta & 0
\end{pmatrix}
$$
is $J=r^2\sin\theta$, so $d\tau=J\,dr\,d\theta\,d\phi$ as above. Taking magnitudes of the area vectors recovers the scalar surface elements on the three coordinate surfaces: for $r=$ const, $dS=r^{2}\sin\theta\,d\theta\,d\phi$; for $\theta=$ const, $dS=r\sin\theta\,dr\,d\phi$; and for $\phi=$ const, $dS=r\,dr\,d\theta$.
