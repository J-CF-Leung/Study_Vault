#IB_Natsci 
# Fourier series
- Let $f(x)$ be a function with period $\Lagr$ 
- Fourier's theorem states that it can be expressed as:
$$f(x)=\frac{a_0}{2}+\sum_{n=1}a_n\cos\left(\frac{2n\pi x}{\Lagr}\right)+\sum_{n=1}b_n\sin\left(\frac{2n\pi x}{\Lagr}\right)$$
- Using the [[Special functions and orthogonal relations#Trig functions|trig function orthogonality relations]]:
$$a_0=\frac{2}{\Lagr}\int_{x_0}^{x_0+\Lagr}f(x)\,dx$$
$$a_n=\frac{2}{\Lagr}\int_{x_0}^{x_0+\Lagr} f(x)\cos\left(\frac{2\pi nx}{\Lagr}\right)\,dx$$
$$b_n=\frac{2}{\Lagr}\int_{x_0}^{x_0+\Lagr} f(x)\sin\left(\frac{2\pi nx}{\Lagr}\right)\,dx$$
- If $f$ is an even function, $b_n=0$
- If $f$ is an odd function, $a_n=0$

## Fourier exponential series
- $f(x)$ can also be written as:
$$f(x)=\sum_{n=-\infty}^\infty C_n\exp(2i\pi nx/\Lagr)$$
- Where the coefficients are:
$$C_n=\frac{1}{\Lagr}\int_{x_0}^{x_0+\Lagr} f(x) \exp(-2i\pi nx/\Lagr)\, dx$$

- The coefficients in the two representations are related by:
$$\displaylines{C_n=\frac{a_n-ib_n}{2}\hspace{1cm} C_{-n}=\frac{a_n+ib_n}{2} \\ a_n=C_n+C_{-n} \hspace{1cm} b_n=i(C_n-C_{-n}) \\ C_0=a_0}$$

- If $f(x)$ is real, $C_{-n}=C_n^*$
- If $f(x)$ is even, $C_n=C_{-n}$
- If $f(x)$ is odd, $C_n=C_{-n}$

# Fourier transforms
>[!quote]
>"We add things that wiggle up and down to make things that don't wiggle up and down"
>
>-Dr. S. J. Cowley, 2022

- Given a function $f(x)$ where:
$$\int_{-\infty}^{\infty} |f(x)|\,dx<\infty$$

- Its _Fourier transform_ $\tilde{f}(k)$ is:
$$\tilde{f}(k)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty e^{-ikx}f(x)\,dx$$

- The transform is a kind of "weighing function" for the superposition of waves

- Conventions differ on the position of the $2\pi$, and sign of the exponent
>[!quote]
>"You can normalise $\epsilon_0$ to be 1, you can normalise $\mu_0$ to be 1, you can normalise $c$ to be 1, the shame is that you can't normalise $2\pi$ to be 1"
>
>-Dr. S. J. Cowley, 2022

## Properties of Fourier transforms
- Unlike the series, if $f$ is real, the Fourier transform is not necessarily real

- If $f$ is real and even, the Fourier transform is real
- If $f$ is real and odd, the Fourier transform is purely imaginary

- The converses of these statements are true

## Examples of Fourier transforms
- Any _pure cosine_:
$$\mathcal{F}[A\cos(\omega_0t)]=\frac{1}{\sqrt{2\pi}}\frac{A}{2}[\delta(\omega+\omega_0)+\delta(\omega-\omega_0)]$$

- A _decaying exponential_ $f(x)=\exp(-b|x|)$ for $b>0$
$$\mathcal{F}[e^{-b|x|}]=\tilde{f}(k)=\frac{1}{\sqrt{2\pi}}\frac{2b}{k^2+b^2}$$
	- One sided decaying exponential: complex Fourier transform

- A _Gaussian_
$$\mathcal{F}\left[\frac{1}{\sqrt{2\pi\epsilon^2}}\exp\left(-\frac{x^2}{2\epsilon^2}\right)\right]=\frac{1}{\sqrt{2\pi}}\exp\left(-\frac{1}{2}\epsilon^2k^2\right)$$
	- The Fourier transform of a Gaussian is a Gaussian
	- For a narrow Gaussian, the Fourier transform will be wide, and vice versa

- The [[Second order linear ODEs and Green's Functions#The Dirac Delta function ❤|Dirac Delta function]]
$$\mathcal{F}[\delta(x-a)]=\frac{1}{\sqrt{2\pi}}e^{ika}$$
	- The Fourier transform of $\delta(x)$ is $1/\sqrt{2\pi}$, _consistent with the limit_ of the narrow Gaussian

- The Heaviside step function
$$\mathcal{F}[H(x-a)]=\frac{1}{\sqrt{2\pi}}\left[\frac{e^{-ikx}}{ik}\right]_a^{\infty}$$
	- The trick:
$$\mathcal{F}[H(x-a)\exp[\epsilon(x-a)]]=\frac{1}{\sqrt{2\pi}}\frac{e^{-ika}}{\epsilon+ik}$$
	- Taking the limit $\epsilon\to 0$:
$$\mathcal{F}[H(x-a)]=\frac{1}{\sqrt{2\pi}}\frac{e^{-ika}}{ik}=\frac{\mathcal{F}[\delta(x-a)]}{ik}$$


- The _top hat function_ 
$$g(x)=\begin{cases}c &a<x<b \\ 0 &\text{otherwise}\end{cases}$$
$$\sqrt{2\pi}\,\tilde{g}(k)=\frac{ic}{k}(e^{-ikb}-e^{-ika})$$
	- For $a=-1$, $b=1$, $c=1$:
$$\sqrt{2\pi}\,\tilde{g}(k)=\frac{2\sin k}{k}$$
- The _comb function_
$$\displaylines{f(x)=\sum_{n=-\infty}^\infty \delta(x-nx_0) \\ \tilde{f}(k)=\frac{k_0}{\sqrt{2\pi}}\sum_{n=-\infty}^\infty\delta(k-nk_0)=\frac{\sqrt{2\pi}}{x_0}\sum_{n=-\infty}^\infty\delta(k-n\frac{2\pi}{x_0})}$$


## The Fourier inversion theorem
- The inverse transform: from the Fourier transform to the function
$$\displaylines{\mathcal{F}(f)\equiv\tilde{f}(k)=\frac{1}{\sqrt{2\pi}} \int_{-\infty}^\infty f(x)e^{-ikx}\,dx}$$
$$\mathcal{I}(\tilde{f})\equiv f(x)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty \tilde{f}(k)\,e^{ikx}\,dk$$
- Derivation: substitute definition of $\tilde{f}$ into the integral, use definition of Delta function
- Interpretation: adding up waves with the Fourier tansform as the "weighing function"

## Properties of Fourier transforms
- Linearity:
$$\mathcal{F}[\alpha f(x)+\beta g(x)]=\alpha\mathcal{F}[f(x)]+\beta\mathcal{F}[g(x)]$$
- Rescaling: let $g(x)=f(\alpha x)$
$$\tilde{g}(k)=\frac{1}{|\alpha|}\tilde{f}\left(\frac{k}{\alpha}\right)$$



- Translation:
$$\mathcal{F}[f(x-\alpha)]=e^{ik\alpha}\mathcal{F}[f(x)]$$
- Exponential:
$$\mathcal{F}[e^{ik\alpha}f(x)](k)=\mathcal{F}[f(x)](k-a)$$

- A translation in $k$ is _equivalent_ to multiplying $f(x)$ by an exponential in $k$

- Duality: if $g(x)=\tilde{f}(x)$
$$\tilde{g}(k)=f(-k)$$
	- Transforming twice gives the reflected function

- Complex conjugation and parity inversion
$$\mathcal{F}[f^*](k)=\mathcal{F}[f](-k)$$

- Symmetry: if $f(x)$ is even or odd
$$\tilde{f}(-k)=\pm \tilde{f}(k)$$

>[!quote]
"Now we move on to the two that I think are magic"
>-Dr. S. J. Cowley, 2022

- Differentiation by $x$: Use the Leibniz rule and the definition of the inverse transform
$$\mathcal{F}\left[\frac{d^nf}{dx^n}\right]=(ik)^n\mathcal{F}[f]$$
- Multiplication by $x$: differentiate the Fourier transform by $k$
$$i\frac{d\tilde{f}}{dk}=\mathcal{F}[xf(x)]$$


- Multiplication in $x(\text{or }k)\leftrightarrow$ differentiation in $k(\text{or }x)$   

## Relation to Fourier series
- Consider the [[#Fourier exponential series]]:
$$f(x)=\sum_{n=-\infty}^\infty C_n\exp(2i\pi nx/\Lagr)$$
- Where the coefficients are:
$$C_n=\frac{1}{\Lagr}\int_{x_0}^{x_0+\Lagr} f(x) \exp(-2i\pi nx/\Lagr)\, dx$$
- Define the _wavenumber_ $k_n$:
$$k_n\equiv\frac{2\pi n}{\Lagr}$$
- The differences in each wavenumber are $\Delta k=2\pi/\Lagr$
- As $\Lagr\to\infty$, $\Delta k$ becomes the infinitesimal $dk$

- Rewrite $f(x)$ as:
$$f(x)=\frac{1}{\sqrt{2\pi}}\sum_{n=-\infty}^\infty \tilde{f}(k_n) \exp(ixk_n) \Delta k$$
- Where:
$$\tilde{f}(k_n)=\frac{\Lagr C_n}{\sqrt{2\pi}}$$
- As $\Delta k$ becomes infinitesimal:
$$\tilde{f}(k)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty f(x)\exp(-ixk)\,dx$$
$$f(x)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty \tilde{f}(k)\exp(ikx)\,dk$$
# The convolution theorem

## Convolutions
- The _convolution_ $f*g$ of $f(x)$ and $g(x)$ is defined as:
$$(f*g)(x)=\int_{-\infty}^\infty f(y)\,g(x-y)\,dy$$
- Expresses the _overlap_ of $f$ and $g$ as the _latter is shifted_ over the former by some amount $x$

- Symmetry: $f*g=g*f$

### In statistics
- Consider a random variable $x$, with a _probability distribution_ $f(x)$
	- In the limit of small $\delta x$, probability of $x$ lying in $x_0<x<x_0+\delta x$ is $f(x_0)\delta x$
- Let there be an _independent_ random variable $y$ with distribution $g(y)$

- Let the sum $x+y=z$, with distribution $h(z)$
- For any given value of $x$, the probability of $z_0<z<z_0+\delta z$ is the probability of:
$$z_0-x<y<z_0-x+\delta z$$
- That probability is $g(z_0-x)\delta z$
- The probability that $z$ lies in that range for _all values of x_ is:
$$h(z_0)\delta z=\int_{-\infty}^\infty f(x)g(z_0-x)\,\delta z\,dx$$
- Therefore:
$$h=f*g$$

- Other applications:
	- Convolution of a _point spread function_ of a telescope with an extended light source
		- Convolving individual responses with the point spread
	- The [[Electromagnetism#The electrostatic potential|electrostatic potential]] of a charge distribution convolves $\rho(r')$ with $1/|r-r'|$

## The convolution theorem
- The Fourier transform of $f*g$ is given by:
$$\mathcal{F}[f*g]=\sqrt{2\pi}\mathcal{F}[f]\mathcal{F}[g]$$

- Proof: write down Fourier transform, change integration order, change variables

- Conversely, the Fourier transform of a product is:
$$\mathcal{F}[fg]=\frac{1}{\sqrt{2\pi}}\mathcal{F}[f]*\mathcal{F}[g]$$
- Proof: write down the transform, express $f$ and $g$ in terms of $\tilde{f}$ and $\tilde{g}$

- Convolution is an operation _best carried out in the Fourier domain_
- Multiplication in Fourier space $\leftrightarrow$ Convolution in normal space

- Deconvolution in normal space: division in Fourier space

# Correlations
- The _correlation_ $f\otimes g$ of $f(x)$ and $g(x)$ is:
$$h(x)=f\otimes g=\int_{-\infty}^\infty [f(y)]^*g(x+y)\,dy$$
- Correlation quantifies the relationship between two oscillatory functions

- Out of phase: negative
- In phase: positive
- Uncorrelated: zero

- The Fourier transform of a correlation:
$$\tilde{h}(k)=\sqrt{2\pi}[\tilde{f}(k)]^*\tilde{g}(k)$$
- Result: the Wiener-Kinchin theorem

- Autoconvolution: $f*f=\sqrt{2\pi}\tilde{f}^2$
- Autocorrelation: $f\otimes f=\sqrt{2\pi}|\tilde{f}|^2$

![[Convolution and correlation.png]]

# Parseval's theorem
- Apply the inverse transform to the Wiener-Kinchin theorem
$$\int_{-\infty}^\infty[f(x)]^*g(x)\,dx=\int_{-\infty}^\infty [\tilde{f}(k)]^*\tilde{g}(k)\,dk$$

- Special case of $g=f$:
$$\int_{-\infty}^\infty |f(x)|^2\,dx=\int_{-\infty}^\infty |\tilde{f}(k)|^2\,dk$$

- The Fourier transform is a [[Vectors and matrices|unitary transformation]] that preserves the inner product

# Power spectra
- The _power spectrum_ is defined as:
$$\Phi(k)=|\tilde{f}(k)|^2$$
- Quantifies _spectral content_ of $f(x)$

- Wiener-Kinchin Theorem: $\Phi$ is the Fourier transform of the autocorrelation

- The spectrum of a perfectly periodic signal consists of a series of $\delta$ functions
	- Its autocorrelation function does not decay

- _White noise_ is an ideal random signal with an autocorrelation proportional to $\delta(t)$
	- It is _decorrelated_, with a flat spectrum

- Less ideal signals: peaks + white noise

# Solving ODEs with Fourier Transforms
- Suppose $\psi$ satisfies:
$$\frac{d^2\psi}{dx^2}-a^2\psi=-f(x)$$
- Let it satisfy the two boundary conditions:
$$\lim_{|x|\to\infty}|\psi|=0$$
- Apply a Fourier transform to both sides and use previous results:
$$-k^2\tilde{\psi}-a^2\tilde{\psi}=-\tilde{f}$$
$$\tilde{\psi}=\frac{\tilde{f}}{k^2+a^2}$$
- From this, the solution is:
$$\psi=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty e^{ikx}\frac{\tilde{f}}{k^2+a^2}\,dk$$
