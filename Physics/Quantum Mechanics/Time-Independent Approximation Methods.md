- Methods:
	- Perturbation Theory
	- The variational method

# Time-independent perturbation theory
- Consider an _"unperturbed"_ Hamiltonian $\hat{H}^{(0)}$, with _known_ eigenstates and eigenvalues:
$$\hat{H}^{(0)}\ket{n^{(0)}}=E_n^{(0)}\ket{n^{(0)}}\hspace{1.5cm}\braket{n^{(0)}|m^{(0)}}=\delta_{nm}$$
- Then _perturb_ the Hamiltonian with an additional term:
$$\hat{H}=\hat{H}^{(0)}+\hat{H}'$$
- The perturbation must be _time-independent_, and "small" such that:
$$\braket{n^{(0)}|\hat{H}|n^{(0)}}<<E_n^{(0)}$$
- The eigenfunctions of $H$ are then obtained by a series of _corrections_, each with an additional _order_ of $\mean{H'}/\mean{H^{(0)}}$:
$$\hat{H}\ket{n}=E_n\ket{n}$$
- To keep track of order, add a _dimensionless parameter_ $\lambda$:
$$\hat{H}'\equiv\lambda\hat{H}^{(1)}$$
- The equation to be solved is then:
$$(\hat{H}^{(0)}+\lambda\hat{H}^{(1)})\ket{n}=E_n\ket{n}$$
- Then look for _power series solutions_:
$$E_n=\sum_m\lambda^mE_n^{(m)}\hspace{2cm}\ket{n}=\sum_m\lambda^m\ket{n^{(m)}}$$
- This assumes that eigenfunctions _evolve smoothly_ from the unperturbed state as $\lambda$ increases (the perturbation is "switched on")

- Substituting the solutions and _comparing terms_:
$$\displaylines{\hat{H}^{(0)}\ket{n^{(0)}}=E_n^{(0)}\ket{n^(0)} \\ \hat{H}^{(0)}\ket{n^{(1)}}+\hat{H}^{(1)}\ket{n^{(0)}}=E_n^{(0)}\ket{n^{(1)}}+E_n^{(1)}\ket{n^{(0)}} \\ \vdots \\  \hat{H}^{(0)}\ket{n^{(k)}}+\hat{H}^{(1)}\ket{n^{(k-1)}}=E_n^{(0)}\ket{n^{(k)}}+E_n^{(1)}\ket{n^{(k-1)}}+\dots+E_n^{(k)}\ket{n^{(0)}}}$$
- One can _choose_ $\ket{n^{(k)}}$ to be _orthogonal_ to $\ket{n^{(0)}}$
	- If $\ket{n^{(k)}}$ is a solution, $\ket{n^{(k)}}+c\ket{n^{(0)}}$ is a solution and can be used to make it _orthogonal_
$$\braket{n^{(k)}|n^{(0)}}=0\;\;\text{   for }n=1,2,3\dots$$

## First-order perturbation theory
- Consider the _first order correction_:
$$\hat{H}^{(0)}\ket{n^{(1)}}+\hat{H}^{(1)}\ket{n^{(0)}}=E_n^{(0)}\ket{n^{(1)}}+E_n^{(1)}\ket{n^{(0)}}$$
- Taking the _inner product_ of both sides with $\ket{n^{(0)}}$, the terms with $\braket{n^{(1)}|n^{(0)}}$ _zero_:
$$E_n^{(1)}=\braket{n^{(0)}|\hat{H}^{(1)}|n^{(0)}}$$
- This gives the _first order energy correction_ $\Delta E_n^{(1)}=\lambda E_n^{(1)}$:
$$\Delta E_n^{(1)}=\braket{n^{(0)}|\hat{H}'|n^{(0)}}$$
- This is _independent of_ $\lambda$

- As for the _wave function correction_ $\ket{\Delta n}^{(1)}=\lambda\ket{n^{(1)}}$, express it _in terms of the unperturbed eigenstates_:
$$\ket{n^{(1)}}=\sum_m\braket{m^{(0)}|n^{(1)}}\ket{m^{(0)}}$$
- Taking the inner product of the _equation above_ with $\ket{m^{(0)}}$, _for_ $n\neq m$:
$$E_m^{(0)}\braket{m^{(0)}|n^{(1)}}+\braket{m^{(0)}|\hat{H}^{(1)}|n^{(0)}}=E_n^{(0)}\braket{m^{(0)}|n^{(1)}}$$
- Provided the unperturbed states are _non-degenerate_:
$$\braket{m^{(0)}|n^{(1)}}=\frac{\braket{m^{(0)}|\hat{H}^{(1)}|n^{(0)}}}{E_n^{(0)}-E_m^{(0)}}$$
- To the _first order_, the _perturbed eigenstate_ is:
$$\displaylines{\ket{n}\approx \ket{n^{(0)}}+\lambda\ket{n^{(1)}} \\ \ket{n}=\ket{n^{(0)}}+\sum_{E_m^{(0)}\neq E_n^{(0)}}\ket{m^{(0)}}\frac{\braket{m^{(0)}|\hat{H'}|n^{(0)}}}{E_n^{(0)}-E_m^{(0)}}}$$

## Second-order perturbation theory
- For the $\lambda^2$ terms:
$$\hat{H}^{(0)}\ket{n^{(2)}}+\hat{H}^{(1)}\ket{n^{(1)}}=E_{n}^{(0)}\ket{n^{(2)}} +E_{n}^{(1)}  \ket{n^{(1)}}+E_{n}^{(2)}\ket{n^{(0)}}  $$

- Taking the inner product with $\ket{n^{(0)}}$, one gets:
$$\braket{n^{(0)}|\hat{H}^{(1)}|n^{(1)}}=E_n^{(2)}$$
- Substituting the equation for $\ket{n^{(1)}}$:
$$E_n^{(2)}=\sum_{E_m^{(0)}\neq E_n^{(0)}} \braket{m^{(0)}|n^{(1)}}\braket{n^{(0)}|\hat{H}^{(1)}|m^{(0)}}$$
- Substituting for the inner products, and multiplying by $\lambda^2$ gives the _second order energy correction_:
$$\Delta E_n^{(2)}=\sum_{E_m^{(0)}\neq E_n^{(0)}} \frac{|\braket{m^{(0)}|\hat{H}'|n^{(0)}}|^2}{E_n^{(0)}-E_m^{(0)}}$$

## Examples 

### Bump in the square well
- Let there be a small _bump_ of height $\epsilon$ in the _square well_:
$$\hat{H}'=\begin{cases}\epsilon &\text{for }|x|<b \\0 &\text{otherwise} \end{cases}$$
![[Bumpy square well.png]]
- For the _unperturbed_ Hamiltonian:
$$\displaylines{E_n^{(0)}=\frac{\hbar^2}{2m}\frac{n^2\pi^2}{4a^2}=n^2E_0 \\ \psi_n(x)=\sqrt{\frac{1}{a}}\sin\left[\frac{n\pi}{2a}(x+a)\right]}$$
- The _first order correction_ is found to be:
$$\Delta E_n^{(1)}=\braket{n^{(0)}|\hat{H}'|n^{(0)}}=\epsilon\int_{-b}^b|\psi_n(x)|^2\,dx=\epsilon\left[\frac{b}{a}-\frac{(-1)^n}{n\pi}\sin\left(\frac{n\pi b}{a}\right)\right]$$
- For the _ground_ and _first excited states_:
$$\Delta E_1^{(1)}=\frac{\epsilon}{a}\left[b+\frac{a}{\pi}\sin\left(\frac{\pi b}{a}\right)\right]\hspace{1.5cm}\Delta E_2^{(1)}=\frac{\epsilon}{a}\left[b-\frac{a}{2\pi}\sin\left(\frac{2\pi b}{a}\right)\right]$$
![[Bumped square well energies.png]]
- For a _narrow bump_ $(b\ll a)$, the equation is approximately:
$$\Delta E_n^{(1)}\approx\frac{\epsilon b}{a}[1-(-1)^n]$$
- This is _zero for even states_
	- For _odd states_, the wave function is _maximal near the bump_
	- For _even states_, the wave function _vanishes near the bump_

- As for the _wave functions_, the _symmetry_ (odd/even) of the wave functions is _preserved_
	- When calculating $\braket{m^{(0)}|\hat{H}'|n^{(0)}}$, terms with _odd_ $m+n$ will _vanish_
- They also satisfy $\psi(\pm a)=0$, and are _continuous everywhere_ as expected

### Square well in an electric field
- Applying an _electric field_ corresponds to adding some _perturbation_ $\hat{H}'=-q\mathcal{E}x$
- Let the perturbation be:
$$\hat{H}'=\epsilon x$$
- By _symmetry_, all _first order energy corrections vanish_:
$$\Delta E_n^{(1)}=\epsilon \int_{-a}^a x|\psi_n(x)|^2\,dx=0$$
- Calculating the _inner products_:
$$\braket{m^{(0)}|x|n^{(0)}}=\frac{1}{a}\int_{-a}^a x\sin\left[\frac{m\pi}{2a}(x+a)\right]\sin\left[\frac{n\pi}{2a}(x+a)\right]\,dx$$
- The integral _vanishes_ for _even_ $n+m$
- _Otherwise_:
$$\braket{m^{(0)}|x|n^{(0)}}=-\frac{16a}{\pi^2}\frac{mn}{(m^2-n^2)^2}$$
- This gives the _change in wave-functions_:
$$\Delta\ket{n^{(1)}}=\frac{\epsilon a}{E_0}\frac{16n}{\pi^2\sqrt{a}}\sum_{m+n\text{ odd}}\frac{m}{(m^2-n^2)^3}\sin\left[\frac{m\pi}{2a}(x+a)\right]$$
- For the _ground state_ $(n=1)$, only $m=2$ contributes significantly, due to $1/(m^2-n^2)^3$
![[Skewed well perturbation.png]]

- The _leading energy corrections_ are _quadratic_:
$$\displaylines{\Delta E_n^{(2)}=\frac{\epsilon^2}{E_0}\sum_{n\ne m}\frac{|\braket{m^{(0)}|x|n^{(0)}}|^2}{n^2-m^2}\\ \frac{\Delta E_n^{(2)}}{E_n^{(0)}}=-\left(\frac{\epsilon a}{E_0}\right)^2\left(\frac{16}{\pi^2}\right)^2 \sum_{m+n\text{ odd}}\frac{m^2}{(m^2-n^2)^3}}$$
- For the _ground state_, only _even $m$_ contributes, and is still _dominated_ by $m=2$

### Harmonic oscillator with linear perturbation
- Add a _linear term_ to the Hamiltonian for the [[Quantum Harmonic Oscillator]]:
$$\hat{H}=\frac{\hat{p}^2}{2m}+\frac{1}{2}m\omega ^2\hat{x}^2+\epsilon\hat{x}$$
- Using the fact that $\hat{x}\propto (\hat{a}+\hat{a}^\dagger)$, one sees that _first order energy corrections vanish_ $\forall n$
- One can calculate the _second order_ energies:
$$E_n=E_n^{(0)}+\frac{\hbar \epsilon^2}{2m\omega}\left(\frac{n}{E_n^{(0)}-E_{n-1}^{(0)}}+\frac{n+1}{E_n^{(0)}-E_{n+1}^{(0)}}\right)$$
- As the energy levels are _evenly spaced_:
$$E_n=\left(n+\frac{1}{2}\right)\hbar\omega-\frac{\epsilon^2}{2m\omega^2}$$

- This can be found from the _true solution_, found from _rewriting the potential_:
$$V(x)=\frac{1}{2}m\omega^2\left(x+\frac{\epsilon}{2m\omega^2}\right)^2 -\frac{\epsilon^2}{2m\omega^2}$$
- Hence, _all energy levels_ are _lowered_ by a _common amount_

### Van der Waals interaction
![[van der Waals.png]]
$$\displaylines{\hat{H}=\hat{H}_0+V \\ \hat{H}_0=-\frac{\hbar^{2}}{2m_{e}}(\nabla_{1}^{2}+\nabla_{2}^{2})-\frac{e^{2}}{4\pi\epsilon_{0}r_{1}}-\frac{e^{2}}{4\pi\epsilon_{0}r_{2}} \\ V=\frac{e^2}{4\pi\epsilon_0}\left(\frac{1}{r}+ \frac{1}{|\boldsymbol{r}+\boldsymbol{r}_{2}-\boldsymbol{r}_{1}|} -\frac{1}{|\boldsymbol{r}-\boldsymbol{r}_{2}|}-\frac{1}{|\boldsymbol{r}-\boldsymbol{r}_{1}|}\right)}$$
- If $r$ is _large_ enough, $V$ is treated as a _perturbation_

- The _perturbed ground state_ is the _product_ of two [[3D time-independent Hamiltonians#The hydrogen-like atom|hydrogen atom ground states]] $\ket{nlm}=\ket{100}$:
$$\ket{0^{(0)}} =\ket{100(\boldsymbol{r}_{1})}\ket{100(\boldsymbol{r}_{2})} \hspace{1.5cm} \hat{H}_{0}\ket{0^{(0)}} =-2R_{\infty}\ket{0^{(0)}}    $$

- For $r\gg a_0$, one can use a _multipole expansion_ for $V$, in _powers_ of $r_{i}/r$
$$V=\frac{e^{2}}{4\pi\epsilon_{0}r^{3}}(x_{1}x_{2}+y_{1}y_{2}-2z_{1}z_{2})+\mathcal{O}\left( \frac{1}{r^{4}} \right)$$
- To leading order, this corresponds to an _interaction between two electric dipoles_ $e\boldsymbol{r}_{1},e\boldsymbol{r}_{2}$

- The _first order correction vanishes_ by _symmetry_:
$$\displaylines{\braket{ 100|x_{1,2} | 100 } = \braket{ 100|y_{1,2} | 100 } = \braket{ 100|z_{1,2} | 100 } =0 \\ \Delta E_{0}^{(1)}=\braket{ 0^{(0)}|V |0^{(0)}  }=0 }$$

- The _second order energy correction_:
$$\Delta E^{(2)}(r)=\left( \frac{e^{2}}{4\pi\epsilon_{0}} \frac{1}{r^{3}} \right)^{2}\sum_{k\neq 0} \frac{|\braket{ k^{(0)}|(x_{1}x_{2}+y_{1}y_{2}-2z_{1}z_{2}) | 0^{(0)} }|^{2}}{E_{0}^{(0)}-E_{k}^{(0)}} $$
- It _varies as_ $1/r^6$, and is _attractive_ since the energy correction is _negative_
	- Negative: $E_{0}^{(0)}<E_{k}^{(0)}$
- This gives the _van der Waals' potential_
## Degenerate perturbation theory
- If a pair of _zeroth order eigenstates_ are _degenerate in energy_:
$$\braket{m^{(0)}|\hat{H}^{(1)}|n^{(0)}}=0\;\;\;\text{   for } n\neq m$$
- As the zeroth order states and the Hamiltonian are _given quantities_, there is _no guarantee that this occurs_
- The original _degenerate eigenstates_, with _degeneracy_ $g$:
$$\hat{H}^{(0)}\ket{n_j^{(0)}}=E_n^{(0)}\ket{n_j^{(0)}}\hspace{1.5cm}j=1,2,\dots g$$

- Form a _new basis from the degnerate eigenstates_:
$$\hat{H}^{(0)}(c_1\ket{n_j^{(0)}}+c_2\ket{n_k^{(0)}})=E_n^{(0)}(c_1\ket{n_j^{(0)}}+c_2\ket{n_k^{(0)}})$$
- One should then make sure the _basis satisfies the condition_:
$$H'_{\alpha\beta}\equiv\braket{n^{(0)}_\alpha|\hat{H}'|n^{(0)}_\beta}=E'_{n,\alpha}\delta_{\alpha\beta}$$
- This _diagonalises_ a _block_ of the matrix corresponding to the _degenerate eigenstates_:
$$H'=\text{diag}(E_{n,1}',E_{n,2}',\dots E_{n,g}')$$
- $E_{n,\alpha}'$ are a set of _constants_
- To find the energies, one can diagonalise the $g\times g$ matrix $H'_{jk}=\braket{n_j^{(0)}|\hat{H}'|n_k^{(0)}}$

- One can also _diagonalise_ the matrix _without explicitly solving for eigenvalues_ in the $\ket{n_j^{(0)}}$ basis, use the fact that _commuting operators have common eigenvectors_
- Therefore, one should find a basis that _diagonalises_ $\hat{A}$, where $[\hat{A},\hat{H}]=0$

- The _first order corrections_ are then just the _eigenvalues_ $E'_{n,\alpha}$:
$$\Delta E_{n,\alpha}^{(1)}=\braket{n_\alpha^{(0)}|\hat{H}'|n_\alpha^{(0)}}=E'_{n,\alpha}$$
- In general, the eigenvalues are _different_
- The energy level then _splits_:
![[Degenerate perturbation.png]]

### Example: 2D square well
- A well of _width_ $2a$
- The _unperturbed energies_:
$$E_{n_{x},n_{y}}^{(0)}=(n_{x}^{2}+n_{y}^{2})E_{0}$$
- All states with $n_{x}\neq n_{y}$ are _degenerate_ with $g=2$
- Consider the _first excited state_, which has _degenerate eigenvectors_ $\ket{1,2}$ and $\ket{2,1}$
- Apply _perturbation_:
$$H'=\epsilon xy$$

- Diagonalising:
![[degenerate square well.png]]
$$A=\epsilon a^{2}\left( \frac{32}{9\pi^{2}} \right)^{2}$$
# Variational method
- The _variational method_ gives an _upper bound_ of eigenstate energies for _any_ $\hat{H}$
- The method relies on _guessing and optimising trial wavefunctions_ $\psi_\text{trial}(\alpha_i)$, depending on some _variational parameters_ $\alpha_i$
- The optimising involves _minimising the trial energy_

- Consider a Hamiltonian with _unknown eigenstates and energies_:
$$\hat{H}\ket{n}=E_n\ket{n}$$
- Introdced some _normalised trial state_ $\ket{\psi(\alpha)}$:
$$\ket{\psi(\alpha)}=\sum_n a_n(\alpha)\ket{\alpha}\hspace{1.5cm}\sum_n|a_n(\alpha)|^2=1$$
- The _expectation value_ is then:
$$E_\alpha\equiv\braket{\psi(\alpha)|\hat{H}|\psi(\alpha)}=\sum_n E_{n}|c_{n}|^{2}\geq E_{0}\sum_{n}|c_{n}|^{2}$$
- Therefore:
$$E_\alpha\geq E_0$$
# Rayleigh-Ritz method
- A type of the variational method, using a _trial wave fucntion_ of the form:
$$\psi(\bm{r})=\sum_j\alpha_j\psi_j(\bm{r})$$
- $\psi_j$ are a _linearly independent set_ of wavefunctions, which are _not necessarily complete or orthonormal_
- The quantity to be _minimised_ according to the variational principle:
$$\left<E\right>=\frac{\braket{ \psi |\hat{H} |\psi  }}{\braket{ \psi |\psi  } }=\frac{\sum_{j,k} \alpha_{j}\alpha_{k} H_{jk}}{\sum_{j,k}\alpha_{j}\alpha_{k}S_{jk}}  $$

- Define the matrices ($S$ is the _overlap matrix_):
$$H_{jk}=\braket{\psi_j|\hat{H}|\psi_k}=H_{kj}^* \hspace{1.5cm} S_{jk}=\braket{\psi_j|\psi_k}=S_{kj}^*$$
- The basis set is _not necessarily orthonormal_, hence the matrix elements _are not diagonalised_

- By _minimising_ the estimate of ground state energy w.r.t. $\alpha_{j}$, one gets:
$$\sum_k\alpha_k(H_{jk}-ES_{jk})=0$$
- One can represent this with a _matrix equation_:
$$(\dunderline{H}-E\dunderline{S})\cdot\underline{\alpha}=0$$
- To get _non-trivial solutions_:
$$\text{det}(\dunderline{H}-E\dunderline{S})=0$$
- This is known as the _secular equation_
- The _lowest solution_ for $E$ gives the _upper bound for ground state energy_

# JWKB method and stationary phase
- A _semiclassical_ technique to obtain _approximate solutions_
- Therefore, it can be characterised by a _position-dependent wavenumber_

- From the 1D Schrodinger equation, for a _classical travelling wave regime_ $E>V$
$$\displaylines{H\psi(x)=E\psi(x) \\ H=-\frac{\hbar^{2}}{2m} \frac{d^{2}}{dx^{2}}+V(x) \\ \psi''(x)+k^{2}(x)\psi(x)=0 \\ k(x)\equiv \sqrt{ \frac{2m(E-V(x))}{\hbar^{2}} }}$$
- In the _semiclassical_ regime, the _potential_ on a lengthscale where there are _many wavelengths_ (slow-varying potential)
	- The wavefunction is approximately _sinusoidal_, with _slowly varying_ amplitude and wavelength

- Take the form:
$$\psi(x)=\exp\left( \frac{iS}{\hbar} \right)$$
- This gives:
$$\left( \frac{iS''}{\hbar}-\frac{S'^{2}}{\hbar^{2}}+k^{2} \right)\exp(iS)=0$$
- In the _semiclassical regime_, take $\hbar S''\ll S'^{2}$

- This gives $S'=\pm \hbar k$
	- As expected, in comparison to the _classical wave_

- _Iterating_, one gets:
$$S'\approx \pm \hbar k +\frac{i\hbar}{2} \frac{k'(x)}{k}$$
- Integrating:
$$\begin{align} S(x)&\approx \pm \int^{x} \hbar k(x') \, dx' +\frac{i\hbar}{2} \int ^{x} \frac{k'(x')}{k(x')} \, dx'+C \\ &=\pm \hbar \int ^{x}k(x') \, dx'+\frac{i\hbar}{2}\ln(k(x))+C   \end{align}$$

- This gives the wave function:
$$\psi(x)=\frac{C}{\sqrt{ k(x) }}\exp\left[ \pm i \int^{x}k(x')  \, dx'  \right]$$
- Examining the formula, $S''\ll(S')^{2}$ holds

- The _wavelength_ $\lambda \sim 1/k$ means $\lambda(dV/dx)\ll \hbar^{2}k^{2}/2m$, or the _potential energy slowly varies_ compared to _kinetic energy_

- In the semiclassical approximation, $p\approx \hbar k$

- The approximation _breaks down_ in the _classically forbidden_ region, where $E<V$
- In this case, define $\kappa$ where $\kappa^{2}=-k^{2}$
- This gives _exponentially growing_ or _decaying_ wave functions
- Following the same derivation:
$$\psi(x)=\frac{C}{\sqrt{ \kappa(x) }}\exp\left[ \pm \int^{x} \kappa(x') \, dx'  \right]$$

## Connection formulae
- _Connect_ the classical and decaying regimes of the wave-function

- At the _turning point_, _approximate_ the potential as _linear_, and $k^{2}(x)=0$
- One can then find formulae to _connect_ the solutions between the semiclassical, and exponentially _decaying_ regions

- One can then write:
$$k^{2}=\frac{2m}{\hbar^{2}}\left( - \frac{dV}{dx} \right)\Bigg|_{x=a}(x-a)$$
- Make the substitutions:
$$z=\alpha(x-a)\hspace{1.5cm}\alpha^{3}=\frac{2m}{\hbar^{2}} \frac{dV}{dx}>0$$
- This gives the _Airy equation_:
$$f''-zf(z)=0$$
- This gives a _well-behaved function_ which converges to the _limits_ of the semiclassical and classically forbidden regions

### Airy equation
- Note _symptotic behaviour_ for $|z| \to \infty$
- _Fourier transform_ the Airy equation:
$$\displaylines{if'(k)+k^{2}f(k)=0 \implies f(k)=A\exp\left( \frac{ik^{3}}{3} \right) \\ f(z)=\frac{1}{2\pi}\int \exp\left[ i\left( \frac{k^{3}}{3}+kz \right) \right] \, dk }$$
- As the equation is _second order_, this must generate _two independent solutions_
- This is dependent on the _integration contour_

- Go to _large_ $|k|$ such that the $k^{3}$ term dominates in the phase
- The integrand _vanishes_ when there is a _negative real part_ in the exponential
	- This occurs in 3 _separate regions_ of angular width $\pi/3$

- The function _falls off quickly_ when entering a region where the real part is _negative_
- Hence, find the _stationary points of the region_
	- From the [[Elementary Analysis#The Cauchy-Riemann equations|Cauchy-Riemann equations]], the _stationary/saddle points_ necessarily lead to the _maximisation_ of the real part

- The _stationary points_ of the _exponent_ lie in:
$$\displaylines{k_\text{sp}^{2}+z=0 \implies k_\text{sp}=\begin{cases}\pm i\sqrt{ z } &z>0 \\ \pm i\sqrt{ |z| } &z<0\end{cases} \\ \exp\left( i \frac{k_\text{sp}^{3}}{3}+ik_\text{sp}z \right)=\begin{cases}\exp\left( \mp \frac{2}{3}z^{3/2}\right) &z>0  \\ \exp\left( \mp i \frac{2}{3} |z|^{3/2}\right) &z<0\end{cases}}$$
- For _large_ $|z|$, the _decay_ of the integrand becomes _quicker_
- Method of _steepest descent_


![[Airy integrate.png]]

- Two different contours
- Two different Airy functions

- The _Airy function_ $\text{Ai}(z)$ _connects_ the wave-functions at the turning point
![[Airy equation.png]]

- Bohr-Sommerfeld quantisation condition