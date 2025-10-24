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
\displaystyle \frac{\partial x}{\partial u} & \displaystyle \frac{\partial x}{\partial v} & \displaystyle \frac{\partial x}{\partial w}\\[6pt]
\displaystyle \frac{\partial y}{\partial u} & \displaystyle \frac{\partial y}{\partial v} & \displaystyle \frac{\partial y}{\partial w}\\[6pt]
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
h_u\hat{\mathbf{e}}_u & h_v\hat{\mathbf{e}}_v & h_w\hat{\mathbf{e}}_w\\[4pt]
\displaystyle \frac{\partial}{\partial u} & \displaystyle \frac{\partial}{\partial v} & \displaystyle \frac{\partial}{\partial w}\\[6pt]
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
\hat{\mathbf z}&=\hat{\mathbf z},\\[4pt]
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
