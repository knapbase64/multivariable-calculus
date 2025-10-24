A scalar potential for a vector field $\mathbf{F}$ on an open set $U\subset\mathbb{R}^n$ is a function $\phi:U\to\mathbb{R}$ such that $\mathbf{F}=\nabla\phi$. A vector field that admits such a $\phi$ is called conservative. For a piecewise smooth curve $C$ with parameterization $\mathbf{r}:[a,b]\to U$ and endpoints $\mathbf{r}(a)=\mathbf{a}$, $\mathbf{r}(b)=\mathbf{b}$, the fundamental theorem for line integrals states that
$$
\int_C \mathbf{F}\cdot d\mathbf{r}
=\int_a^b \nabla\phi(\mathbf{r}(t))\cdot \mathbf{r}'(t)\,dt
=\phi(\mathbf{b})-\phi(\mathbf{a}),
$$
so the work done by $\mathbf{F}$ depends only on the endpoints. Conversely, if the line integral $\int_C \mathbf{F}\cdot d\mathbf{r}$ is independent of the path between any two points of a connected open set $U$, then there exists a potential $\phi$ with $\nabla\phi=\mathbf{F}$, and $\phi$ is unique up to an additive constant. Choosing a base point $\mathbf{x}_0\in U$ and fixing $\phi(\mathbf{x}_0)$, one may define
$$
\phi(\mathbf{x})=\phi(\mathbf{x}_0)+\int_{\gamma_{\mathbf{x}_0\to \mathbf{x}}}\mathbf{F}\cdot d\mathbf{r},
$$
where $\gamma_{\mathbf{x}_0\to \mathbf{x}}$ is any piecewise smooth path from $\mathbf{x}_0$ to $\mathbf{x}$. When $\mathbf{F}$ is conservative this is well defined because the integral is path independent.

In three dimensions the curl provides a differential test for the existence of a potential. If $\mathbf{F}=\langle P,Q,R\rangle$ has continuous first partial derivatives on a simply connected open set $U\subset\mathbb{R}^3$, then
$$
\nabla\times \mathbf{F}=\mathbf{0}\quad\Longleftrightarrow\quad \mathbf{F}=\nabla\phi\ \text{for some }\phi:U\to\mathbb{R}.
$$
Equivalently, on such a domain, the necessary conditions
$$
\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}=0,\qquad
\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}=0,\qquad
\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=0
$$
are also sufficient. In the plane the analogous statement is that, for $\mathbf{F}=\langle P,Q\rangle$ with continuous partials on a simply connected open set $U\subset\mathbb{R}^2$, the condition
$$
\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}
$$
is necessary and sufficient for the existence of $\phi$ with $\nabla\phi=\mathbf{F}$. The topology of the domain matters; the equalities above are necessary on any domain, but without simple connectivity they do not guarantee a global potential, because integrals around nontrivial closed loops may fail to vanish.

Once existence is assured, potentials can be constructed in several equivalent ways. A direct method integrates components and enforces consistency across partial derivatives. In three dimensions one begins by integrating $P$ with respect to $x$,
$$
\phi(x,y,z)=\int P(x,y,z)\,dx+g(y,z),
$$
where $g$ is independent of $x$. Differentiating this expression with respect to $y$ and matching $\partial\phi/\partial y$ with $Q$ determines $g_y$, which can then be integrated in $y$ to recover $g$ up to a function $h(z)$. Finally, differentiating with respect to $z$ and matching $\partial\phi/\partial z$ with $R$ determines $h$ up to an additive constant, thereby fixing $\phi$ up to the chosen normalization. In two dimensions the same idea reads
$$
\phi(x,y)=\int P(x,y)\,dx+g(y),\qquad
\frac{\partial \phi}{\partial y}=Q(x,y)\ \Rightarrow\ g'(y)=Q(x,y)-\frac{\partial}{\partial y}\!\left(\int P(x,y)\,dx\right),
$$
and integrating $g'(y)$ in $y$ yields $\phi$ up to a constant, provided the mixed-partial compatibility holds.

A path-integral formula is often computationally convenient. Fixing $(x_0,y_0,z_0)\in U$ and using a piecewise linear path that moves first along the $x$-axis, then along $y$, then along $z$, one obtains
$$
\begin{aligned}
\phi(x,y,z)=\phi(x_0,y_0,z_0)
&+\int_{x_0}^{x} P(s,y_0,z_0)\,ds
+\int_{y_0}^{y} Q(x,t,z_0)\,dt
+\int_{z_0}^{z} R(x,y,u)\,du,
\end{aligned}
$$
which is valid when the integral is path independent; any other convenient path yields the same value. On a star-shaped domain containing the origin one may also use the straight-line path to write the compact radial formula
$$
\phi(\mathbf{x})=\int_0^1 \mathbf{F}(t\mathbf{x})\cdot \mathbf{x}\,dt,
$$
or with an arbitrary base point $\mathbf{x}_0$,
$$
\phi(\mathbf{x})=\phi(\mathbf{x}_0)+\int_0^1 \mathbf{F}\big(\mathbf{x}_0+t(\mathbf{x}-\mathbf{x}_0)\big)\cdot (\mathbf{x}-\mathbf{x}_0)\,dt.
$$
Differentiating any of these expressions under the integral sign recovers $\nabla\phi=\mathbf{F}$.

The equivalence between zero curl and path independence is a direct consequence of Stokes’ theorem. If $\nabla\times \mathbf{F}=\mathbf{0}$ on a region and $C$ is any closed curve that bounds an oriented smooth surface $S$, then
$$
\oint_C \mathbf{F}\cdot d\mathbf{r}
=\iint_S (\nabla\times \mathbf{F})\cdot \mathbf{n}\,dS
=0,
$$
so $\int_C \mathbf{F}\cdot d\mathbf{r}$ vanishes for every contractible loop. On simply connected domains every closed loop is contractible, and hence the line integral depends only on endpoints. Conversely, if all closed-loop integrals vanish, then Stokes’ theorem implies $\iint_S (\nabla\times \mathbf{F})\cdot \mathbf{n}\,dS=0$ for every surface $S$, which forces $\nabla\times \mathbf{F}=\mathbf{0}$. In the plane, Green’s theorem gives the criterion
$$
\oint_{\partial D} \mathbf{F}\cdot d\mathbf{r}
=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\,dA,
$$
so the vanishing of the scalar curl over every region $D$ yields path independence and hence a potential.

In differential-form language determining a potential means deciding whether the 1-form $\omega=P\,dx+Q\,dy+R\,dz$ is exact. The exterior derivative is
$$
d\omega=\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\,dx\wedge dy
+\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)\,dy\wedge dz
+\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)\,dz\wedge dx,
$$
so $d\omega=0$ is the coordinate-free statement that $\nabla\times\mathbf{F}=\mathbf{0}$. 

---

## Example

**Problem.** Given the vector field
$$
\mathbf F(x,y,z)=\langle yz+2x,\; xz+2y,\; xy+2z\rangle,
$$
find a scalar potential $\phi$ on $\mathbb R^{3}$ such that $\nabla\phi=\mathbf F$.

**Solution.** Because the components of $\mathbf F$ have continuous first partial derivatives on $\mathbb R^{3}$ and the domain is simply connected, it suffices to check that the curl vanishes. Compute
$$
\begin{aligned}
\nabla\times\mathbf F=
\Big\langle \partial_y(xy+2z)-\partial_z(xz+2y),\;
\partial_z(yz+2x)-\partial_x(xy+2z),\;
\partial_x(xz+2y)-\partial_y(yz+2x)\Big\rangle \\
=\langle x-x,\; y-y,\; z-z\rangle=\mathbf 0,
\end{aligned}
$$
so a potential exists.

To construct $\phi$, integrate the first component with respect to $x$ and include an $x$–independent function:
$$
\phi(x,y,z)=\int (yz+2x)\,dx=xyz+x^{2}+g(y,z).
$$
Differentiate this expression with respect to $y$ and match the second component $F_2=xz+2y$ to obtain
$$
\phi_y=xz+g_y(y,z)=xz+2y \quad\Rightarrow\quad g_y(y,z)=2y,
$$
which integrates to $g(y,z)=y^{2}+h(z)$ for some function $h$. Differentiate with respect to $z$ and match the third component $F_3=xy+2z$ to obtain
$$
\phi_z=xy+h'(z)=xy+2z \quad\Rightarrow\quad h'(z)=2z \quad\Rightarrow\quad h(z)=z^{2}+C.
$$
Combining these pieces gives a potential
$$
\phi(x,y,z)=xyz+x^{2}+y^{2}+z^{2}+C
$$
and a direct computation verifies that $\nabla\phi=\langle yz+2x,\; xz+2y,\; xy+2z\rangle=\mathbf F$.
