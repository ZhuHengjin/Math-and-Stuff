---
tags:
  - Math
dlink: "[[-Applications of Integral]]"
date: 2024-06-09
aliases:
  - 矩，质心与形心
---

## Moment

The $moment$ of an object about an axis or plane is defined to be the product of the mass and the directed distance to the axis or plane.

### In 2 Dimensions

We discuss the $moment$ about $x$-axis, $M_x$, and the $moment$ about $y$-axis, $M_y$.

The direct distance of a point $(x,y)$ to the $x$-axis equals to $y$, approximating $M_x$ with a Riemann sum, where $(x^*_{ij}, y^*_{ij})$ represents the center of mass in the given area $A_{ij}$ and $\delta (x^*_{ij}, y^*_{ij})$ represents the density on the give point

$$
M_x \approx \sum_{i} \sum_{j} \delta (x^*_{ij}, y^*_{ij}) y^*_{ij} \Delta A_{ij}
$$

Taking the limit yields a double integral over the region $D$

$$
M_x = \iint_{D} y \delta (x, y) \, dA
$$

Similarly, formula $M_y$ is given by

$$
M_y = \iint_{D} x \delta (x, y) \, dA
$$

### In 3 Dimensions

We discuss the $moment$ about the $xy$-plane, $M_{xy}$, the $moment$ about the $xz$-plane, $M_{xz}$, and the $moment$ about the $yz$-plane, $M_{yz}$.

The direct distance from a point $(x,y,z)$ to the $xy$-plane is equal to the $z$-value. Similarly, formulas for the 3 moments over the region $E$ are

$$ 
M_{xy} = \iiint_E z \delta (x, y, z) \, dV
$$

$$
M_{xz} = \iiint_E y \delta (x, y, z) \, dV
$$

$$
M_{yz} = \iiint_E x \delta (x, y, z) \, dV
$$

## Center of Mass

The $center \ of \ mass$ is defined as the point about which the total moment is 0.

### In 2 Dimensions

Let $(\bar{x}, \bar{y})$ be the coordinates for the center of mass for a lamina.

Consider the moment about the line $x = \bar{x}$. The directed distance from the point $(x,y)$ to the line is $x - \bar{x}$. Taking the double integral we have

$$
M_{\bar {x}} = \iint_D (x - \bar{x}) \delta (x,y) \ dA
$$

Since the moment about the line $x = \bar{x}$ equals to 0, we can set the equation above to 0 to solve for $\bar{x}$.

$$
0 = \iint_D (x - \bar{x}) \delta (x,y) \ dA
$$

Remembering $\bar{x}$ is a constant

$$
0 = \iint_D x \delta (x,y) \ dA - \iint_D \bar{x} \delta (x,y) \ dA
\quad \Rightarrow \quad
\bar{x} = \frac {\iint_D x \delta (x,y) \ dA} {\iint_D \delta (x,y) \ dA}
= \frac{M_y}{m}
$$

Similarly, the moment about the line $y = \bar{y}$ is

$$
M_{\bar {y}} = \iint_D (y - \bar{y}) \delta (x,y) \ dA
$$

Setting the equation to 0 we have

$$
\bar{y} = \frac {\iint_D y \delta (x,y) \ dA} {\iint_D \delta (x,y) \ dA}
= \frac{M_x}{m}
$$

In conclusion,

$$
\bar{x} = \frac{M_y}{m},
\quad
\bar{y} = \frac{M_x}{m}
$$

### In 3 Dimensions

Let $(\bar{x}, \bar{y}, \bar{z})$ be the center of mass of a solid, through the identical derivation as the 2D case we have

$$
\bar{x} = \frac{M_{yz}}{m},
\quad
\bar{y} = \frac{M_{xz}}{m}
\quad
\bar{z} = \frac{M_{xy}}{m}
$$

## Centroid

The $centroid$ of a lamina or solid region corresponds to the center of mass of a region with constant density. This is often referred to as the **geometric center of mass**.

Thus, we can assume $\delta$ is constant then it cancels out in the computation of $\bar{x}$, $\bar{y}$, and $\bar{z}$. 

- For laminas:

$$
\bar{x} = \frac {\iint_D x \ dA} {\iint_D \ dA},
\quad
\bar{y} = \frac {\iint_D y \ dA} {\iint_D \ dA}
$$

- For solids:

$$
\bar{x} = \frac {\iiint_E x \ dV} {\iiint_E \ dV},
\quad
\bar{y} = \frac {\iiint_E y \ dV} {\iiint_E \ dV},
\quad
\bar{z} = \frac {\iiint_E z \ dV} {\iiint_E \ dV}
$$