The del operator is a vector operator is a vector differential operator acting on scalar or vector functions and is defined as:

$$
\nabla = \hat{\textbf{x}} \frac{\partial}{\partial x}+\hat{\textbf{y}} \frac{\partial}{\partial y} + \hat{\textbf{z}} \frac{\partial}{\partial z}
$$

There are three ways the operator $\nabla$ can act on a function: 
1. On a scalar function $T$: $\nabla T$ (the gradient) 
2. On a vector function $\textbf{v}$, via the dot product, $\nabla \cdot \textbf{v}$ (the divergence)
3. On a vector function $\textbf{v}$, via the cross product, $\nabla \times \textbf{v}$ (the curl) 

The divergence is a measure for how much the vector $\textbf{v}$ spreads out. The curl is a vector to measure how much $\textbf{v}$ curls around a point in question. 

Identities for the del operator for vector functions $\textbf{F}$ and $\textbf{G}$ and scalar functions $f$ and $g$:
$$
\begin{aligned} 
\nabla \cdot (\textbf{F}+\textbf{G}) = \nabla \cdot \textbf{F} + \nabla \cdot \textbf{G} &&
\nabla \times (\textbf{F}+\textbf{G}) = \nabla \times \textbf{F} + \nabla \times \textbf{G} \\ 
\nabla \cdot (f \textbf{G})=f(\nabla \cdot \textbf{G})+\textbf{G}\cdot (\nabla f) && \nabla \times (f \textbf{G})=f(\nabla \times \textbf{G})-\textbf{G}\times (\nabla f) \\ 
\nabla \cdot \left(\frac{\textbf{G}}{g}\right)=\frac{g(\nabla \cdot \textbf{G})-\textbf{G}\cdot(\nabla g)}{g^2} && \nabla \times \left(\frac{\textbf{G}}{g}\right)=\frac{g(\nabla \times \textbf{G})+\textbf{G}\times(\nabla g)}{g^2}
\end{aligned}
$$

The curl of a gradient is always $0$. For a scalar function, $f$, the laplacian is defined as the divergence of $\nabla f$. For the laplacian of a vector function $\textbf{v}$ with components $\langle v_x, v_y, v_z \rangle$, 
$$
\nabla^2 \textbf{v} = (\nabla^2 v_x) \hat{\textbf{x}}+(\nabla^2 v_y) \hat{\textbf{y}}+(\nabla^2 v_z) \hat{\textbf{z}}
$$
