Let $f(x,y)$ be a function of two variables. The critical points of this function is given by solving $\nabla F = \mathbf{0}$. 

To determine the nature of the critical points, we construct the so-called Hessian matrix $H_f$:

$$
H_f = \begin{bmatrix}
\dfrac{\partial^2 f}{\partial x^2} & \dfrac{\partial^2 f}{\partial x \partial y} \\ 
\dfrac{\partial^2 f}{\partial x \partial y} & \dfrac{\partial^2 f}{\partial y^2} 
\end{bmatrix}
$$
We determine the eigenvalues of this matrix to interpret as follows:
- Both eigenvalues $>$ 0 $\Rightarrow$ Strict local minimum
- Both eigenvalues $<$ 0 $\Rightarrow$ Strict local maximum 
- Eigenvalues with mixed signs $\Rightarrow$ Saddle point 
- Any zeroes $\Rightarrow$ Inconclusive. 

When optimizing $f(x,y)$ subject to a smooth equality constraint $g(x,y)=c$, introduce the Lagrangian $L(x,y,\lambda)=f(x,y)-\lambda\,(g(x,y)-c)$. A necessary condition for a constrained extremum, under the regularity assumption $\nabla g(x_0,y_0)\neq \mathbf{0}$, is

$$
\nabla f(x_0,y_0)=\lambda\,\nabla g(x_0,y_0)\qquad\text{together with}\qquad g(x_0,y_0)=c.
$$

This condition states that at a constrained extremum the gradient of the objective is parallel to the gradient of the constraint, which captures that the level curve of $f$ is tangent to the constraint set at the solution. With several equality constraints $g_i(x,y)=c_i$, the stationarity condition becomes

$$
\nabla f(x_0,y_0)=\sum_i \lambda_i\,\nabla g_i(x_0,y_0)\qquad\text{and}\qquad g_i(x_0,y_0)=c_i\ \text{for all }i.
$$

To determine the nature of a constrained critical point, look at second-order changes along directions that keep the constraint fixed to first order. Take any nonzero vector $v\in\mathbb{R}^2$ satisfying $\nabla g(x_0,y_0)\cdot v=0$. Define
$$
Q(v)=v^{\top}\Big(\nabla^2 f(x_0,y_0)-\lambda\,\nabla^2 g(x_0,y_0)\Big)v.
$$
If $Q(v)>0$ for every such $v$, the point is a strict constrained local minimum. If $Q(v)<0$ for every such $v$, the point is a strict constrained local maximum. If $Q$ takes both signs or is zero for some nonzero $v$ with $\nabla g(x_0,y_0)\cdot v=0$, the second-order test is inconclusive. 

---

## Problems

**(Problem 01)** Maximize and minimize
$$
f(x,y,z)=x+2y-2z\quad\text{subject to}\quad g(x,y,z)=x^2+2y^2+4z^2=1.
$$
**Solution:**

Set $\nabla f=\lambda \nabla g$:
$$
(1,2,-2)=\lambda(2x,4y,8z)\quad\Rightarrow\quad x=\frac{1}{2\lambda},\ y=\frac{1}{2\lambda},\ z=-\frac{1}{4\lambda}.
$$
Impose the constraint:
$$
\left(\frac{1}{2\lambda}\right)^2+2\left(\frac{1}{2\lambda}\right)^2+4\left(-\frac{1}{4\lambda}\right)^2
=\frac{1}{4\lambda^2}+\frac{2}{4\lambda^2}+\frac{1}{4\lambda^2}
=\frac{1}{\lambda^2}=1,
$$
so $\lambda=\pm 1$. The candidates are
$$
\lambda=1:\ \left(\frac{1}{2},\frac{1}{2},-\frac{1}{4}\right),\qquad
\lambda=-1:\ \left(-\frac{1}{2},-\frac{1}{2},\frac{1}{4}\right).
$$
Evaluate $f$:
$$
f\!\left(\frac{1}{2},\frac{1}{2},-\frac{1}{4}\right)=2,\qquad
f\!\left(-\frac{1}{2},-\frac{1}{2},\frac{1}{4}\right)=-2.
$$


**(Problem 02)** Optimize $f(x,y)=xy$ subject to the smooth equality constraint
$$
g(x,y)=x^2+y^2=1.
$$

**Solution:**

$$
\nabla f(x,y)=(y,x).
$$
Setting $\nabla f=\mathbf 0$ gives the only critical point $(0,0)$.  

The Hessian of $f$ is constant:
$$
H_f=\begin{bmatrix}0&1\\ 1&0\end{bmatrix}.
$$
Its eigenvalues are $+1$ and $-1$, so $(0,0)$ is a **saddle**.

Constrained critical points via Lagrange multipliers:  

$$
L(x,y,\lambda)=xy-\lambda\,(x^2+y^2-1).
$$
First-order conditions:
$$
\begin{cases}
\partial_x L:\; y-2\lambda x=0,\\
\partial_y L:\; x-2\lambda y=0,\\
x^2+y^2=1.
\end{cases}
$$
From the first two equations: $y=2\lambda x$ and $x=2\lambda y$. If $x=0$ then $y=0$, impossible on the unit circle, so $x\neq 0$. Hence $x=4\lambda^2x\Rightarrow 4\lambda^2=1\Rightarrow \lambda=\pm \dfrac12$.

- If $\lambda=\dfrac12$, then $y=x$ and $x^2+y^2=1$ gives
  $$
  (x,y)=\left(\dfrac1{\sqrt2},\dfrac1{\sqrt2}\right),\ \left(-\dfrac1{\sqrt2},-\dfrac1{\sqrt2}\right),\quad f=\dfrac12.
  $$
- If $\lambda=-\dfrac12$, then $y=-x$ and $x^2+y^2=1$ gives
  $$
  (x,y)=\left(\dfrac1{\sqrt2},-\dfrac1{\sqrt2}\right),\ \left(-\dfrac1{\sqrt2},\dfrac1{\sqrt2}\right),\quad f=-\dfrac12.
  $$

Classify constrained critical points with the second-order test:  

With $\nabla^2 f=\begin{bmatrix}0&1\\1&0\end{bmatrix}$ and $\nabla^2 g=\begin{bmatrix}2&0\\0&2\end{bmatrix}=2I$, take any tangent direction at $(x_0,y_0)$ as
$$
v=(-y_0,\,x_0)\quad\text{so}\quad \nabla g(x_0,y_0)\cdot v=2(x_0,y_0)\cdot(-y_0,x_0)=0,\ \ \|v\|^2=1.
$$
Then
$$
Q(v)=v^\top\big(\nabla^2 f-\lambda\,\nabla^2 g\big)v
=2v_xv_y-2\lambda\|v\|^2=-2x_0y_0-2\lambda.
$$
Evaluate at the candidates:
- $\left(\dfrac1{\sqrt2},\dfrac1{\sqrt2}\right)$ with $\lambda=\dfrac12$: $x_0y_0=\dfrac12\Rightarrow Q=-2<0$ $\Rightarrow$ **strict constrained local maximum**.
- $\left(-\dfrac1{\sqrt2},-\dfrac1{\sqrt2}\right)$ with $\lambda=\dfrac12$: $Q=-2<0$ $\Rightarrow$ **strict constrained local maximum**.
- $\left(\dfrac1{\sqrt2},-\dfrac1{\sqrt2}\right)$ with $\lambda=-\dfrac12$: $x_0y_0=-\dfrac12\Rightarrow Q=+2>0$ $\Rightarrow$ **strict constrained local minimum**.
- $\left(-\dfrac1{\sqrt2},\dfrac1{\sqrt2}\right)$ with $\lambda=-\dfrac12$: $Q=+2>0$ $\Rightarrow$ **strict constrained local minimum**.

So, unconstrained, $f$ has a saddle at $(0,0)$. Constrained to $x^2+y^2=1$, the maxima $f=\dfrac12$ occur at $\big(\pm\dfrac1{\sqrt2},\pm\dfrac1{\sqrt2}\big)$, and the minima $f=-\dfrac12$ occur at $\big(\pm\dfrac1{\sqrt2},\mp\dfrac1{\sqrt2}\big)$. The second-order constrained test matches these classifications.

