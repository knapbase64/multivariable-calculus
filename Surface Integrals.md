A scalar surface integral over a smooth oriented surface $S\subset\mathbb{R}^3$ parameterized by $\mathbf{r}:D\subset\mathbb{R}^2\to\mathbb{R}^3$, $(u,v)\mapsto \mathbf{r}(u,v)$, is
$$
\iint_S f\,dS
=\iint_D f(\mathbf{r}(u,v))\,\|\mathbf{r}_u\times \mathbf{r}_v\|\,du\,dv,
$$
where $dS=\|\mathbf{r}_u\times \mathbf{r}_v\|\,du\,dv$ is the area element and $\mathbf{r}_u\times\mathbf{r}_v$ is normal to the surface.

Given an orientation on $S$ with unit normal $\mathbf{n}$, the flux (vector) surface integral of a vector field $\mathbf{F}$ across $S$ is
$$
\iint_S \mathbf{F}\cdot \mathbf{n}\,dS
=\iint_D \mathbf{F}(\mathbf{r}(u,v))\cdot\big(\mathbf{r}_u\times \mathbf{r}_v\big)\,du\,dv.
$$
Reversing the orientation ($\mathbf{n}\mapsto -\mathbf{n}$) flips the sign of the flux integral, while the scalar surface integral is orientation-independent. If $S$ is a closed surface (no boundary), one often writes
$$
\oint_S \mathbf{F}\cdot \mathbf{n}\,dS.
$$

For surfaces given as graphs, $S=\{(x,y,g(x,y)):(x,y)\in D\}$ with the upward orientation, a convenient form is
$$
\begin{aligned}
\iint_S f\,dS=\iint_D f\big(x,y,g(x,y)\big)\,\sqrt{1+g_x^2+g_y^2}\,dx\,dy,
\\
\iint_S \mathbf{F}\cdot \mathbf{n}\,dS=\iint_D \mathbf{F}\big(x,y,g(x,y)\big)\cdot\langle -g_x,-g_y,1\rangle\,dx\,dy.
\end{aligned}
$$
Analogous projection formulas hold for graphs over the $yz$- or $xz$-planes.

If $S$ is the union of smooth patches $S_1$ and $S_2$ with compatible orientations, then
$$
\iint_S f\,dS=\iint_{S_1} f\,dS+\iint_{S_2} f\,dS,
\qquad
\iint_S \mathbf{F}\cdot\mathbf{n}\,dS=\iint_{S_1} \mathbf{F}\cdot\mathbf{n}\,dS+\iint_{S_2} \mathbf{F}\cdot\mathbf{n}\,dS.
$$
For a piecewise smooth surface with boundary $C=\partial S$, the positive boundary orientation is determined by the right–hand rule: if the thumb points along $\mathbf{n}$, the curled fingers indicate the direction of traversal of $C$. If there are holes with inner boundary curves $C_1,\dots,C_m$ and an outer boundary $C_0$, orient each $C_j$ by this rule relative to the chosen $\mathbf{n}$; the same formulas below hold with $\partial S=C_0\cup C_1\cup\cdots\cup C_m$ and line integrals understood as sums over all boundary components.

Stokes’ theorem connects the circulation around the boundary of a surface to the flux of the curl through the surface. Let $\mathbf{F}=\langle P,Q,R\rangle$ have continuous partial derivatives on an open set containing a smooth oriented surface $S$ with positively oriented boundary $C=\partial S$. Then
$$
\oint_{C} \mathbf{F}\cdot d\mathbf{r}
=\iint_{S} (\nabla\times \mathbf{F})\cdot \mathbf{n}\,dS.
$$
Equivalently, writing $\mathbf{T}\,ds=d\mathbf{r}$ for the boundary curve, one has
$$
\oint_C \mathbf{F}\cdot \mathbf{T}\,ds=\iint_S \operatorname{curl}\mathbf{F}\cdot \mathbf{n}\,dS,
$$
with the boundary orientation consistent with the chosen $\mathbf{n}$ by the right–hand rule. If $S_1$ and $S_2$ share the same boundary with matching boundary orientations, then
$$
\iint_{S_1} (\nabla\times\mathbf{F})\cdot \mathbf{n}\,dS=\iint_{S_2} (\nabla\times\mathbf{F})\cdot \mathbf{n}\,dS,
$$
so the surface integral of $\nabla\times\mathbf{F}$ depends only on $\partial S$. In particular, if $S$ is closed ($\partial S=\varnothing$), then
$$
\iint_S (\nabla\times\mathbf{F})\cdot \mathbf{n}\,dS=0.
$$

The divergence theorem relates the flux across a closed surface to a triple integral over the enclosed volume. Let $E\subset\mathbb{R}^3$ be a solid region with piecewise smooth boundary $\partial E$ oriented by the outward unit normal. Then
$$
\oint_{\partial E} \mathbf{F}\cdot \mathbf{n}\,dS
=\iiint_{E} \operatorname{div}\mathbf{F}\,dV,
\qquad
\operatorname{div}\mathbf{F}=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}.
$$
As a consequence, if $\operatorname{div}\mathbf{F}=0$ on a region, the net outward flux across any closed surface contained in that region is zero:
$$
\oint_{\partial E} \mathbf{F}\cdot \mathbf{n}\,dS=0.
$$
Similarly, if $\mathbf{F}=\nabla\times \mathbf{G}$ on a region, then for every closed surface $\partial E$ one has
$$
\oint_{\partial E} \mathbf{F}\cdot \mathbf{n}\,dS
=\iiint_E \operatorname{div}(\nabla\times \mathbf{G})\,dV=0.
$$

In differential form notation, the line integral of the 1–form $P\,dx+Q\,dy+R\,dz$ around $\partial S$ equals the surface integral of its exterior derivative:
$$
\oint_{\partial S} (P\,dx+Q\,dy+R\,dz)=\iint_S d(P\,dx+Q\,dy+R\,dz),
$$
which is Stokes’ theorem. For flux, using the 2–form $\omega=P\,dy\wedge dz+Q\,dz\wedge dx+R\,dx\wedge dy$, the divergence theorem reads
$$
\oint_{\partial E} \omega=\iiint_E d\omega,
\qquad
d\omega=(\operatorname{div}\mathbf{F})\,dx\wedge dy\wedge dz.
$$

For a positively oriented parameterization $\mathbf{r}(u,v)$, one may summarize the geometric identities as
$$
\mathbf{n}\,dS=\frac{\mathbf{r}_u\times \mathbf{r}_v}{\|\mathbf{r}_u\times \mathbf{r}_v\|}\,\|\mathbf{r}_u\times \mathbf{r}_v\|\,du\,dv=\big(\mathbf{r}_u\times \mathbf{r}_v\big)\,du\,dv,
$$
so that $\mathbf{F}\cdot \mathbf{n}\,dS=\mathbf{F}\cdot(\mathbf{r}_u\times \mathbf{r}_v)\,du\,dv$ and $dS=\|\mathbf{r}_u\times \mathbf{r}_v\|\,du\,dv$. These formulas are invariant under smooth re-parameterizations that preserve the chosen orientation; orientation–reversing re-parameterizations flip the sign of the flux integral.

---

## Problems

### **(Problem 01)**

Check the divergence theorem for the function: 

$$
\textbf{v} = r^2 \cos{\theta} \hat{\textbf{r}} + r^2 \cos{\phi} \hat{\boldsymbol \theta} - r^2 \cos{\theta}\sin{\phi} \hat{\boldsymbol \phi}
$$

using as your volume one octant of the sphere of radius $R$ below. Make sure you include
the entire surface. 

![[Pasted image 20251025113243.png]]

**Solution:**

We will start by manually determining the surface integral:
$$
\begin{aligned}
S_1: \hat{\textbf{n}}=-\hat{\textbf{y}}=-\sin\theta\sin\phi\,\hat{\mathbf r}
-\cos\theta\sin\phi\,\hat{\boldsymbol \theta}
-\cos\phi\,\hat{\boldsymbol \phi}, && \phi=0 && \theta=\left[0, \frac{\pi}{2}\right] && r=[0,R] \\
S_2: \hat{\textbf{n}}=-\hat{\textbf{z}}=-\cos\theta\,\hat{\mathbf r}
+\sin\theta\,\hat{\boldsymbol \theta}. && \phi=\left[0,\frac{\pi}{2}\right] && \theta=\frac{\pi}{2} && r=[0,R] \\ 
S_3 : \hat{\textbf{n}}=-\hat{\textbf{x}}=-\sin\theta\cos\phi\,\hat{\mathbf r}
-\cos\theta\cos\phi\,\hat{\boldsymbol \theta}
+\sin\phi\,\hat{\boldsymbol \phi} && \phi=\frac{\pi}{2} && \theta=\left[0,\frac{\pi}{2}\right] && r=[0,R] \\
S_4: \hat{\textbf{n}}=\hat{\textbf{r}} && \phi=\left[0, \frac{\pi}{2}\right] && \theta=\left[0, \frac{\pi}{2}\right] && r=R
\end{aligned}
$$
Note that the differential surface element is given by: 
$$
\begin{aligned}
r=\text{const}:&\quad dS=r^{2}\sin\theta\,d\theta\,d\phi,\\
\theta=\text{const}:&\quad dS=r\sin\theta\,dr\,d\phi,\\
\phi=\text{const}:&\quad dS=r\,dr\,d\theta.
\end{aligned}
$$

For $S_1$, we have $dS=r\, dr \, d\theta$, so, 

$$
\begin{aligned}
\iint_{S_1} \textbf{v} \cdot \hat{\textbf{n}} \cdot dS =\int_0^R \int_{0}^\frac{\pi}{2} \langle r^2 \cos{\theta}, r^2\cos{\phi}, -r^2 \cos{\theta}\sin{\phi} \rangle \\ \cdot \langle -\sin{\theta}\sin{\phi}, -\cos{\theta}\sin{\phi}, -\cos{\phi}\rangle r \cdot dr \cdot d\theta
\end{aligned}
$$
$$
\int_0^R \int_{0}^\frac{\pi}{2} \langle r^2 \cos{\theta}, r^2, 0 \rangle \cdot \langle 0, 0, -1\rangle r \cdot dr \cdot d\theta = 0
$$

For $S_2$ we have $dS=r\cdot dr \cdot d\phi$, so, 
$$
\iint_{S_2} \textbf{v} \cdot \hat{\textbf{n}} \cdot dS = \int_0^R \int_0^\frac{\pi}{2} \langle 0, r^2 \cos{\phi}, 0\rangle \cdot \langle 0, 1, 0\rangle r \cdot d\phi \cdot dr = \int_0^R \int_0^\frac{\pi}{2} r^3 \cos{\phi} \cdot d\phi\cdot dr 
$$
$$
\int_0^R r^3 \cdot dr = \frac{R^4}{4}
$$
For $S_3$, we have $dS=r\cdot dr \cdot d\theta$, 
$$
\iint_{S_3} \textbf{v} \cdot \hat{\textbf{n}} \cdot dS = \int_0^R \int_0^\frac{\pi}{2} \langle r^2\cos{\theta,} 0, -r^2\cos{\theta}\rangle \cdot \langle 0, 0, 1\rangle r \cdot d\phi \cdot dr 
$$

$$
\int_0^R \int_0^{\frac{\pi}{2}} -r^3 \cos{\theta} \cdot d\phi \cdot dr = -\frac{R^4}{4} 
$$

For $S_4$, we have $dS=r^2\sin{\theta} \cdot d\theta \cdot d\phi$,

$$
\iint_{S_4} \textbf{v} \cdot \hat{\textbf{n}} \cdot dS = \int_0^R \int_0^\frac{\pi}{2} \langle R^2\cos{\theta}, -R^2\cos{\phi},R^2\cos{\theta} \sin{\phi} \rangle \cdot \langle 1, 0, 0\rangle R^2 \sin{\theta}\cdot d\phi \cdot d\theta$$

$$
\int_0^\frac{\pi}{2} \int_0^\frac{\pi}{2} R^4 \cos{\theta}\sin{\theta} \cdot d\phi \cdot d\theta = \frac{\pi R^4}{2}
$$

So, the surface integral is $\dfrac{\pi R^4}{4}-\dfrac{R^4}{4}+\dfrac{R^4}{4}=\dfrac{\pi R^4}{4}$. 

We will now attempt to solve it using the divergence theorem. Starting by calculating the divergence: 

$$
\nabla \cdot \textbf{v} = \frac{1}{r^2}\frac{\partial}{\partial r} (r^3\cos{\theta}) + \frac{1}{r\sin{\theta}} \frac{\partial}{\partial \theta} \left(r^2\cos{\phi}\sin{\theta}\right)-\frac{1}{r\sin{\theta}}\frac{\partial}{\partial \phi}(r^2\cos{\theta}\sin{\phi})=4r\cos{\theta}
$$

The divergence theorem tells us:
$$
\oint_{\partial E} \mathbf{F}\cdot \mathbf{n}\,dS
=\iiint_{E} \operatorname{div}\mathbf{F}\,dV,
$$

And so, 

$$
\int_0^R \int_0^\frac{\pi}{2} \int_0^\frac{\pi}{2} 4r^3 \cos{\theta}\sin{\theta} \cdot d\theta \cdot d\phi \cdot dr = \int_0^R \int_0^{\frac{\pi}{2}} \left[-r^3 \cos{2\theta}\right]_0^\frac{\pi}{2} \cdot d\phi \cdot dr = \int_0^R \pi r^3 \cdot dr = \frac{\pi R^4}{4} 
$$

as expected. 

### **(Problem 02)**

Check the divergence theorem for the function
$$\textbf{v}=r^2\sin{\theta} \hat{\textbf{r}}+4r^2\cos{\theta} \hat{\boldsymbol \theta}+r^2\tan{\theta}\hat{\boldsymbol \phi}$$using the volume of the "ice-cream cone" shown below. the top surface is spherical, with
radius $R$ and centered at the origin.

![[Pasted image 20251025224244.png]]

**Solution:**

By geometry, we have: 

$$
\begin{aligned}
\frac{r}{z}=\cos{\left(\frac{\pi}{6}\right)} \\
2\sqrt{x^2+y^2+z^2} = \sqrt{3}z \\
z^2-3x^2-3y^2=0
\end{aligned}
$$

Turning it into a level surface $F(x,y,z)$:

$$
\begin{aligned}
\nabla F = -6x \hat{\textbf{x}} - 6y \hat{\textbf{y}} + 2z \hat{\textbf{z}} 
\end{aligned}
$$

To determine in spherical coordinates: 

$$
\begin{aligned}
(\nabla F) \cdot \hat{\textbf{r}} = \langle -6x, -6y, 2z\rangle \cdot \langle \sin{\theta}\cos{\phi}, \sin{\theta}\sin{\phi}, \cos{\theta} \rangle
=-6x\sin{\theta}\cos{\phi}-6y\sin{\theta}\sin{\phi} + 2z\cos{\theta} \\ 
=-6r\sin^2{\theta}\cos^2{\phi}-6r\sin^2{\theta}\sin^2{\phi}+2r\cos^2{\theta} =-6r\sin^{2}\theta+2r\cos^2{\theta}=-8r\sin^{2}\theta + 2r \\ 
-8r+8r\cos^2{\theta} +2r=8r\cos^2{\theta} - 6r 
\end{aligned} 
$$
$$
\begin{aligned}
(\nabla F) \cdot \hat{\boldsymbol \theta} = \langle -6x, -6y, 2z\rangle \cdot \langle \cos{\theta}\cos{\phi}, \cos{\theta}\sin{\phi}, -\sin{\theta} \rangle \\= -6r\sin{\theta}\cos{\theta}\cos^2{\phi}-6r\cos{\theta}\sin{\theta}\sin^2{\phi}-2r\cos{\theta}\sin{\theta} \\= -3r\sin{2\theta}\cos^2{\phi}-3r\sin{2\theta}\sin^2{\phi}-r\sin{2\theta}=-3r\sin{2\theta}-r\sin{2\theta}=-8r\sin\theta \cos \theta
\end{aligned}
$$

$$
(\nabla) \cdot \hat{\boldsymbol \phi} = \langle -6x,-6y,2z \rangle \cdot \langle -\sin{\phi}, \cos{\phi},0 \rangle = 6r\sin{\theta}\cos{\phi}\sin{\phi}+6r\sin{\theta}\cos{\phi}\sin{\phi}=0
$$

So, the normal vector is: 
$$
\textbf{n} =(8r\cos^2{\theta}-6r)\hat{\textbf{r}}-(8r\sin{\theta}\cos{\theta})\hat{\boldsymbol \theta}
$$

The magnitude of this vector is:

$$
\begin{aligned}
||\textbf{n}||=\sqrt{64r^2\cos^4{\theta} -96r^2\cos^2{\theta}+36r^2+64r^2\sin^2{\theta} \cos^2{\theta}} \\ 
=\sqrt{64r^2\cos^2{\theta}-96r^2\cos^2{\theta}+36r^2}=\sqrt{36r^2-32r^2\cos^2{\theta}}=2r\sqrt{9-8\cos^2{\theta}}
\end{aligned}
$$

So, the unit normal vector is:

$$
\hat{\textbf{n}}= \frac{4\cos^2{\theta}-3}{\sqrt{5-4\cos^2{\theta}}} \hat{\textbf{r}} - \frac{4\sin\theta\cos\theta}{\sqrt{5-4\cos^2{\theta}}}\hat{\boldsymbol \theta}
$$

Finally, we can start with the surface integrals. 

Starting with $S_1$ defined for the cone: $\theta$=$\pi /6$, $r=[0,R]$, and $\phi=[0,2\pi]$. The unit normal vector (with this $\theta$) is: 

$$
\hat{\textbf{n}}=\frac{4\cdot \dfrac{3}{4}-3}{\sqrt{5-4\cdot \dfrac{3}{4}}}\hat{\textbf{r}}-\frac{4 \cdot \dfrac{1}{2} \cdot \dfrac{\sqrt{3}}{2}}{\sqrt{5-4\cdot \dfrac{3}{4}}}\hat{\boldsymbol{\theta}}=-\hat{\boldsymbol{\theta}}
$$

$$
\begin{aligned}
\int_0^{2\pi} \int_0^R \langle r^2\sin{\theta}, 4r^2\cos{\theta}, r^2\tan{\theta} \rangle \cdot \langle 0,1,0 \rangle r\sin{\theta} \cdot dr \cdot d\phi \\=\int_0^{2\pi} \int_0^R \sqrt{3}r^3\sin{2\theta} \cdot dr \cdot d\phi
=\int_0^{2\pi} \frac{\sqrt{3}}{4}R^4 \cdot d\phi = \frac{\pi\sqrt{3}}{2} R
\end{aligned}
$$


And with $S_2$, defined for the sphere centered at the origin: 

$$
\hat{\textbf{n}}=\hat{\textbf{r}}
$$

With $r=R$, $\theta = [0,2\pi]$, and $\phi=[0,\pi]$, 

$$
\int_0^{2\pi} \int_0^\pi \langle r^2\sin{\theta},4r^2\cos{\theta},r^2\tan{\theta} \rangle \cdot \langle 1,0,0\rangle \cdot r^2\sin{\theta} \cdot d\theta \cdot d\phi = \int_0^{2\pi} \int_0^\pi r^4\sin^2{\theta} \cdot d\theta \cdot d\phi
$$

$$
\begin{aligned}
\int_0^{2\pi} \int_0^{\frac{\pi}{6}} \frac{1}{2}R^4 (1-\cos{2\theta}) \cdot d\theta \cdot d\phi =\int_0^{2\pi} \left[\frac{R^4}{2}\theta-\frac{R^4}{4}\sin{2\theta} \right]_0^{\frac{\pi}{6}} \cdot d\phi = \int_0^{2\pi} \frac{\pi R^4}{12}-\frac{R^4\sqrt{3}}{8} \cdot d\phi \\
=\frac{2\pi^2 R^4}{12} - \frac{\pi R^4 \sqrt{3}}{4} = \frac{\pi R^4}{12} (2\pi-3\sqrt{3})
\end{aligned}
$$

Now, we will attempt to derive a similar result using the divergence theorem. Start by determining the divergence: 


$$
\begin{aligned}
\hat{\textbf{r}}: && \frac{1}{r^{2}}\frac{\partial}{\partial r}\!\left(r^{2}\textbf{v}_r\right)
&=\frac{1}{r^{2}}\frac{\partial}{\partial r}\!\left(r^{4}\sin\theta\right)
=4r\sin\theta,\\
\hat{\boldsymbol \theta}: &&\frac{1}{r\sin\theta}\frac{\partial}{\partial\theta}\!\left(\sin\theta\,\textbf{v}_\theta\right)
&=\frac{1}{r\sin\theta}\frac{\partial}{\partial\theta}\!\left(4r^{2}\sin\theta\cos\theta\right)
=\frac{4r\cos 2\theta}{\sin\theta},\\
\hat{\boldsymbol \phi}: && \frac{1}{r\sin\theta}\frac{\partial \textbf{v}_\phi}{\partial\phi}&=0.
\end{aligned}
$$

$$
\;\nabla\!\cdot\!\mathbf v
=4r\sin\theta+\frac{4r\cos 2\theta}{\sin\theta}
=\frac{4r\cos^{2}\theta}{\sin\theta}\;
$$

And setting up the triple integral:
$$
\begin{aligned}
\int_0^{2\pi} \int_0^{\frac{\pi}{6}}\int_0^R \frac{4r^3\cos^2{\theta}}{\sin{\theta}} \sin{\theta} \cdot dr \cdot d\theta \cdot d\phi = \int_0^{2\pi}\int_0^{\frac{\pi}{6}} R^4\cos^2{\theta} \cdot d\theta \cdot d\phi \\ 
=\int_0^{2\pi} \int_0^{\frac{\pi}{6}} \frac{R^4}{2} +\frac{R^4}{2}\cos{2\theta} \cdot d\theta \cdot d\phi =\int_0^{2\pi} \frac{\pi R^4}{6}+\frac{R^4\sqrt{3}}{8} \cdot d\phi = \frac{2\pi^2 R^4}{12}+\frac{\pi R^4 \sqrt{3}}{4} \\
=\frac{\pi R^4}{12}(2\pi+3\sqrt{3}) 
\end{aligned}
$$

As expected. 