- Deal with _effective field theories_ at some range of energy

- Consider $D-$dimensional theories, where $D$ is the _number of parameters_ the quantum field depends on
- The _action_, a _functional_ of the path
$$S[\phi]=\int  d^Dx\,\mathcal{L}[\phi(\{x\})]\quad x^{i}=x^{0},x^{1}\dots x^{D-1} $$

- _String theory_ is a 2D quantum field theory
	- A 1D object _sweeps out_ a 2D _world sheet_ in spacetime
	- String theory describes the _embedding_ of the sheet in 10 or 26-dimensional spacetime
	- The _action_ depends on parameters of the 2D sheet

# Path integrals
- The evolution of a _quantum state_, and the _position-space wave function_
$$\displaylines{\ket{ \psi(t)}=\exp\left( -\frac{iHt}{\hbar} \right)\ket{\psi(0)}  \\ \psi(x,t)=\braket{ x |\psi(t)  }=\braket{ x | \exp(-iHt/\hbar)|\psi(0) }  }$$
- Inserting a _set_ of position kets inbetween, one can express it in terms of an _integral_, where the _kernel_ is known as the _propagator_
$$\begin{align}
\psi(x,t)&=\int  dx' \, \braket{ x|\exp [-iH(t-t')/\hbar] | x' }  \psi(x',t') \\
&\equiv \int  dx' \,U(x,t,x',t')\psi(x',t')
\end{align}$$
- The propagator describes a _transition_ between wavefunctions in spacetime

- This leads to the _path integral formulation_ of QFT

## Expressing propagator as path integral
- _Split_ the evolution of the wavefunction into timesteps of width $\Delta t$
- The propagator is a _sum of possible paths_
$$\displaylines{t_{i}=t_{0}\quad t_{f}=t_{N+1}\quad x_{r}=x(t_{r}) \\ U(x_{f},t_{f},x_{i},t_{i})= \int  dx_{1}\dots dx_{N} \prod_{r=0}^{N} \Braket{ x_{r+1} |\exp\left( -\frac{i}{\hbar}H(t_{r+1}-t_{r}) \right)|t_{r}  } }$$
- One matrix element within the product:
$$U_{r+1,r}=\braket{ x_{r+1}|\exp(-iH\Delta t/\hbar) | x_{r} }  $$
- The Hamiltonian will be of the form:
$$H=\frac{p^{2}}{2m}+V(x)$$
- The _Suzuki-Trotter decomposition_:
$$\exp[\epsilon(A+B)]=\exp(\epsilon A)\exp(\epsilon B)(1+O(\epsilon))$$
- As potential is a function of position:
$$U_{r+1,r}=\Braket{ x_{r+1} |\exp\left( \frac{p^{2}}{2imh}\Delta t \right)| x_{r} }\exp\left( -\frac{i}{\hbar}V(x_{r}) \right) $$
- Inserting a _full set of momentum eigenstates_, one gets a _Gaussian integral_:
$$\begin{align}\Braket{ x_{r+1} |\exp\left( \frac{p^{2}}{2imh}\Delta t \right)| x_{r} }&=\int  \frac{dp}{2\pi \hbar} \exp\left( -\frac{i}{\hbar}\frac{p^{2}}{2m}\Delta t+\frac{i}{\hbar}p(x_{r+1}-x_{r}) \right) \\ &=\sqrt{ \frac{m}{2\pi i\hbar\Delta t} } \exp\left( \frac{i}{\hbar} \frac{m}{2}\left( \frac{x_{r+1}-x_{r}}{\Delta t} \right)^{2}\Delta t \right)
\end{align}$$
- From this, the propagator, for $N\Delta t=t_{f}-t_{i}$
$$\begin{align}
U(x_{f},t_{f},x_{i},t_{i})&=\lim_{\substack{\Delta t \to 0  \\ N\to \infty}}
\int  \prod_{r=1}^{N}dx_{r}\,\left( \frac{m}{2\pi i\hbar\Delta t} \right)^{(N+1)/2} \\ &\times \exp\left( \frac{i}{\hbar}\sum_{r=0}^{N}\left[\frac{m}{2}\left( \frac{x_{r+1}-x_{r}}{\Delta t} \right)^{2}-V(x_{r})\right] \Delta t\right)  
\end{align}$$
- This is a _path integral_
	- As an _effective field theory_, it converges for some _scale_

- It can be written as:
$$\displaylines{U(x_{f},t_{f},x_{i},t_{i})=N \int_{x(t_{i})=x_{i}}^{x(t_{f})=x_{f}}  \mathcal{D}x\,\exp\left( \frac{i}{\hbar}S[x(t)] \right)  \\ S[x]=\int_{t_{i}}^{t_f}  dt\,L(x,t) }$$
- Analogy: _slit interference_, adding an $N-$slit at every point in space

- The path integral is a _sum of paths_, _weighted_ by some _phase factor_ determined by the action
	- A _functional integral_, integrating over a _space of functions_

- Drawing an analogy to _statistical fields_, one may use an _imaginary time_
	- Known as a _Wick rotation_
	- Might give better _convergence_
	- $S_{E}$ is analagous to the _Hamiltonian_, making the path integral a _partition function_
$$\int_{i}^{f}  \mathcal{Dx}\exp(-S_{E}[x]) \qquad S_{E}[x]=\int  d\tau\,\left( \left( \frac{dx}{d\tau} \right)^{2}+V(x) \right)  $$

## Functional derivatives
- Evaluating the integral may require a _functional derivative_:
$$\displaylines{\frac{\delta L[x(t')]}{\delta x(t)}=\lim_{ \epsilon \to 0 } \frac{L[x(t')+\epsilon\delta(t-t')]-L[x(t')]}{\epsilon} \\ \frac{\delta S[x]}{\delta x(t)}=\lim_{ \epsilon \to 0 } \int  dt'\, \frac{L[x(t')+\epsilon\delta(t-t')]-L[x(t')]}{\epsilon} }$$
- A $D-$dimensional result:
$$\frac{\delta \phi(x)}{\delta \phi(y)}=\delta^{D}(x-y)$$
### Example: Klein-Gordon action
$$S[\phi]=\int  d^4x\left( \frac{1}{2}\partial_{\mu}\phi\partial^{\mu}\phi-\frac{1}{2}m^{2}\phi^{2} \right) $$
- The functional derivative:
$$\frac{\delta S[\phi]}{\delta \phi(y)}=\int  d^4x(-\Box\phi(x)-m^{2}\phi(x))\delta^{4}(x-y)=-(\Box_{y}+m^{2})\phi(y) $$
- Setting it at zero gives the _Klein-Gordon equation_

## Time ordering
- Consider some _correlation function_ with Heisenerg operators $X_{H}$
$$\displaylines{\braket{ x_{f},t_{f}|X_{H}(t_{1})X_{H}(t_{2}) |x_{i},t_{i}  } \qquad t_{f}>t_{1}>t_{2}>t_{i}\\ X_{H}(t)=\exp\left( \frac{iHt}{\hbar} \right)X(0)\exp\left( -\frac{iHt}{\hbar} \right)}$$
- Let them be _position operators_, inserting a set of basis states:
$$\int  dx_{1}\,dx_{2} \,\braket{ x_{f},t_{f} | x_{1},t_{1} } \braket{ x_{1},t_{1} |x_{2},t_{2}  }\braket{ x_{2},t_{2} |x_{i},t_{i}  }\,x_{1}x_{2}  $$
- Expressing it as a path integral (with some _normalisation_ $\mathcal{N}$)
$$\braket{ x_{f},t_{f}|x(t_{1})x(t_{2}) |x_{i},t_{i}  }=\mathcal{N} \int_{i}^{f}  \mathcal{D}x\,x(t_{1})x(t_{2}) \exp\left( -\frac{iS[x]}{\hbar} \right)$$
- If one _swaps_ $t_{1},t_{2}$, one gets the _same integral_

- By _construction_, the path integral gives _time ordered correlations_
	- With _Wick rotation_ into imaginary time, there may be _radial ordering_

- With _normalisation_, one gets $\mathcal{N}^{-1}$, thus one can write the _normalised time ordered correlation function_:
$$\frac{\braket{ x_{f}t_{f} |T\{O(x_{1})\dots O(x_{n})\}| x_{i}t_{i} }}{\braket{ x_{f}t_{f}| x_{i}t_{i}  } } =\frac{\int  \mathcal{D}x\,O(x_{1})\dots O(x_{n})\exp(iS[x]/\hbar) }{\int  \mathcal{D}x \,\exp(iS[x]/\hbar)}$$
## Canonical commutation relations
- Consider the _commutation_:
$$\braket{ x_{f}t_{f}|[x(t),p(t)] |x_{i}t_{i}  } $$
- Define _composite functions_ in the _path integral_:
$$x(t)p(t)=\lim_{ \epsilon \to 0 }x(t+\epsilon)p(t) $$
- Consider some function $F$ of $x(t)$:
$$\left\langle  \frac{\delta F}{\delta x(t)}  \right\rangle =\Braket{ x_{f}t_{f}|\frac{\delta F}{\delta x(t)} |  x_{i}t_{i}}=\int_{i}^{f}  \mathcal{D}x \frac{\,\delta F}{\delta x(t)}\exp\left( \frac{iS[x]}{\hbar} \right)  $$
- Assume that for functionals, there is some analagogue of _Stokes Theorem_ and _integration by parts_:
$$\left\langle  \frac{\delta F}{\delta x(t)}  \right\rangle=-\frac{i}{\hbar}\left\langle  F\,\frac{\delta S}{\delta x(t)}  \right\rangle  $$
- Going back to the _discretised_ limit, the action is:
$$\displaylines{S[x]=\sum_{r} \left[ \frac{m}{2} \frac{(x_{r+1}-x_{r})^{2}}{\delta t^{2}} -V(x_{r})\right]\delta t\\ \frac{\delta S}{\delta x(t)}\to\frac{\partial S}{\partial x_{k}}=-m\left( \frac{x_{k+1}-x_{k}}{\delta t}- \frac{x_{k}-x_{k-1}}{\delta t} \right)}$$
- Going back to the functional derivative, with $F=x_{k}$:
$$1=-\frac{i}{\hbar}\left\langle -x_{k}m \left( \frac{x_{k+1}-x_{k}}{\delta t}- \frac{x_{k}-x_{k-1}}{\delta t} \right)\right\rangle  $$
- In the infinitesimal limit:
$$\lim_{ \delta t \to 0 } \frac{x_{k+1}-x_{k}}{\delta t}=m\dot{x}(t_{+})=p(t_{+}) \qquad \lim_{ \delta t \to 0 } \frac{x_{k}-x_{k-1}}{\delta t}=p(t_{-})  $$

- With time ordering:
$$1=-\frac{i}{\hbar}\langle p(t_{+})x(t)-x(t)p(t_{-}) \rangle $$

- This gives (with normalisation):
$$\langle x_{f},t_{f}|T\{x(t),p(t)\}|x_{i},t_{i} \rangle=i\hbar $$

## Generalisation to higher dimensions

# QFT in zero dimensions
- A quantum field theory with _no parameters_, as a _toy model_

- _No space or time_ coordinates, only a field $\phi \in \mathbb{R}$
- The _functionals_ become simple _functions_
- The _action_ has _no parameter to integrate over_

- Example: $\phi^{4}$ theory
$$S(\phi)=\frac{\alpha}{2}\phi^{2}+\frac{\lambda}{4!}\phi^{4}\qquad \alpha>0$$
## Generating function
 - The _generating function_:
$$Z_{\lambda}(J)=N\int_{-\infty}^{\infty}  d\phi\,e^{-S[\phi]+J\phi } $$
- An _analogue_ of the functional integral, with _imaginary "time"_
- _Normalisation factor_ $N$

- $J$ is some _source term_
- Differentiation w.r.t. $J$ then gives _powers_ of $\phi$
- The _expectation values_ can then be written as:
$$\langle \phi^{n} \rangle=N \int  d\phi\,\phi^{n}  e^{-S[\phi]}=\left[ \frac{\partial^{n}}{\partial J^{n}}Z_{\lambda}(J) \right]_{J=0}$$
- More generally:
$$\langle f(\phi) \rangle =\left[ f\left( \frac{\partial}{\partial J} \right)Z_{\lambda}(J) \right]_{J=0}$$

### Free case
$$Z_0(J)=N\int  d\phi\,\exp\left( -\frac{1}{2}\alpha \phi^{2}+J\phi \right) $$
- Choose $N$ such that:
$$Z_{0}(0)=1\implies N=\sqrt{ \frac{\alpha}{2\pi} }$$
- With this, one gets:
$$Z_{0}(J)=\exp\left( \frac{J^{2}}{2\alpha} \right)$$
- The _odd_ powered expectation values are $0$:
$$\langle \phi^{2n+1} \rangle=0 $$
- The _even_ powered expectation values:
$$\displaylines{\langle \phi^{2n} \rangle=\frac{1}{Z_{0}(0)}\left[ \frac{\partial^{2n}}{\partial J^{2n}} Z_{0}(J)\right] =\frac{(2n-1)!!}{\alpha^{n}} \\ n!! = n(n-2)(n-4)\dots \\ \langle \phi^{2} \rangle=\frac{1}{\alpha}\qquad \langle \phi^{4} \rangle=\frac{3}{\alpha^{2}}\qquad \langle \phi^{6} \rangle=\frac{15}{\alpha^{3}}   }$$
- This can be described using _Feynman diagrams_, where it gives $2n-$point _correlations_
- Each _propagator_ between points gives a factor of $\alpha^{-1}$, and the correlations are _weighted by a combinatoric factor_ $(2n-1)!!$
	- Combinatorics: $2n-1$ choices for first propagator, $2n-3$, and so on

### Interacting theory
$$Z_{\lambda}(J)=N \int  d\phi\,\exp\left( -\frac{1}{2}\alpha \phi^{2} -\frac{\lambda}{4!}\phi^{4}+J\phi\right) $$
- Choosing the same normalisation:
$$N=\frac{1}{Z_{0}(0)}=\sqrt{ \frac{\alpha}{2\pi} }$$
- Assume $\lambda\ll 1$, such that one can _expand_:
$$Z_{\lambda}(J)=\sqrt{ \frac{\alpha}{2\pi} }\int  d\phi\,\exp\left( -\frac{1}{2}\alpha \phi^{2}-\frac{\lambda}{4!}\phi^{4} \right)\sum_{k=0}^{\infty}\left( -\frac{\lambda}{4!} \right)^{k}\frac{\phi^{4k}}{k!} $$
- Make an _approximation_ by _swapping_ the sum and integral
	- Exact answer (no swap) has $\exp(-1/\lambda)$ _instanton_ factor
$$Z_{\lambda}(J)=\sum_{k} \frac{1}{k!}\left( -\frac{\lambda}{4!} \right)^{k}\int  d\phi\,\phi^{4k}\,\exp\left( -\frac{1}{2}\alpha \phi^{2}+J\phi \right) $$
- This consists of _expectation values in the free theory_
- Thus, one can write $Z_{\lambda}(J)$ _in terms of the free theory generating function_
$$\begin{align}
Z_{\lambda}(J)&=\sum_{k=0}^{\infty} \frac{1}{k!}\left( -\frac{\lambda}{4!} \right)^{k}\,\frac{\partial^{4k}}{\partial J^{4k}}Z_{0}(J) \\
&=Z_{0}(J)-\frac{\lambda}{4!} \frac{\partial^{4}}{\partial J^{4}}Z_{0}(J)+\frac{1}{2}\left( \frac{\lambda}{4!} \right)^{2}\frac{\partial^{8}}{\partial J^{8}}Z_{0}(J)+\dots
\end{align}$$
- Correlations with normalisation:
$$\langle \phi^{n} \rangle=\frac{1}{Z_{\lambda}(0)} \left[ \frac{\partial^{n}}{\partial J^{n}}Z_{\lambda}(J) \right]_{J=0} $$

### Normalisation, partition function, and vaccum bubbles
- $Z_{\lambda}(0)$ is known as the _partition function_
- It describes how _interactions_ affect the _vacuum_ and the _normalisation_ of correlations

- First few terms:
$$\begin{align}
Z_{\lambda}(0)&=1-\frac{\lambda}{8\alpha^{2}}+\frac{105}{2(4!)^{2}} \frac{\lambda^{2}}{\alpha^{4}}+\dots \\
&=1+(-\lambda) \left( \frac{1}{\alpha} \right)^{2}\left( \frac{1}{8} \right)+(-\lambda)^{2} \left( \frac{1}{\alpha^{4}} \right)\left( \frac{1}{48}+\frac{1}{16}+\frac{1}{128} \right)+\dots
\end{align}$$
- This can be expressed as a series of _vacuum bubbles_
![[Vacuum bubbles.png]]
- There is a factor of $\alpha^{-1}$ for each line
- A factor of $-\lambda$ for each _vertex_
- Then, one divides by a _symmetry factor_
	- The size of the _automorphism group_ of the graph
