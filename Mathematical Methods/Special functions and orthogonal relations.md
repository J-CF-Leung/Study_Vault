- Many functions are a _complete set_ as they are an [[Vectors and matrices|orthonormal eigenbasis]]

# Trig functions
- Orthogonality of trig functions with period $\Lagr$:
$$\begin{aligned}\int_0^\Lagr\sin\left(\frac{2n\pi x}{\Lagr}\right)\sin\left(\frac{2m\pi x}{\Lagr}\right)\,dx&=\frac{\Lagr}{2}\delta_{nm} \\ \int_0^\Lagr\cos\left(\frac{2n\pi x}{\Lagr}\right)\cos\left(\frac{2m\pi x}{\Lagr}\right)\,dx&=\frac{\Lagr}{2}\delta_{nm}  \\ \int_0^\Lagr\sin\left(\frac{2n\pi x}{\Lagr}\right)\cos\left(\frac{2m\pi x}{\Lagr}\right)\,dx&=0\end{aligned}$$

- Alternative form: integrating over a half period
$$\begin{aligned}\int_0^L\sin\left(\frac{n\pi x}{L}\right)\sin\left(\frac{m\pi x}{L}\right)\,dx&=\frac{L}{2}\delta_{nm} \\ \int_0^L\cos\left(\frac{n\pi x}{L}\right)\cos\left(\frac{m\pi x}{L}\right)\,dx&=\frac{L}{2}\delta_{nm}  \\ \int_0^L\sin\left(\frac{n\pi x}{L}\right)\cos\left(\frac{m\pi x}{L}\right)\,dx&= \begin{cases} 0 &\text{if } n+m \text{ is even} \\ 2nL/[\pi(n^2-m^2)] &\text{if } n-m \text{ is odd}\end{cases}\end{aligned}$$


# Legendre polynomials


## Associated Legendre functions


# Spherical harmonics

# Bessel functions

# Hermite polynomials
- The _physicist's Hermite polynomials_ satisfy _Hermite's equation_:
$$\frac{d^2H}{dq^2}-2q\frac{dH}{dq}+(\epsilon-1)H(q)=0$$
- They can be given by the _Rodrigues formula_:
$$H_n(x)=(-1)^n\exp\left(x^2\right)\frac{d^n}{dx^n}\exp\left(-x^2\right)$$
- They are _orthogonal_ w.r.t. [[Sturm-Liouville Theory#Weight functions and converting to Sturm-Liouville form|weight function]] $\exp(-x^2)$
$$\int_{-\infty}^\infty H_m(x)H_n(x)\exp(-x^2)\,dx=\sqrt{\pi}2^n(n!)\delta_{nm}$$
- The first few Hermite polynomials are:
$$\displaylines{H_0(x)=1 \\ H_1(x)=2x \\ H_2(x)=4x^2-2 \\ H_3(x)=8x^3-12x}$$
# Laguerre polynomials

## Associated Laguerre polynomials
