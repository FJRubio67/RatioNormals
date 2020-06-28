# Ratio of two normals and a normal approximation


## The distribution of the ratio of two independent normals and a normal approximation

Let $X\sim N(\mu_x,\sigma_x^2)$ and $Y\sim N(\mu_y,\sigma_y^2)$ be two independent random variables, and $Z=X/Y$. Define $\beta = \mu_x/\mu_y$, $\rho=\sigma_y/\sigma_x$, and $\delta = \sigma_y/\mu_y$. Then, the probability density function of the ratio $Z$ is given by:
$$f_Z(z;\beta,\rho,\delta_y) = \frac{\rho}{\pi(1+\rho^2 z^2)}\left\{\exp\left[-\frac{\rho^2\beta^2+1}{2\delta_y^2}\right] + \sqrt{\frac{\pi}{2}} q \text{erf}\left(\frac{q}{\sqrt{2}}\right)\exp\left[-\frac{\rho^2(z-\beta)^2}{2\delta_y^2(1+\rho^2 z^2)}\right] \right\},$$
where
$$q=\frac{1+\beta\rho^2 z}{\delta_y\sqrt{1+\rho^2z^2}}.$$
This density is heavy tailed and has no moments. The shape of this density can be unimodal, bimodal, symmetric, asymmetric, and/or even similar to a normal distribution close to its mode. [1] found that the density $f_Z$ can be approximated with a normal distribution on an interval of a certain probability, provided that the coefficient of variation of $Y$, $\delta_y$, is smaller than $0.1$ (See Theorem 1 of [1] for more precise conditions). [1] proposed a normal approximation to the distribution of the ratio of two independent normals as $Z\stackrel{\cdot}{\sim}N(\mu_z,\sigma_z^2)$, where $\mu_z=\beta = \mu_x/\mu_y$ and $\sigma_z^2 = \delta_y^2 (\rho^{-2}+\beta^2)$. The following R code shows the shapes of the distribution of $Z$ as well as the accuracy of the normal approximation proposed by [1]. Note that only the first three examples fall into the range $\delta_y\leq 0.1$.



**References.**

1. [On the existence of a normal approximation to the distribution of the ratio of two independent normal random variables](http://link.springer.com/article/10.1007/s00362-012-0429-2)

## R code (R Markdown)

1. [Ratio of two normals and a normal approximation](https://rpubs.com/FJRubio/RatioNormals)
