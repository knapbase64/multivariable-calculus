A line integral of a vector field $\mathbf{v}$ along a curve $C$ parameterized by $\mathbf{r}:[a,b]\to\mathbb{R}^3$ is
$$
\int_{C}\mathbf{v}\cdot d\mathbf{r}
=\int_a^b \mathbf{v}(\mathbf{r}(t))\cdot \mathbf{r}'(t)\,dt.
$$

If $C$ is a closed curve (i.e., $\mathbf{r}(a)=\mathbf{r}(b)$), we write
$$
\oint_C \mathbf{v}\cdot d\mathbf{r}.
$$

A scalar line integral with respect to arc length is
$$
\int_C f\,ds=\int_a^b f(\mathbf{r}(t))\,\|\mathbf{r}'(t)\|\,dt,
\qquad t\in [a,b],
$$
where $ds=\|d\mathbf{r}\|$. 

Given a path $C$ composed of multiple paths $C_1$ and $C_2$, the line integral on $C$ is nothing more than:

$$
\int_C \textbf{v}\cdot d\textbf{r}=\int_{C_1} \textbf{v} \cdot d\textbf{r}+\int_{C_2} \textbf{v} \cdot d\textbf{r}
$$

For planar fields, Green's theorem connects a closed line integral to a double integral over the enclosed region. Let $\mathbf{F}(x,y)=\langle P(x,y),Q(x,y)\rangle$ have continuous partial derivatives on an open set containing a bounded region $D\subset\mathbb{R}^2$ whose positively oriented boundary is the simple, piecewise smooth closed curve $C=\partial D$ (counterclockwise orientation). Then
$$
\oint_{C} P\,dx+Q\,dy
=\iint_{D}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\,dA.
$$
Equivalently, writing $\operatorname{curl}\mathbf{F}=\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}$ (the $k$-component of the 3D curl of $\langle P,Q,0\rangle$), the circulation form is
$$
\oint_C \mathbf{F}\cdot \mathbf{T}\,ds=\iint_D \operatorname{curl}\mathbf{F}\,dA,
$$
where $\mathbf{T}$ is the unit tangent consistent with the positive orientation. There is also the flux form: with outward unit normal $\mathbf{n}$ along $C$,
$$
\oint_C \mathbf{F}\cdot \mathbf{n}\,ds
=\iint_D \operatorname{div}\mathbf{F}\,dA,
\qquad
\operatorname{div}\mathbf{F}=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}.
$$
In differential form notation these identities are
$$
\oint_C P\,dx+Q\,dy=\iint_D d(P\,dx+Q\,dy),
\qquad
\oint_C P\,dy-Q\,dx=\iint_D\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}\right)\,dA,
$$
and for a positively oriented parameterization $x=x(t),y=y(t)$ one has the identities $\mathbf{T}\,ds=\langle dx,dy\rangle$ and $\mathbf{n}\,ds=\langle dy,-dx\rangle$.

If $D$ has holes bounded by simple closed curves $C_1,\dots,C_m$ inside an outer boundary $C_0$, orient $C_0$ counterclockwise and each inner boundary clockwise; then the same formulas hold with $\partial D=C_0\cup C_1\cup\cdots\cup C_m$ and the line integral understood as the sum over all boundary components.

Two basic consequences are worth recording. If $\operatorname{curl}\mathbf{F}=0$ on a simply connected region, then $\oint_C \mathbf{F}\cdot d\mathbf{r}=0$ for every closed $C$ in that region, so $\int_C \mathbf{F}\cdot d\mathbf{r}$ depends only on endpoints and $\mathbf{F}$ is conservative ($\mathbf{F}=\nabla \varphi$ for some potential $\varphi$). If $\operatorname{div}\mathbf{F}=0$ on a region, then the net outward flux across any closed curve contained in that region is zero:
$$
\oint_C \mathbf{F}\cdot \mathbf{n}\,ds=0.
$$

--- 

## Problems

### **(Problem 01)** 

Calculate the line integral of the function $\textbf{v}=y^2\hat{\textbf{x}}+2x(y+1)\hat{\textbf{y}}$ along the path from $\textbf{a}$ to $\textbf{b}$ as shown in the image below: 

![[Pasted image 20251021221457.png]]

**Solution:** 

Divide the path into $C_1$ and $C_2$ such that $C_1: \langle 1,1\rangle \to \langle 2,1\rangle$ and $C_2: \langle 2,1\rangle \to \langle 2,2\rangle$. 

The path along $C_1$ can be expressed as: 

$$
r(t)=\langle 1,1 \rangle + t\langle 1, 0 \rangle = \langle 1+t, 1 \rangle, \qquad t\in [0,1]
$$

And so, $r'(t)=\langle 1, 0 \rangle$, and $\textbf{v}(r(t))=\langle 1, 4+4t \rangle$. Thus, the line integral along $C_1$ is:

$$
\int_{C_1} \textbf{v} \cdot r'(t) \cdot dt = \int_0^1 1\cdot dt = 1
$$

Next, the path along $C_2$ can be expressed as:
$$
r(t)= \langle 2, 1+t \rangle \qquad t \in [0,1]
$$
And so, $r'(t)=\langle 0, 1 \rangle$, and $\textbf{v}(r(t))=\langle (1+t)^2, 8+4t\rangle$. Thus, the line integral along $C_2$ is: 

$$
\int_{C_2} \textbf{v} \cdot r'(t) \cdot dt = \int_0^1 8+4t \cdot dt = 8+2=10
$$

The total line integral is: $10+1=11$. 

We now define $C_3: \langle 1,1 \rangle \to \langle 2,2 \rangle$, so we parameterize the path as:
$$
r(t)=\langle 1+t, 1+t\rangle \qquad t\in[0,1]
$$
And again, $r'(t)=\langle 1, 1 \rangle$ and $\textbf{v}(r(t))=\langle (1+t)^2, 2(1+t)(2+t)\rangle$ 

So,

$$
\int_{C_3} \textbf{v} \cdot r'(t) \cdot dt = \int_0^1 t^2+2t+1+2(2+t+2t+t^2) \cdot dt = \int_0^1 t^2 + 2t+1+4+6t+2t^2 \cdot dt
$$

$$
\int_0^1 3t^2+8t+5\cdot dt = 1+4+5 = 10
$$

Reversing the orientation of this path ($-C_3: \langle 2,2 \rangle \to \langle 1,1 \rangle$), the line integral is $-10$ (this can easily be verified as shown below): 

The reverse orientation of $C_3$ can be parameterized as $\langle 2-t, 2-t \rangle$ for $t\in [0,1]$. We have $r'(t)=\langle -1,-1 \rangle$ and $\textbf{v}(r(t))=\langle (2-t)^2, 2(2-t)(3-t) \rangle$, 

$$
\int_0^1 -1\cdot (t^2-4t+4) - 2(6-5t+t^2) \cdot dt
$$
$$= \int_0^1 -t^2-2t^2+4t+10t-4-12 \cdot dt = 1 + 7 - 18 =-10
$$
As hypothesized. 

So, if we form a closed loop going from $C: C_1\to C_2 \to -C_3$, the loop integral with the path $C$ reduces to the sum of three line integrals: 

$$
\oint_C \textbf{v}\cdot d\textbf{r} = \int_{C_1} \textbf{v} \cdot \textbf{dr}+\int_{C_2} \textbf{v} \cdot \textbf{dr} -\int_{C_3} \textbf{v} \cdot \textbf{dr} =11-10=1
$$

### **(Problem 02)** 

Compute the scalar line integral
$$
\int_{C} x\,y\,z^{2}\, ds
$$
where $C$ is the straight line segment from $(1,1,0)$ to $(2,3,1)$.

**Solution:** 

Parameterize the segment by
$$
\mathbf r(t)=(1+t,\;1+2t,\;t),\qquad 0\le t \le 1,
$$

so that $\mathbf r'(t)=(1,2,1)$ and $\|\mathbf r'(t)\|=\sqrt{6}$.

Along $C$ we have $x=1+t$, $y=1+2t$, $z=t$, hence
$$
\int_{C} x\,y\,z^{2}\, ds
=\int_{0}^{1} (1+t)(1+2t)t^{2}\,\|\mathbf r'(t)\|\,dt
=\sqrt{6}\int_{0}^{1}\bigl(1+3t+2t^{2}\bigr)t^{2}\,dt.
$$
Therefore
$$
\sqrt{6}\left[\frac{t^{3}}{3}+\frac{3t^{4}}{4}+\frac{2t^{5}}{5}\right]_{0}^{1}
=\sqrt{6}\left(\frac{1}{3}+\frac{3}{4}+\frac{2}{5}\right)
=\frac{89\sqrt{6}}{60}.
$$

### **(Problem 03)** 

Evaluate the planar work integral
$$
\int_{C} x\,y\,dx+(x+y)\,dy,
$$
where $C=C_{1}\cup C_{2}$ consists of the straight segments $C_{1}:(1,2)\to(3,4)$ and $C_{2}:(3,4)\to(4,0)$.

**Solution.**

Extract the vector: 

$$
\int_C (xy\hat{\textbf{x}}+(x+y)\hat{\textbf{y}}) \cdot d\textbf{r}
$$

For $C_1$, we parameterize the path as $\textbf{r}(t)=\langle 1+2t, 2+2t\rangle$ for $t\in [0,1]$. 

$$
\begin{aligned}
\textbf{r}'(t) = \langle 2, 2 \rangle \\
\textbf{v}(\textbf{r}(t))=\langle 4t^2+6t+2, 3+4t\rangle
\end{aligned}
$$

And so, for $C_1$

$$
\int_{C_1} \textbf{v} \cdot d\textbf{r} =\int_0^1 8t^2+20t+10 \cdot dt = \left[\frac{8}{3} t^3 + 10t^2 + 10\right]_0^1 =\frac{68}{3}
$$

For $C_2$, we parameterize the path as $\textbf{r}(t)=\langle 3+t, 4-4t \rangle$ for $t \in [0,1]$.

$$
\begin{aligned}
\textbf{r}'(t)=\langle1,-4 \rangle \\
\textbf{v}(\textbf{r}(t)) = \langle 12-8t-4t^2, 7-3t \rangle
\end{aligned}
$$

$$
\int_0^1 12-8t-4t^2-28+12t \cdot dt = \int_0^1 -16 + 4t-4t^2 \cdot dt = \left[-16t +2t-\frac{4t^3}{3}\right]_0^1 = -16+2-\frac{4}{3}
$$
$$
=-\frac{46}{3}
$$

Adding the two integrals, we get $\dfrac{68}{3}-\dfrac{48}{3}=\dfrac{22}{3}$. 

### **(Problem 04)** 

Evaluate the line integral
$$
\oint_{C} (y^{2}+\cos x)\,dx+(x-\arctan y)\,dy,
$$
where $C$ is the positively oriented boundary of the region between $y=0$ and $y=4-x^{2}$.

**Solution.**

By Green's theorem,
$$
\oint_{C} P\,dx+Q\,dy=\iint_{D}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\,dA,
\quad
P=y^{2}+\cos x,\quad Q=x-\arctan y.
$$
Then
$$
\frac{\partial Q}{\partial x}=1,\qquad \frac{\partial P}{\partial y}=2y,
$$
so
$$
\oint_{C} (y^{2}+\cos x)\,dx+(x-\arctan y)\,dy
=\iint_{D}(1-2y)\,dA,
$$
where $D=\{(x,y): -2\le x\le 2,\ 0\le y\le 4-x^{2}\}$.

Compute:
$$
\iint_{D}(1-2y)\,dA
=\int_{-2}^{2}\!\!\int_{0}^{\,4-x^{2}} (1-2y)\,dy\,dx
=\int_{-2}^{2}\Big[(y-y^{2})\Big]_{0}^{\,4-x^{2}}dx
=\int_{-2}^{2}\big[(4-x^{2})-(4-x^{2})^{2}\big]\,dx.
$$
Simplify the integrand:
$$
(4-x^{2})-(4-x^{2})^{2}=-12+7x^{2}-x^{4},
$$
hence
$$
\int_{-2}^{2}(-12+7x^{2}-x^{4})\,dx
=2\int_{0}^{2}(-12+7x^{2}-x^{4})\,dx
=2\left[-12x+\frac{7x^{3}}{3}-\frac{x^{5}}{5}\right]_{0}^{2}$$
$$
=2\left(-24+\frac{56}{3}-\frac{32}{5}\right)
=-\frac{352}{15}.
$$

### **(Problem 05)** 

Compute the line integral of: 

$$
\textbf{v} = (r\cos^2{\theta})\hat{\textbf{r}} - (r\cos{\theta}\sin{\theta})\hat{\boldsymbol{\theta}} + 3r\hat{\boldsymbol{\phi}}
$$

around the path shown below (the points are labeled by their Cartesian coordinates). Use spherical and cylindrical coordinates. 

![[Pasted image 20251023124518.png]]

**Solution:**

I'll only be using spherical coordinates for this, though you can do it more easily in cylindrical coordinates. 

The differential line element for spherical coordinates is: (as stated [here](<Curvilinear Coordinates>))
$$
d\boldsymbol{\ell}=dr\,\hat{\mathbf{r}}+r\,d\theta\,\hat{\boldsymbol{\theta}}+r\sin\theta\,d\phi\,\hat{\boldsymbol{\phi}},
$$
And so, 

$$
\textbf{v} \cdot d\boldsymbol{\ell} = r\cos^2\theta \cdot dr -(r^2\cos{\theta}\sin{\theta})\cdot d\theta+3r^2\sin{\theta} \cdot d\phi
$$

We will divide the overall path into the following segments: 

$$
\begin{aligned} 
C_1: (0,0,0) \to (1,0,0) \\ 
C_2: (1,0,0) \to (0,1,0) \\ 
C_3: (0,1,0) \to (0,1,2) \\ 
C_4: (0,1,2) \to (0,0,0)
\end{aligned}
$$

For $C_1$, we parameterize the path as: $r=t$ (and $dr=dt$), $\theta=\dfrac{\pi}{2}$ and $\phi=0$ (and $d\phi=0$) for $t \in [0,1]$, and so:

$$
\int_{C_1} \left\langle 0, 0, 3r^2 \right\rangle \cdot \langle dr, d\theta, d\phi \rangle = \int_{C_1} \left\langle 0, 0, 3r^2 \right\rangle \cdot \langle dr, d\theta, 0 \rangle = 0
$$

For $C_2$, we parameterize the path as: $r=1$ ($dr=0$), $\theta=\dfrac{\pi}{2}$ ($d\theta=0$) and $\phi=t$ ($d\phi=dt$) for $t\in[0,\frac{\pi}{2}]$, which gives us:

$$
\int_{C_2} \langle 0,0,3\rangle \cdot \langle 0, 0,d\phi\rangle = \int_0^{\frac{\pi}{2}} 3 \cdot d\phi = \frac{3\pi}{2}
$$

For $C_3$,  we parameterize the path as: $r=t$, $\theta=\arcsin{1/t}$ and $\phi=\dfrac{\pi}{2}$ for $t \in [1,\sqrt{5}]$. We have: 

$$
d\theta=\frac{-dt}{t^2\sqrt{1-\dfrac{1}{t^2}}} = \frac{-dt}{t\sqrt{t^2-1}}
$$

$$
\int_{t=1}^{t=\sqrt{5}} \langle r(1-\sin^2{\theta}), -r^2\sqrt{1-\sin^2{\theta}}\sin\theta, 3r^2 \sin{\theta} \rangle \cdot \left\langle dt, \frac{-dt}{t \sqrt{t^2-1}},0 \right\rangle 
$$

Note down a few handy identities:
$$
\begin{aligned}
\sin^{2}(\theta)=\sin\theta \cdot \sin\theta = \frac{1}{t^2} \\
1-\sin^{2}\theta = 1-\frac{1}{t^2} = \frac{t^2-1}{t^2}
\end{aligned}
$$
Then proceed to solve:
$$
\int_1^\sqrt{5}\left \langle t-\frac{1}{t}, -\sqrt{t^2-1} \right \rangle  \left\langle dt, \frac{-dt}{t \sqrt{t^2-1}} \right\rangle 
$$
(We omit the $\phi$ component entirely as its corresponding differential is $0$: 
$$
\int_1^\sqrt{5} t-\frac{1}{t} + \frac{1}{t} \cdot dt = \frac{5}{2}-\frac{1}{2}=2 
$$

For $C_4$, we parameterize the path as: $r=t$, $\theta=\arcsin{\frac{1}{\sqrt{5}}}$, and $\phi=\dfrac{\pi}{2}$ going from $t=\sqrt{5}$ to $t=0$, 

$$
\int_\sqrt{5}^0 t \left(1-\frac{1}{5}\right)\cdot dt = \frac{4}{5} \int_\sqrt{5}^0 t \cdot dt = -2
$$

So, the total line integral is $\dfrac{3\pi}{2}+2-2+0$ which is $\dfrac{3\pi}{2}$. 

We can derive an equivalent result using Stokes' Theorem. We have two surfaces in this case (one directed along the unit normal $\hat{\textbf{z}}$ and $\hat{\textbf{x}}$). Stokes' theorem: (retrieved from [here](<Surface Integrals>)) 

$$
\oint_{C} \mathbf{v}\cdot d\mathbf{r}
=\iint_{S} (\nabla\times \mathbf{v})\cdot \mathbf{n}\,dS.
$$


Before anything, we start with the curl of $\textbf{v}$ in spherical coordinates: (curl formula retrieved from [here](<Curvilinear Coordinates>))
$$
(\nabla \times \textbf{v})_r = \frac{1}{r\sin\theta}\!\left(\frac{\partial}{\partial \theta}(\sin\theta\,v_\phi)-\frac{\partial v_\theta}{\partial \phi}\right)=\frac{1}{r\sin{\theta}}\left(\frac{d}{d\theta} (3r\sin{\theta})-\frac{d}{d\phi}\left(\frac{r}{2}\sin{2\theta}\right)\right)=3\cot{\theta}
$$

$$
(\nabla \times \textbf{v})_\theta = \frac{1}{r}\left(\frac{1}{\sin \theta} \frac{\partial (r\cos^2{\theta})}{\partial \phi}-\frac{\partial(r \cdot 3r)}{\partial r}\right)=-6
$$

$$
(\nabla \times \textbf{v})_\phi = \frac{1}{r}\left( \frac{\partial}{\partial r}(rv_\theta) - \frac{\partial v_r}{\partial \theta} \right)=0
$$

Starting with $S_1$ (the circular arc in the $xy$-plane), we have $\theta=\dfrac{\pi}{2}$ as a constant so that $dS=r\sin\theta\,dr\,d\phi$. 

We know that $z=\cos{\theta}\hat{\textbf{r}}-\sin\theta \hat{\boldsymbol{\theta}}$ (from [here](<Curvilinear Coordinates>)) 
$$
\iint_{S_1} \langle 3\cot{\theta}, -6, 0 \rangle \cdot \langle \cos{\theta}, -\sin{\theta}, 0 \rangle \cdot dS = \iint_{S_1} 6 \cdot dS
$$
We have: $r\in [0,1]$ and $\phi \in [0, \frac{\pi}{2}]$, 

$$
\int_{0}^1 \int_{0}^{\frac{\pi}{2}} 6r \cdot d\theta \cdot dr = \int_0^1 3\pi r \cdot dr= \frac{3\pi}{2}
$$

Moving to $S_2$ (the triangle on the $yz$ plane), we have $\phi=\dfrac{\pi}{2}$ as a constant so that $dS=r\cdot dr\cdot d\theta$. The normal vector is the $x$-axis, so $\hat{\textbf{n}}=\sin\theta\cos\phi\,\hat{\mathbf r}+\cos\theta\cos\phi\,\hat{\boldsymbol \theta}-\sin\phi\,\hat{\boldsymbol \phi}$,

$$
\iint_{S_2} \langle 3\cot{\theta},-6,0 \rangle \cdot \left \langle \sin\theta\cos\frac{\pi}{2}\,,\cos\theta\cos\frac{\pi}{2}\,,-\sin\frac{\pi}{2}\,\hat{\boldsymbol \phi} \right \rangle \cdot dS = 0
$$

Which, as expected, stays the same. 