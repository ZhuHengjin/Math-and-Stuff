---
tags:
  - Math
dlink: "[[-Integrals]]"
date: 2024-06-09
aliases:
  - 三重积分
---
## Triple Integral over Boxes

## Triple Integral over General Regions

## Change Variables

## Coordinate Transformations

### Cylindrical Coordinates

Let point $P = (x,y,z)$. If $(r,\theta)$ is the set of polar coordinates for $(x,y)$ the $(r, \theta, z)$ is the set of $cylindrical \ Coordinates$ for $P$.

The Cylindrical Coordinate Transformation can be written as

$$
x = r \ cos \theta, \quad
y = r \ sin \theta, \quad
z = z
$$

The **Jacobian determinant** for this transformation is

$$
\begin{align*} 
\frac{\partial(x, y, z)}{\partial(r, \theta, z)} 
&= 
\begin{vmatrix} 
\cos \theta & -r \sin \theta & 0 
\\ \sin \theta & r \cos \theta & 0 
\\ 0 & 0 & 1 
\end{vmatrix} \\ 
&= \cos \theta 
\begin{vmatrix} 
r \cos \theta & 0 \\ 
0 & 1 
\end{vmatrix} 
- (-r \sin \theta) 
\begin{vmatrix} 
\sin \theta & 0 \\ 
0 & 1 
\end{vmatrix} 
+ 0
\begin{vmatrix} 
\sin \theta & r \cos \theta \\ 
0 & 0 
\end{vmatrix} \\ 
&= r \cos^2 \theta + r \sin^2 \theta \\ 
&= r 
\end{align*}
$$

Therefore, working with **non-negative** values of $r$, transforming from region $E$ to region $E^*$, we have

$$
\iiint_{E} f(x, y, z) \, dx \, dy \, dz = 
\iiint_{E^*} f(r \cos \theta, r \sin \theta, z) r \, dz \, dr \, d\theta
$$

### Spherical Coordinates

The $P$ be a point in $\mathbb{R}^{3}$ described in rectangular (Cartesian) coordinates by $(x,y,x)$ and cylindrical coordinates by $(r, \theta, z)$. Let

$$
\rho = \text{Length of } \, OP = \sqrt{x^2 + y^2 + z^2}
$$

And Let

$$
\phi = \text{the angle between $OP$ and the positive $z$-axis}
\, (0 \leq \phi \leq \pi)
$$

The point $Q$ is the projection of the point $P$ on the $xy$-plane. Like with cylindrical coordinates, let

$$
\theta = \text{the angle between $OQ$ and the positive $x$-axis}
\, (0 \leq \theta \leq 2\pi)
$$

```tikz
\usepackage{tikz-3dplot}
\begin{document}
\tdplotsetmaincoords{60}{110}
\begin{tikzpicture}[tdplot_main_coords]

\def\thetavec{45}
  \def\phivec{40}
  \def\rvec{2}
  
  \draw[thick,->] (0,0,0) -- (3,0,0) node[anchor=north east] {$x$};
  \draw[thick,->] (0,0,0) -- (0,3,0) node[anchor=north west] {$y$};
  \draw[thick,->] (0,0,0) -- (0,0,3) node[anchor=south] {$z$}; 
  
  \coordinate (O) at (0,0,0); 
  \coordinate (P) at (1.5,1.5,2.5); 
  \coordinate (Q) at (1.5,1.5,0); 
  
  \draw[dashed, gray] (P) -- (0,0,2.5); 
  \draw[thick, cyan] (Q) -- (O); 
  \draw[thick, blue] (P) -- (Q); 
  \draw[thick, red] (O) -- (P) node[midway, right] {$\rho$}; 
  
  \filldraw[black] (O) circle (1pt) node[anchor=south east] {$O$};
  \filldraw[black] (P) circle (1pt) node[anchor=west] {$P$}; 
  \filldraw[black] (Q) circle (1pt) node[anchor=north west] {$Q$};
  
  \tdplotdrawarc[-]{(O)}{0.4}{0}{\thetavec}
    {anchor=north}{$\theta$}
  \tdplotsetthetaplanecoords{\thetavec}
  \tdplotdrawarc[-,tdplot_rotated_coords]{(0,0,0)}{0.7}{0}{\phivec}
    {anchor=south west}{\hspace{-1mm}$\phi$};
    
\end{tikzpicture}
\end{document}

```

Thus, the spherical coordinates can be written as

$$
\begin{align*}
x &= \rho \sin \phi \cos \theta \\
y &= \rho \sin \phi \sin \theta \\
z &= \rho \cos \phi \\
\end{align*}
$$

$$
\text{With $ 0 \leq \theta \leq 2\pi $ and $0 \leq \phi \leq \pi $ .}
$$

![[Pasted image 20240609212831.png]]
