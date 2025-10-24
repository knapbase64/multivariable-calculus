For a scalar function $T(x,y,z)$ that changes infinitesimally by $dT$ with variables $x, y, z$ that change infinitesimally by $dx, dy, dz$, 

$$
dT = \left(\frac{\partial T}{\partial x}\right) dx + \left(\frac{\partial T}{\partial y}\right) dy + \left(\frac{\partial T}{\partial z}\right) dz
$$
$$
dT = \left(\frac{\partial T}{\partial x}\hat{\textbf{x}} + \frac{\partial T}{\partial y}\hat{\textbf{y}}+\frac{\partial T}{\partial z}\hat{\textbf{z}}\right) \cdot \left(dx \hat{\textbf{x}}+dy \hat{\textbf{y}}+dz \hat{\textbf{z}}\right)=(\nabla T) \cdot (d\textbf{l})
$$

The quantity $\nabla T$ here is a *vector*, which is the generalized derivative of $T$. 

The gradient $\nabla T$ points in the direction of maximum increase of the function $T$. The magnitude $|\nabla T|$ gives the slope (rate of increase) along this maximal direction.  

Because $dT=\nabla T\cdot d\mathbf{l}$, any infinitesimal displacement $d\mathbf{l}$ that stays on a level surface $T(x,y,z)=k$ makes no change in $T$, so $\nabla T\cdot d\mathbf{l}=0$ and the gradient is perpendicular to the surface at that point. 

If $a\hat{\textbf{x}}+b\hat{\textbf{y}}+c\hat{\textbf{z}}$ lies on $T=k$ and $\nabla T(a,b,c)\neq \mathbf{0}$, the tangent plane therefore has normal vector $\nabla T(a,b,c)$ and satisfies

$$
\nabla T(a,b,c)\cdot\big((x-a)\hat{\textbf{x}}+(y-b)\hat{\textbf{y}}+(z-c)\hat{\textbf{z}})\big)=0,
$$

If a surface is given implicitly by an equation $F(x,y,z)=0$, the same idea applies with $T=F$. At a point $(a,b,c)$ on the surface with $(F_x,F_y,F_z)(a,b,c)\neq(0,0,0)$, the tangent plane equation is 

$$
F_x(a,b,c)\,(x-a)+F_y(a,b,c)\,(y-b)+F_z(a,b,c)\,(z-c)=0.
$$

If a surface is the graph of a function $z=f(x,y)$, the total differential gives the best linear approximation near $(a,b)$ and yields the tangent plane at $(a,b,f(a,b))$,

$$
z=f(a,b)+f_x(a,b)\,(x-a)+f_y(a,b)\,(y-b).
$$

The same plane can be written in normal-vector form as

$$
(-f_x(a,b),-f_y(a,b),1)\cdot\big((x-a),(y-b),(z-f(a,b))\big)=0.
$$

If a surface is given by a parameterization $\mathbf{r}(u,v)=\langle x(u,v),y(u,v),z(u,v)\rangle$, then the two derivative vectors $\mathbf{r}_u(u_0,v_0)$ and $\mathbf{r}_v(u_0,v_0)$ are tangent directions at $\mathbf{r}(u_0,v_0)$. 

When these two vectors are not multiples of each other, they span the tangent plane, and a convenient point–normal form is

$$
\big(\mathbf{r}_u(u_0,v_0)\times\mathbf{r}_v(u_0,v_0)\big)\cdot\big(\mathbf{r}-\mathbf{r}(u_0,v_0)\big)=0,
$$

while a point–direction form that shows the spanning directions explicitly is

$$
\mathbf{r}=\mathbf{r}(u_0,v_0)+s\,\mathbf{r}_u(u_0,v_0)+t\,\mathbf{r}_v(u_0,v_0).
$$

If a space curve is given by a parameterization $\mathbf{r}(t)$, the velocity $\mathbf{r}'(t_0)$ points along the curve, so the tangent line at $t_0$ passes through $\mathbf{r}(t_0)$ with direction $\mathbf{r}'(t_0)$ and can be written as

$$
\mathbf{\ell}(s)=\mathbf{r}(t_0)+s\,\mathbf{r}'(t_0).
$$

If a curve is the intersection of two surfaces $F(x,y,z)=0$ and $G(x,y,z)=0$, then at a point $(a,b,c)$ where the gradients $\nabla F$ and $\nabla G$ are both nonzero and not parallel, the tangent direction is perpendicular to both gradients, which is captured by the cross product. 

A parametric form for the tangent line is

$$
(x,y,z)=(a,b,c)+s\big(\nabla F(a,b,c)\times\nabla G(a,b,c)\big).
$$

If a plane level curve is given by $f(x,y)=k$, then at a point $(a,b)$ with $(f_x,f_y)(a,b)\neq(0,0)$ the gradient $(f_x,f_y)$ is perpendicular to the curve, so the tangent line in the $xy$-plane satisfies

$$
f_x(a,b)\,(x-a)+f_y(a,b)\,(y-b)=0,
$$

and, when $f_y(a,b)\neq 0$, the usual slope with respect to $x$ follows by implicit differentiation,
$$
\frac{dy}{dx}\Big|_{(a,b)}=-\frac{f_x(a,b)}{f_y(a,b)}.
$$

---

## Examples

**Example 1.** Find the tangent plane to the graph
$$
z=f(x,y)=\ln(xy+1)+x^2-y
$$
at the point $(1,1,\ln 2)$. Write the plane in the linearization form
$$
z=f(1,1)+f_x(1,1)\,(x-1)+f_y(1,1)\,(y-1)
$$
and also in the point–normal form
$$
A(x-1)+B(y-1)+C\big(z-\ln 2\big)=0,
$$
identifying the normal vector $(A,B,C)$.

**Solution:**

In linearization form:

$$
\begin{aligned}
z=\ln(2) + \left[\frac{\partial(\ln(xy+1))}{\partial(xy+1)} \cdot \frac{\partial(xy+1)}{\partial x} + \frac{\partial(x^2-y)}{\partial x}\right]_{(x,y)=(1,1)} (x-1)+\\
\left[\frac{\partial(\ln(xy+1))}{\partial(xy+1)} \cdot \frac{\partial(xy+1)}{\partial y} + \frac{\partial (x^2-y)}{\partial y}\right]_{(x,y)=(1,1)} (y-1)
\end{aligned}
$$

$$
z=\ln{2} + \frac{5}{2}(x-1) - \frac{1}{2}(y-1) 
$$
In normal-vector form: 

$$
\begin{aligned}
\left(-\frac{5}{2}, \frac{1}{2},1\right) \cdot \left((x-1),(y-1),(z-\ln{2})\right) \\ 
= -\frac{5}{2}(x-1) +\frac{1}{2} (y-1) + (z-\ln{2})=0
\end{aligned}
$$

**Example 2.** Consider the level surface defined implicitly by
$$
F(x,y,z)=\sin(xy)+z\ln x-3=0.
$$
Verify that $(e,0,3)$ lies on the surface and that $\nabla F(e,0,3)\neq \mathbf{0}$. Find the tangent plane at $(e,0,3)$ using
$$
F_x(e,0,3)\,(x-e)+F_y(e,0,3)\,(y-0)+F_z(e,0,3)\,(z-3)=0,
$$
and then give a unit normal vector to this plane.

**Solution:**

$$
F_x(x,y,z)=y\cos{xy} + \frac{z}{x} \Rightarrow F_x(e,0,3)=\frac{3}{e}
$$
$$
F_y(x,y,z)=x\cos{xy} \Rightarrow F_y(e,0,3)=e
$$
$$
F_z(x,y,z)=\ln{x} \Rightarrow F_z(e,0,3)=1
$$

So, 

$$
3e^{-1}(x-e)+ey + (z-3)=0
$$
The unit normal is: 
$$
\hat{\textbf{n}} = \frac{\langle 3e^{-1},e,1 \rangle}{\sqrt{9e^{-2}+e^2+1^2}}=\frac{\langle3,e^2,e\rangle}{\sqrt{9+e^4+e^2}}
$$

**Example 3.** Let the curve $\mathcal{C}$ be the intersection of the sphere
$$
x^2+y^2+z^2=3
$$
and the saddle surface
$$
z=xy.
$$
Show that the point $(1,1,1)$ lies on $\mathcal{C}$. Find a direction vector for the tangent line to $\mathcal{C}$ at $(1,1,1)$ using the cross product of the gradients of the two defining surfaces at that point, and then write a parametric equation for the tangent line

$$
(x,y,z)=(1,1,1)+s\,\mathbf{v}.
$$

**Solution:**

$$
\begin{aligned}
\nabla F = 2x\hat{\textbf{x}}+2y\hat{\textbf{y}}+2z\hat{\textbf{z}} \\ 
\nabla F(1,1,1) = 2\hat{\textbf{x}}+2\hat{\textbf{y}}+2\hat{\textbf{z}}
\end{aligned}
$$
$$
\begin{aligned}
\nabla G = y\hat{\textbf{x}}+x\hat{\textbf{y}}-\hat{\textbf{z}} \\ 
\nabla G(1,1,1) = 1\hat{\textbf{x}}+1\hat{\textbf{y}} - 1\hat{\textbf{z}}
\end{aligned}
$$
$$
\nabla F(1,1,1) \times \nabla G(1,1,1) = \begin{vmatrix}
\hat{\textbf{x}} & \hat{\textbf{y}} & \hat{\textbf{z}} \\
2 & 2 & 2 \\ 
1 & 1 & -1
\end{vmatrix}=-4\hat{\textbf{x}}+4\hat{\textbf{y}}
$$
$$
r(t)=\langle 1,1,1 \rangle + s \langle1,-1,0\rangle
$$

**Example 4.** Consider the parametrized surface
$$
\mathbf{r}(u,v)=\big(u\cos v,\,u\sin v,\,2v+u^2v\big).
$$
Evaluate $\mathbf{r}(1,0)$ and the partial derivative vectors $\mathbf{r}_u(1,0)$ and $\mathbf{r}_v(1,0)$. Confirm that these two tangent directions are not collinear and find the tangent plane at $\mathbf{r}(1,0)$ in the point–direction form
$$
\mathbf{r}=\mathbf{r}(1,0)+s\,\mathbf{r}_u(1,0)+t\,\mathbf{r}_v(1,0),
$$

**Solution:**

$$
\textbf{r}(1,0)=\langle 1, 0, 0 \rangle
$$
$$
\begin{aligned}
\textbf{r}_u = \langle\cos{v}, \sin{v}, 2uv\rangle \\ 
\textbf{r}_v = \langle -u\sin{v},u\cos{v},2+u^2\rangle \\ 
\textbf{r}_u(1,0) = \langle 1,0,0\rangle \\ 
\textbf{r}_v(1,0) = \langle 0,1,3\rangle \\ 
\end{aligned}
$$

They are not collinear. In point-direction form: 
$$
\textbf{r} = \langle 1,0,0\rangle + s \langle 1,0,0 \rangle + t \langle 0,1,3 \rangle
$$

**Example 5.** The height of a certain hill (in feet) is given by
$$h(x,y)=10(2xy-3x^2-4y^2-18x+28y+12)$$
where $y$ is the distance (in miles) north, $x$ the distance east. 
1. Where is the top of the hill located? 
2. How high is the hill? 
3. How steep is the slope (in feet per mile) at a point 1 mile north and one mile east of South Hadley? In what direction is the slope steepest, at that point? 

**Solution:**

Gradient vector is:

$$
\nabla h=(20y-60x-180)\hat{\textbf{x}} + (20x-80y+280)\hat{\textbf{y}}
$$
$$
\begin{aligned}
y-3x-9 = 0 \Rightarrow y=3x+9 \\ 
x-4y+14=0 \Rightarrow x-12x-36+14 = 0 \\ 
x = -2
\end{aligned}
$$
And we get $y=3$. The height is $h(-2,3)=10(2(-2)(3)-12+84+12)=720$. 
$$
\nabla h(1,1)=(20-60-180)\hat{\textbf{x}}+(20-80+280)\hat{\textbf{y}}=-220\hat{\textbf{x}}+220\hat{\textbf{y}}
$$
The direction is at $(-1,1)$, the unit direction is:
$$
\left\langle -\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}} \right\rangle
$$
