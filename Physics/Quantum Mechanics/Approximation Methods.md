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
- To the _first order_, the _perturbed eigenstate_ os:
$$\displaylines{\ket{n}\approx \ket{n^{(0)}}+\lambda\ket{n^{(1)}} \\ \ket{n}=\ket{n^{(0)}}+\sum_{E_m^{(0)}\neq E_n^{(0)}}\ket{m^{(0)}}\frac{\braket{m^{(0)}|\hat{H'}|n^{(0)}}}{E_n^{(0)}-E_m^{(0)}}}$$

## Second-order perturbation theory
- For the $\lambda^2$ terms:

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