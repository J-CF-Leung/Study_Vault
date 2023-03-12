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
- Aside from the _path_, the contour also includes the _travel direction_
- The result _may depend on the contour_\

- The _formal definition_ divides the interval $[\alpha,\beta]$ into $N$ parts:
$$\displaylines{\alpha=z_0<z_1<z_2<\dots<z_N=\beta \\ \delta z_k=z_k-z_{k-1} \\ \Delta=\max_k|\delta z_k|}$$
- The integral is then the limit as $N$ approaches infinity:
$$\int_C f(z)\,dz=\lim_{\Delta\to0}\sum_{k=0}^{N-1}f(z_k)\,\delta z_k$$

## Properties
- If $C_1$ is a contour from $\alpha$ to $\beta$, and $C_2$ is a contour from $\beta$ to $\gamma$, and $C$ is $C_1$ _followed by_ $C_2$:
$$\int_C f(z)\,dz=\int_{C_1} f(x)\,dz+\int_{C_2}f(z)\,dz$$
- If $C_+$ is a contour from $\alpha$ to $\beta$ and $C_-$ is the contour _in reverse_, then:
$$\int_{C_+}f(z)\,dz=-\int_{C_-}f(z)\,dz$$
- If $C$ is a _closed contour_, then _starting point is irrelevant_, but _direction matters_:
$$\oint_\text{clockwise}f(z)\,dz=-\int_\text{anticlockwise}f(z)\,dz$$
- An integral around a _closed contour_ can also be _split into two parts_

- If a contour has _length_ $L$, then:
$$\left|\int_C f(z)\,dz\right|\leq L\max_C|f(z)|$$
- Integration _by parts_ and by _substitution_ are still usable

# Cauchy's theorem
- A _simply connected domain_ (SCD) is a region $R$ of the complex plane _without any holes_
	- In other words, _any closed curve_ in $R$ encircles points _only in $R$_

- A _simple closed curve_ (SCC) is a _continuous closed curve of finite length_ which _has no self-intersections_
	- It must _divide_ the complex plane into an _interior_ and an _exterior_

- _Cauchy's theorem_ states that if a function $f(z)$ is _analytic_ in an SCD $R$, then for _any simple closed curve_ $C$ in $R$:
$$\oint_C f(z)\,dz=0$$
