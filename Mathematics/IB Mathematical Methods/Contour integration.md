- Heavily relies on results in [[Elementary Analysis#Analytic functions of a complex variable|complex analysis]]

# Results from analysis
- The _differentiability_ of a _complex function_ $f(z)$ requires:
$$\frac{df}{dz}\equiv f'(z)=\lim_{\delta z\to0}\frac{f(z+dz)-f(z)}{\delta z}$$
- This must be _finite_, and be the same _regardless of the direction of the limit_

- _Separate_ the function into real and imaginary parts:
$$\displaylines{z=x+iy \\f(z)=u(x,y)+iv(x,y)}$$
- For a function to be differentiable, it must obey the _Cauchy-Riemann equations_:
$$\displaylines{\pd{u}{x}=\pd{v}{y} \\ \pd{v}{x}=-\pd{u}{y}}$$
- This also implies $u$ and $v$ are _harmonic_

# Contour integrals

## Definition
- Consider the integral of $f(z)$ along the _contour_ $C$ from $z=\alpha$ to $\beta$
- The result _may depend on the contour_

- The _formal definition_ divides the interval $[\alpha,\beta]$ into $N$ parts:
$$\displaylines{\alpha=z_0<z_1<z_2<\dots<z_N=\beta \\ \delta z_k=z_k-z_{k-1} \\ \Delta=\max_k|\delta z_k|}$$
- The integral is then the limit as $N$ approaches infinity:
$$\int_C f(z)\,dz=\lim_{\Delta\to0}\sum_{k=0}^{N-1}f(z_k)\,\delta z_k$$

## Properties
