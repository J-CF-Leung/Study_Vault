- This is the _application_ of methods from [[Elementary Analysis|Complex Analysis]] and [[Contour integration]] to _Fourier transforms_

## Jordan's Lemma
- Consider the integral:
$$\lim_{R\to\infty} \oint_{C_R}g(z)\exp(i\lambda z)\,dz$$
- Where:
	- $\lambda>0$ is a _constant_
	- $g(z)$ is _analytic_ in the _upper half plane_, $\Im(z)>0$
	- The contour $C_R$ is a _semicircle_ of radius $R$ in the _upper half plane_

- Then, _Jordan's Lemma_ states that if $g(z)\to0$ uniformly on $C_R$ as $R\to\infty$, then:
$$\lim_{R\to\infty} \oint_{C_E}g(z)\exp(i\lambda z)\,dz=0$$
- For _negative_ $\lambda$, then the semicircle must be in the _lower half plane_
- The _condition_ of decreasing $g(z)$ can be expressed as:
$$|g(Re^{i\theta})|<G(R)\hspace{1cm}\text{for }0<\theta<\pi$$
	- where $G(R)$ tends to zero as $R\to\infty$

