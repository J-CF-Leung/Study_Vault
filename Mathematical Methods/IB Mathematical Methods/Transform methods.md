- This is the _application_ of methods from [[Elementary Analysis|Complex Analysis]] and [[Contour integration]] to [[Fourier series and transforms|Fourier transforms]]
- _Define_ the Fourier transform as:
$$\tilde{f}(k)\equiv\mathcal{F}[f(x)]=\int_{-\infty}^\infty f(x)\exp(-ikx)\,dx$$
- Then define the _inverse Fourier transform_:
$$f(x)\equiv\mathcal{F}^{-1}[\tilde{f}(k)]=\frac{1}{2\pi}\int_{-\infty}^\infty \tilde{f}(k)\exp(ikx)\,dk$$
- These can be interpreted as _contour integrals along the real axis_ in the complex $x-$ and $k-$planes

- Useful properties:
$$\mathcal{F}\left[\frac{d^nf}{dx^n}\right]=(ik)^n\mathcal{F}[f]$$
- The [[Fourier series and transforms#The convolution theorem|convolution theorem]]:
$$h(x)=(f*g)(x)=\int_{-\infty}^\infty f(y)g(x-y)\,dy \Longleftrightarrow \tilde{h}(k)=\tilde{f}(k)\tilde{g}(k)$$
## The damped forced harmonic oscillator
- Consider the 2nd-order linear ODE:
$$\ddot{x}(t)+2\gamma\dot{x}(t)+\omega_0^2x(t)=f(t)$$
- Using the property of _Fourier transforming a derivative_:
$$\displaylines{\tilde{x}(\omega)=\frac{\tilde{f}(\omega)}{(\omega_0^2-\omega^2)+2i\gamma\omega}=\tilde{g}(\omega)\tilde{f}(\omega) \\ \tilde{g}(\omega)=\frac{1}{(\omega-\omega_+)(\omega-\omega_-)}\hspace{1.5cm} \omega_\pm=i\gamma\pm\sqrt{\omega_0^2-\gamma^2}}$$
- _As long as_ $\omega_0^2>0$ (real natural frequency), the poles are in the _upper-half plane_

- Then using the _convolution theorem_:
$$x(t)=\int_{-\infty}^\infty f(s)g(t-s)\,ds$$
- This is equivalent to solving a [[Green's Functions for ODEs|Green's Function problem]] for a 2nd order linear operator

- To find the _inverse Fourier transform_ of $\tilde{g}(\omega)$:
$$g(\tau)=\frac{1}{2\pi}\int_{-\infty}^{\infty}\frac{\exp(i\omega \tau)}{(\omega-\omega_+)(\omega-\omega_-)}\,d\omega$$
- This can be treated as a _contour integral_
	- If $t<0$, use a contour in the _lower-half plane_, which encircles _no poles_
	- If $t>0$, use a contour in the _upper-half plane_, encircling the _poles_ at $\omega_\pm\in\mathbb{C}$
- From [[Contour integration#Jordan's Lemma|Jordan's Lemma]], the contribution from semi-circular arcs _vanishes_

- Hence, $g(t-s)=0$ if $s>t$, therefore if $f(t<0)=0$
$$x(t<0)=\int_{-\infty}^t f(s)g(t-s)\,ds=0$$
- In other words, the object _does not oscillate until the forcing is switched on_
- $g(t-s)$ is then known as a _causal Green's function_

### The solutions
- For the _underdamped_ case, where $\omega_0>\gamma$, from the Residue theorem:
$$g(\tau)=\frac{\exp(-\gamma\tau)}{\sqrt{\omega_0^2-\gamma^2}}\sin\left(T\sqrt{\omega_0^2-\gamma^2}\right)$$
- There is a _decaying oscillatory response_, with a timescale of $1/\gamma$

- For the _overdamped_ case, where $\omega_0<\gamma$, the object _does not oscillate at all_

- For the _critically damped_ case where $\omega_0=\gamma$, there is a _double pole_ at $\omega_\pm=-\gamma$:
$$g(\tau)=\tau\exp(-\gamma\tau)$$

## The diffusion equation
- The _temperature_ $T(x,t)$ of a uniform bar obeys the equation:
$$\pd{T}{t}=\lambda T''$$
- _Initially_, there is some temperature profile $T_0(x)$

- Fourier transforming both sides _with respect to_ $x$:
$$\pd{}{t}\tilde{T}(k,t)=-\lambda k^2\tilde{T}(k,t)$$
- From this, one gets:
$$\tilde{T}(k,t)=\tilde{T_0}(k)\exp(-\lambda k^2t) \hspace{1.5cm} \tilde{T}_0(k)=\mathcal{F}[T_0(x)]$$
- From the _convolution theorem_, letting $\exp(-\lambda k^2t)=\tilde{g}(k,t)$:
$$T(x,t)=\int_{-\infty}^\infty T_0(y)\,g(x-y,t)\,dy$$
- The inverse transform of $\tilde{g}$, using a _new integration variable_ $u=\sqrt{\lambda t}k$ then _completing the square_ and using the [[Contour integration#Gaussian integration lemma|Gaussian integration lemma]]:
$$g(x,t)=\frac{1}{2\pi}\int_{-\infty}^\infty\exp(ikx-\lambda k^2t)\,dk=\frac{\exp(-x^2/4\lambda t)}{\sqrt{4\pi\lambda t}}$$
- The _final solution_ is then:
$$T(x,t)=\int_{-\infty}^\infty T_0(y)\frac{\exp\left[-(x-y)^2/4\lambda t\right]}{\sqrt{4\pi\lambda t}}\,dy$$
