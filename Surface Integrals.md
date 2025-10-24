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
so that $\mathbf{F}\cdot \mathbf{n}\,dS=\mathbf{F}\cdot(\mathbf{r}_u\times \mathbf{r}_v)\,du\,dv$ and $dS=\|\mathbf{r}_u\times \mathbf{r}_v\|\,du\,dv$. These formulas are invariant under smooth reparameterizations that preserve the chosen orientation; orientation–reversing reparameterizations flip the sign of the flux integral.

---


