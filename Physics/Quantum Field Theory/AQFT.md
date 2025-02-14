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
	- Known as a [[#Wick rotation and Euclidean QFT|Wick rotation]]
	- Might give better _convergence_
	- $S_{E}$ is analagous to the _Hamiltonian_, making the path integral a _partition function_
$$\int_{i}^{f}  \mathcal{Dx}\exp(-S_{E}[x]) \qquad S_{E}[x]=\int  d\tau\,\left( \left( \frac{dx}{d\tau} \right)^{2}+V(x) \right)  $$

## Functional derivatives
- Evaluating the integral may require a _functional derivative_:
$$\displaylines{\frac{\delta L[x(t')]}{\delta x(t)}=\lim_{ \epsilon \to 0 } \frac{L[x(t')+\epsilon\delta(t-t')]-L[x(t')]}{\epsilon} \\ \frac{\delta S[x]}{\delta x(t)}=\lim_{ \epsilon \to 0 } \int  dt'\, \frac{L[x(t')+\epsilon\delta(t-t')]-L[x(t')]}{\epsilon} }$$
- A $D-$dimensional result:
$$\frac{\delta \phi(x)}{\delta \phi(y)}=\delta^{D}(x-y)$$
- The _functional chain rule_:
$$\frac{\delta}{\delta \phi(x)}=\int  d^4y\, \frac{\delta J(y)}{\delta \phi(x)}  \frac{\delta}{\delta J(y)}$$
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
$$Z_{\lambda}(J)=\sqrt{ \frac{\alpha}{2\pi} }\int  d\phi\,\exp\left( -\frac{1}{2}\alpha \phi^{2}+J\phi\right)\sum_{k=0}^{\infty}\left( -\frac{\lambda}{4!} \right)^{k}\frac{\phi^{4k}}{k!} $$
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

## Normalisation, partition function, and vaccum bubbles
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

- The correlation function can be calculated using:
$$\begin{align}
\frac{Z_{\lambda}(J)}{Z_{\lambda}(0)}=&\left( 1+\frac{\lambda}{8\alpha^{2}}+\dots \right)\bigg[ 1-\frac{\lambda}{4!} \left( \frac{J^{4}}{\alpha^{4}} +\frac{6J^{2}}{\alpha^{3}}+\frac{3}{\alpha^{2}}\right) \\
&+ \frac{1}{2}\left( -\frac{\lambda}{4!} \right)^{2}\left( \frac{J^{8}}{\alpha^{8}}+\frac{28J^{6}}{\alpha^{7}}+\frac{210J^{4}}{\alpha^{6}}+\frac{420J^{2}}{\alpha^{5}}+\frac{105}{\alpha^{4}} \right)+\dots\bigg]Z_{0}(J)
\end{align}$$
## Two-point correlator
- The two-point correlation:
$$\langle \phi^{2} \rangle=\frac{1}{Z_{\lambda}(0)} \frac{\partial^{2}}{\partial J^{2}}Z_{\lambda}(J)\Bigg|_{J=0}$$
- Without $1/Z_{\lambda}(0)$, the _un-normalised_ diagrams:
![[Two point correlator unnormalised.png]]

- Any _vacuum contributions_ will be _cancelled out_ in the normalisation
- Evaluating the rest, one gets:
$$\langle \phi^{2} \rangle=\frac{1}{\alpha}+\frac{-\lambda}{\alpha^{3}} \left( \frac{1}{2} \right)+\frac{(-\lambda)^{2}}{\alpha^{5}}\left( \frac{1}{2^{2}}+\frac{1}{2^{2}}+\frac{1}{3!}\right)+\dots$$
![[Two point correlator diagram.png]]

# QFT in four dimensions
- In four dimensions, the _action_ is now a _functional_, where the Lagrangian density depends on fields with _four parameters_:
$$\displaylines{S=\int  d^4x\,\mathcal{L}[\boldsymbol{\phi}..] \\ \phi=\phi(x)\qquad x^{\mu}=(t,\boldsymbol{x})}$$
- The _generating functional_ is then:
$$Z[J]\propto \int  \mathcal{D}\phi\,\exp\left[ \frac{i}{\hbar} \int  d^4x\,\Big(\mathcal{L}(\phi)+J(x)\phi(x)\Big) \right] $$

- Denote the _vacuum_ in 4 dimensions as $\ket{\Omega}$

- The _time-ordered correlation function_:
$$\begin{align}
\langle T\{\phi(x_{1})\phi(x_{2})\dots \phi(x_{n})\} \rangle :&=\frac{\braket{ \Omega|T\{\phi(x_{1})\phi(x_{2})\dots \phi(x_{n}) | \Omega }}{\braket{ \Omega | \Omega } }  \\
&=\left[ \frac{(-i\hbar)^{n}}{Z[J]} \frac{\delta^{n}Z[J]}{\delta J(x_{1})\delta J(x_{2})\dots\delta J(x_{n})} \right]_{J=0} 
\end{align}$$
- The _partition function_ is $Z[0]=\braket{ \Omega  |\Omega  }$
- For a _vacuum-to-vacuum_ transition, one can _define_ the $t\to \pm \infty$ _limits_ of any initial or final state to be _vacuums_
$$\ket{\Omega}=\lim_{ t \to -\infty } \ket{\text{in},t}\qquad \bra{\Omega}=\lim_{ t \to +\infty }  \bra{\text{out},t}   $$

## Free Theory
- Set $\hbar=1$
- The [[QFT#Free theory of quantum fields|Klein-Gordon Lagrangian]]:
$$\mathcal{L}=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2}$$
- The corresponding generating function, using _integration by parts_
$$Z[J]=\mathcal{N}\int  \mathcal{D}\phi \,\exp\left[-i \int  d^4x \left( \frac{1}{2}\phi\,\partial^{2}\phi+\frac{1}{2}m^{2}\phi^{2}-J\phi \right)\right]$$

### The generating functional
- This can be evaluated using the _Greens function_ for $\partial^{2}+m^{2}$, also known as the [[QFT#The Feynman propagator|Feynman propagator]]
$$\displaylines{D_{F}(x-y)=\int  \frac{d^{4}p}{(2\pi)^{4}} \frac{i}{p^{2}-m^{2}+i\epsilon}e^{-i\cdotp(x-y)}  \\ (\Box_{x}+m^{2}-i\epsilon)D_{F}(x-y)=-i\delta^{4}(x-y)}$$
- It gives the _time-ordered product_ of observables in the _free theory_

- Introduce a _linear shift_ in $\phi$
$$\tilde{\phi}(x):=\phi(x)-i \int  d^4y\,D_{F}(x-y)J(y) $$
- The _exponent_ is then a _combination_ of a _functional of_ $\phi$ and a simple _scalar_
$$\begin{align}
&\int  d^4x\Big(\mathcal{L}(\phi)+J(x)\phi(x)\Big) \\
=&-\frac{1}{2}\int  d^4x \,\tilde{\phi}(x)(\Box+m^{2})\tilde{\phi}(x)+\frac{i}{2}\int  d^4x\,d^{4}y\,J(x)D_{F}(x-y)J(y)  
\end{align}$$
- Then by _integrating over_ $\phi$:
$$Z[J]\propto Z_{0}[0]\exp\left( -\frac{1}{2}\int  d^4x\,d^{4}y\,J(x)D_{F}(x-y)J(y)  \right) $$
- With the _normalisation_ $Z_{0}[0]=1$
$$Z_{0}[J]=\exp\left( -\frac{1}{2}\int  d^4x\,d^{4}y\,J(x)D_{F}(x-y)J(y)  \right) $$
- Compared to the [[#Free case|zero dimensional theory]], $J$ still appears _quadratically_

### Correlation functions
- A _two-point correlation_ then regains the _Feynman propagator_:
$$\begin{align}
\langle \phi(x_{1})\phi(x_{2}) \rangle  &= \frac{1}{Z_{\lambda}[0]} \left( -i \frac{\delta}{\delta J(x_{1})} \right)\left( -i \frac{\delta}{\delta J(x_{2})} \right)Z_{\lambda}[J]\Bigg|_{J=0}  \\
&=- \frac{\delta^{2}}{\delta J(x_{1})\delta J(x_{2})} \exp\left( -\frac{1}{2}\int  d^4x\,d^{4}y\,J(x)D_{F}(x-y)J(y)  \right)\Bigg|_{J=0} \\
&=\frac{\delta}{\delta J(x_{1})}\int  d^4y \,D_{F}(x_{2}-y)J(y)\,Z[J]\Bigg|_{J=0}  \\
&=D_{F}(x_{1}-x_{2})
\end{align}$$
- The _four-point correlation_ can be calculated similarly:
$$\begin{align}
\langle \phi(x_{1})\phi(x_{2})\phi(x_{3})\phi(x_{4}) \rangle&=D_{F}(x_{1}-x_{2})D_{F}(x_{3}-x_{4})+D_{F}(x_{1}-x_{3})D_{F}(x_{2}-x_{4}) \\
&+D_{F}(x_{1}-x_{4})D_{F}(x_{2}-x_{3}) 
\end{align}$$

### Yukawa potential
- Let the action have some _source term_:
$$\displaylines{S_{J}[\phi]=\frac{1}{2}\int  d^4x\,[(\partial \phi)^{2}-m^{2}\phi^{2}+2J\phi] \\ (\Box+m^{2})\phi=J}$$
- The _vacuum_ with the source present is $\ket{0}_{J}$
- The _transition amplitude_ with some time $T$ is:
$$\frac{_{J}\braket{ 0|e^{-iHT} |0  }_{J}}{\braket{ 0 |0  } } =\frac{1}{Z[0]} \int_{\phi_{J}(0)}^{\phi_{J}(T)} \mathcal{D}\phi e^{iS[\phi]}=\exp\left( -\frac{1}{2}\int  d^4x\,d^{4}y\,J(x)D_{F}(x-y)J(y)  \right) $$
- Assume the source is _point-like_:
$$J_{1}(x)=q_{1}\delta^{3}(\boldsymbol{x}-\boldsymbol{x}_{1})$$
- $\phi$ encodes some _current_ between the point-like sources $J_{1}$ and $J_{2}$
	- Simplification of [[QFT#Interactions Yukawa theory|Yukawa Theory]]

- The transition amplitude can be written as:
$$\exp(-iET)$$
- $E$ is some _measure of interaction energy_ between the sources:
$$\exp(-iET)\propto \exp\left( -\frac{q_{1}q_{2}}{2}\int  dt_{1}\,dt_{2}\,D_{F}(\boldsymbol{x}_{1}-\boldsymbol{x}_{2})  \right)$$
- Using the expression for the Feynman propagator:
$$E=\frac{q_{1}q_{2}}{iT}\int_{0}^{T}  dt_{1} \,dt_{2}\int  \frac{d^4k}{(2\pi)^{4}} \frac{i}{k^{2}-m^{2}+i\epsilon}e^{ik(x_{1}-x_{2})} $$
- One of the timelike integrals gives $k_{0}=0$, giving:
$$E=-\frac{q_{1}q_{2}}{T}\int_{0}^{T}  dt_{1}\int  \frac{d^3k}{(2\pi)^{3}} \frac{e^{i\boldsymbol{k}\cdot(\boldsymbol{x}_{1}-\boldsymbol{x}_{2})}}{\boldsymbol{k}^{2}+m^{2}-i\epsilon}  $$
- From contour integration, with $r=|\boldsymbol{x}_{1}-\boldsymbol{x}_{2}|$, this gives the _Yukawa potential_
$$E=-\frac{q_{1}q_{2}}{4\pi r}e^{-mr}$$
- For a _massless scalar field_, this is the _Coulomb potential_

## Quartic potential
- With a _quartic interaction term_:
$$\mathcal{L}=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2}-\frac{\lambda}{4!}\phi^{4}$$
- The generating functional is now:
$$Z_{\lambda}[J]=\frac{1}{Z_{0}[0]}\int  \mathcal{D}\phi \exp\left( i \int  d^4x\left( \frac{1}{2}\phi(-\partial^{2}-m^{2})\phi-\frac{\lambda}{4!}\phi^{4}+J(x)\phi(x) \right)  \right)$$
- Expand as a _power series_ in $\lambda$, then exchange summation and functional integration, similar to the [[#Interacting theory|zeroth dimensional case]]
$$Z_{\lambda}[J]=\sum_{k=0}^{\infty} \frac{1}{k!}\left( -\frac{i\lambda}{4!} \right)^{k}\left( \int  d^4y \frac{\delta^{4}}{\delta J(y)^{4}}  \right)^{k}Z_{0}[J]$$
- Writing out in full:
$$Z_{\lambda}[J]=\sum_{k=0}^{\infty} \frac{1}{k!}\left( -\frac{i\lambda}{4!} \right)^{k}\left( \int  dx_{1}\dots dx_{k} \frac{\delta^{4}}{\delta J(x_{1})^{4}}\dots\frac{\delta^{4}}{\delta J(x_{k})^{4}}  \right)Z_{0}[J]$$
- The _partition function_ is $Z_{\lambda}[0]=\braket{ \Omega |\Omega  }$
- The time-ordered correlation is then:
$$\begin{align}
\langle \phi(x_{1})\dots \phi(x_{n}) \rangle&=\frac{\braket{ \Omega |T\{\phi(x_{1})\dots \phi(x_{n})\}|\Omega  }}{\braket{ \Omega |\Omega  } } \\
&=\left[ \frac{1}{Z_{\lambda}[J]} \left( -i \frac{\delta}{\delta J(x_{1})} \right)\dots\left( -i \frac{\delta}{\delta J(x_{n})} \right)Z_{\lambda}[J] \right]_{J=0}
\end{align}$$
### Explicit form of generating functional
- The generating functional:
$$Z_{\lambda}[J]=Z_{0}[J]-\frac{i\lambda}{4!}\int  d^4y \frac{\delta^{4}}{\delta J(y)^{4}} Z_{0}[J]$$
- Calculating the functional derivatives gives the $\lambda^{1}$ term as:
$$\begin{align}
-\frac{i\lambda}{4!}\int  d^4y\bigg\{3(&D_{F}(0))^{2}+ \int  \prod_{i=1}^{4}d^{4}z_{i}D_{F}(y-z_{i})J(z_{i}) \\
+6&D_{F}(0)\int  \prod_{i=1}^{2}d^{4}z_{i} D_{F}(y-z_{i})J(z_{i}) \bigg\} Z_{0}[J]
\end{align}$$
- Here, the Feynman propagator:
$$D_{F}(0)=\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}-m^{2}+i\epsilon} $$
- It _diverges quadratically_ when integrated over _all momenta_

- The terms above can be written as:
![[phi4 four dimensions correction.png]]

- The _partition function_ can then be written to the first order as:
$$Z_{\lambda}[0]=1+ \frac{1}{2^{3}}\left(-i\lambda \int  d^4y \right)(D_{F}(0))^{2}$$
- Aside from an infinity in $D_{F}(0)$, one also integrates some _large volume of spacetime_

### Two-point correlation and the mass shift
- The only _connected_ $\lambda^{1}$ contribution to $\braket{ \phi(x_{1})\phi(x_{2})  }$ comes from the $\sim J(z_{1})J(z_{2})$ term
	- The disconnected contribution is cancelled out in normalisation
- The contribution:
$$\begin{align}
&(-i)^{2} \frac{\delta^{2}}{\delta J(x_{1})\delta J(x_{2})}\left( -\frac{i\lambda}{4!} (-6)D_{F}(0)\int  d^4y \int  \prod_{i=1}^{2}d^{4}z_{i} D_{F}(y-z_{i})J(z_{i}) \right) \Bigg|_{J=0}\\ =&-\frac{i\lambda}{2}D_{F}(0)\int  d^4y\, D_{F}(y-x_{1}) D_{F}(y-x_{2})
\end{align}$$
- There is a $1/2$ _symmetry factor_

- Define:
$$\Pi:= \frac{\lambda}{2}D_{F}(0)$$
- Evaluating the $\lambda^{1}$ contribution using the explicit form of $D_{F}$ then gives:
$$\braket{ \phi(x_{1}) \phi(x_{2})} =D_{F}(x_{1}-x_{2})+i\Pi \int  \frac{d^4p}{(2\pi)^{4}} \frac{e^{-ip\cdot(x_{1}-x_{2})}}{(p^{2}-m^{2}+i\epsilon)^{2}} $$
- This can be written as:
$$\begin{align}
\braket{ \phi_{1}\phi_{2} } &=\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}-m^{2}+i\epsilon} e^{-ip\cdot(x_{1}-x_{2})} \left( 1+ \frac{\Pi_{1}}{p^{2}-m^{2}+i\epsilon} \right) \\ &=\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}-m^{2}+i\epsilon} e^{-ip\cdot(x_{1}-x_{2})} \left( 1- \frac{\Pi_{1}}{p^{2}-m^{2}+i\epsilon} \right)^{-1} 
\end{align}$$
- Therefore, up to $\lambda^{1}$:
$$\langle \phi_{1}\phi_{2} \rangle =\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}-m^{2}-\Pi+i\epsilon}e^{-ip\cdot(x_{1}-x_{2})}+\mathcal{O}(\lambda^{2})  $$
- The _one-loop contribution_ can be accounted for by a _mass shift_:
$$m^{2}\to m^{2}+\Pi$$
- Qualitatively, this mass shift is _present for all orders in perturbation theory_
	- Effectively, the classical parameter $m$ used to define the quantum field theory is not observable

### Four-point correlation
- $\lambda^{1}$ contribution to 4-point function:
$$(-i)^{4} \frac{\delta^{4}}{\delta J(x_{1})\delta J(x_{2})\delta J(x_{3})\delta J(x_{4})} \int  d^{4}y \left( -\frac{i\lambda}{4!} \right) \int  \prod_{i=1}^{4}d^{4}z_{i}D_{F}(y-z_{i})J(z_{i}) $$
- Evaluating gives:
$$-i\lambda \int  d^4y \int  \prod_{i=1}^{4} \frac{d^{4}p_{i}}{(2\pi)^{4}} \frac{1}{p_{i}^{2}-m^{2}+i\epsilon}\exp\left( -i \sum_{i=1}^{4}p_{i}\cdot(y-x_{i}) \right)   $$
- Evaluating the $y$ integral gives a _momentum conservation delta function_:
$$-i\lambda (2\pi)^{4}\delta^{4}\left( \sum_{i=1}^{4}p_{i} \right)\int  \prod_{i=1}^{4} $$
- This is a _Fourier transform_ of the _momentum space propagator_:
$$\tilde{D}_{F}(p)=\frac{i}{p^{2}-m^{2}+i\epsilon}$$
### $\phi^4$ Feynman rules in spacetime
- For each _line_, there is a propagator $D_{F}(x-y)$
- Each vertex gives a factor of $-i\lambda$
- _Divide_ by some _symmetry factor_
- _Integrate_ over any _unconstrained points_

### One-loop correction to the four point function

![[One loop four point function.png]]

### Momentum space $\phi^4$ Feynman rules
- Each line, there is the _momentum space Feynman propagator_ $\tilde{D}_{F}(x-y)$
- Each vertex gives a factor of $-i\lambda$
- For each loop, integrate over the _unconstrained momentum_
$$\int  \frac{d^4q}{(2\pi)^{4}} $$
- Impose _momentum conservation at each vertex_ and overall conservation
$$(2\pi)^{4} \delta^{4}\left( \sum_{i}p_{i} \right)$$
- Divide by the _symmetry factor_

# Effective Action
- $Z_{\lambda}[J]$ generates correlation functions $\langle \phi^{n} \rangle$, represented by _Feynman diagrams_
- _Normalisation_ removes _vacuum bubbles_ from the Feynman diagrams

- There are still _redundant, disconnected diagrams_ generated, which _do not encode interactions_
	- The number of disconnected diagrams _increases_ as $n$ increases

- Example: the four-point function (normalised, no vacuum bubbles)
![[4 point function diagrams.png]]
$$\langle \phi^{4} \rangle=\langle \phi^{4} \rangle_\text{conn}+(\langle \phi^{2} \rangle\langle \phi^{2} \rangle+\{\text{disconnected} \} )  $$

- The _Wilsonian effective action_ $W[J]$ will give only $\langle \phi^{n} \rangle_\text{conn}$
- One desires:
$$W[J]\sim \sum_{n=0}^{\infty} \frac{1}{n!} \langle \phi^{n} \rangle_\text{conn}\,J^{n} $$
## Wilsonian effective action in zero dimensions
- Work in _zero dimensions_

- The Wilsonian effective action is:
$$Z_{\lambda}[J]=N\int  \mathcal{D}\phi\,e^{-S[\phi]-J\phi} =\exp(-W[J])$$
- The correlation function is then:
$$\langle \phi^{n} \rangle_\text{conn}=-\frac{\partial^{n}W}{\partial J^{n}}\Bigg|_{J=0} $$
### Motivation
- In the case of _multiple interacting fields_:
$$Z[J]=\int  \mathcal{D}\phi\,\mathcal{D}\chi\,e^{-S[\phi,\chi]-J\phi-K\chi} $$
- The _effect_ of the $\chi$ field on $\phi$ is given by setting $K=0$ (to get rid of irrelevant $\chi$ correlations) and integrating over $\chi$
$$\int  \mathcal{D}\phi\,\mathcal{D}\chi \,e^{-S[\phi,\chi]-J\phi}=\int  \mathcal{D}\phi \,e^{-S_\text{eff}[\phi]-J\phi}$$
- One gets an _effective action_ by integrating over $\chi$

### Example: 4-point function
- For example, to generate the 4-point function:
$$-W''''=\frac{Z''''}{Z}-4\dots$$
- _Normalisation_ is _built in_ as the factor is always _cancelled out_

- Example: in $\phi^{4}$ theory, setting $J=0$, the _one-point_ and _three-point_ functions disappear, giving:
$$\langle \phi^{4} \rangle_\text{conn}=\langle \phi^{4} \rangle-3\langle \phi^{2} \rangle^{2}   $$
- The _disconnected diagram_ is _subtracted_

## One-particle irreducibles (1PI)
- A _connected diagram_: all lines in one piece
- An _amputated diagram_: all external lines removed

- A _one-particle irreducible diagram_ (1PI) is one that _cannot be split into two diagrams_ by cutting an _internal line_ ("cutting" one particle)

- A non-1PI diagram cut into two 1PIs:
![[1PI diagram cut.png]]

## Quantum effective action
- Analogue of the classical action, but encoding quantum mechanics

- Recall the _Wilsonian effective action_:
$$Z(J)=\int  d\phi \exp\left[ -\frac{1}{\hbar}(S(\phi)+J\phi) \right]\qquad W(J)= -\hbar \ln(Z(J))$$
### Definition
- Consider the _differential_ of $W[J]$, where $\Phi$ is defined as the _mean field_
	- The mean field: some _one point correlation_ with nonzero source
$$dW=\frac{\partial W}{\partial J}dJ=\Phi dJ$$
- The _Legendre transform_ $E$, a function of $\Phi$
$$E=\Phi J-W(J)\implies dE=Jd\Phi$$
- The _quantum effective action_:
$$\Gamma(\Phi)=W(J)-J\Phi\qquad \Phi=\frac{\partial W(J)}{\partial J}$$
- Assuming $\Gamma(\Phi)$ can be written as a _power series_:
$$\Gamma(\Phi)=\sum_{n=0}^{\infty} \frac{1}{n!}\Gamma_{n}\Phi^{n}\qquad \Gamma_{n}=\frac{\partial^{n}\Gamma}{\partial \Phi^{n}}$$
- As seen in the section below, $\Gamma_{n}$ gives _vertices_
### Diagrammatic interpretation
- Consider a _quantum effective analogue_ of the _Wilsonian action_, using _parameter_ $g$
$$\exp\left( -\frac{1}{g}W_{\Gamma}(J) \right)=\int  d\phi\,\exp\left( -\frac{1}{g}(\Gamma(\phi)+J\phi) \right) $$
- $\phi$ is an _unconstrained field_, not necessarily satisfying $\partial W/\partial J=\Phi$

- $W_{\Gamma}(J)$ can be written as an _expansion in $g$ loops_:
	- $g$: an _analogue_ to $\hbar$ in this case
$$W_{\Gamma}(J)=\sum_{l=0}^{\infty}g^{l}W_{\Gamma}^{(l)}(J)$$
- In the $g\to 0$ limit, $W_{\Gamma}^{(0)}(J)$ is the only part that contributes, giving _tree level diagrams_
	- _All relevant quantum information $\sim \hbar^{n}$ are contained_ within this contribution

- The path integral is then _dominated_ by the _extrema_ of $\Gamma(\phi)+J\phi$, defining the value of $\phi$ at the extremum to be the _mean field_ $\Phi$
$$\left[ \frac{\partial\Gamma}{\partial \phi }+J \right]_{\phi=\Phi}=0$$
- This can be written as:
$$\exp(-W_{\Gamma}^{(0)}(J))\approx \exp[-(\Gamma(\Phi)+J\Phi)]$$
- $\Gamma(\Phi)+J\Phi$ is the _Wilsonian effective action_, with $\Phi$ being the _mean field_

- The _fully quantum, connected correlation functions_ are given by the _tree level diagrams_ generated by $\Gamma(\phi)$ using _Feynman rules_
- $\Gamma_{n}$ can then be interpreted as $n-$_point, amputated, 1PIs_, which _compose_ the tree-level diagrams
	- Interpretation: draw _analogues_ to the _classical action_
	- $\Gamma_{2}$ gives a _propagator_ which is _inversely proportional_ to the _mass coefficient_ $\alpha$ in the _kinetic term_ of the action
	- $\Gamma_{3}$ gives a _3-point vertex_, and so on

## Quantum effective action in 0-dimensional $\phi^4$ theory
- The _generating functional_ in the [[#Interacting theory|zero-dimensional interacting theory]]
$$\begin{align}
Z_{\lambda}(J)&=N \int  d\phi\,\exp\left( -\frac{1}{2}\alpha \phi^{2} -\frac{\lambda}{4!}\phi^{4}+J\phi\right) \\ &=\left( 1-\frac{\hbar^{2}\lambda}{4!}\left( \frac{J^{4}}{\alpha^{4}\hbar^{4}}+\frac{6J^{2}}{\alpha^{3}\hbar^{3}}+\frac{3}{\alpha^{2}\hbar^{2}} \right)+\dots \right)\exp\left( \frac{J^{2}}{2\alpha^{2}\hbar} \right)
\end{align}$$
- The _Wilsonian effective action_, to first order in $\lambda$:
$$W(J)=-\hbar \ln [Z_{\lambda}(J)]=-\frac{J^{2}}{2\alpha}+\frac{\lambda}{4!} \frac{J^{4}}{\alpha^{4}}+\frac{\lambda \hbar}{4} \frac{J^{2}}{\alpha^{3}}+\frac{\hbar^{2}\lambda}{8\alpha^2}+\dots$$
- The _mean field_ is then:
$$\begin{align}
\Phi=\frac{\partial W}{\partial J}&=-\frac{J}{\alpha}+\frac{\lambda}{3!} \frac{J^{3}}{\alpha^{4}}+\frac{\lambda \hbar}{2} \frac{J}{\alpha^{3}}+\dots \\
&=-\frac{J}{\alpha}\left( 1-\frac{\lambda \hbar}{2\alpha^{2}} \right)+\frac{\lambda}{3!}
\frac{J^{3}}{\alpha^{4}}\end{align}$$
- There is _only one quantum correction_
- One also gets that for $J=0$, the _mean field vanishes_, as it is the _connected one-point function_, as expected in $\phi^{4}$ theory

- This can then be _iteratively inverted_
$$\begin{align}
J(\Phi)&=-\alpha\left( 1-\frac{\lambda \hbar}{2\alpha^{2}} \right)^{-1}\left( \Phi-\frac{J^{3}}{3!} \frac{\lambda}{\alpha^{4}} \right)+\dots \\ &=-\alpha\left( 1+\frac{\lambda \hbar}{2\alpha^{2}} \right)\left( \Phi-\frac{J^{3}}{3!} \frac{\lambda}{\alpha^{4}} \right)+\dots \\ &=-\alpha \Phi+\frac{\lambda}{3!} \frac{J^{3}}{\alpha^{3}} -\frac{\lambda \hbar}{2\alpha}\Phi+\dots \\ &=-\alpha \Phi-\frac{\lambda}{3!}\Phi^{3}-\frac{\hbar\lambda}{2\alpha}\Phi
+\dots\end{align}$$
- The Wilsonian effective action in terms of the mean field:
$$W(\Phi)=\frac{\hbar^{2}\lambda}{8\alpha^{2}}-\frac{1}{2}\alpha \Phi^{2}+\left( \frac{1}{4!}-\frac{1}{3!} \right)\lambda \Phi^{4}-\frac{\lambda \hbar}{4\alpha}\Phi^{2}+\dots$$
- Finally, the _quantum effective action_:
$$\Gamma(\Phi)=W(\Phi)-J(\Phi)\Phi=\frac{\lambda \hbar^{2}}{8\alpha^{2}}+\frac{1}{2}\left( \alpha-\frac{\hbar\lambda}{2\alpha} \right)\Phi^{2}+\frac{\lambda}{4!}\Phi^{4}$$
- This _resembles the classical action_, but with _quantum corrections_
	- The classical action $S(\Phi)$ is regained as $\hbar\to 0$
	- It _does not break_ the $\Phi\to -\Phi$ symmetry

- One can then use more _Feynman rules_ to generate diagrams

- Each _looped correction_ has a factor of $\hbar/\alpha$
- There is a _quantum vacuum shift_, coming from a _two-loop vacuum diagram_
- The $\Phi^{4}$ term has _no correction at order_ $\lambda$ as the first corresponding diagram has $\lambda^{2}$
- The _propagator_ has a _one-loop correction_:
$$W_{2}=\left( \alpha+\frac{\hbar\lambda}{2\alpha} \right)^{-1}=\frac{1}{\alpha}-\frac{\hbar\lambda}{2\alpha^{3}}$$

## Summary of functions
- The _generating functional_, which _generates all possible diagrams_
$$Z_{\lambda}[J]=\int  \mathcal{D}\phi\,\exp\left( -S[\phi]+J\phi \right) $$
- The _partition function_, which _generates vacuum bubble diagrams_
$$Z_{\lambda}[0]$$
- The _Wilsonian effective action_, which generates _connected diagrams_
$$W_{\lambda}[J]=-\hbar \ln(Z[J])$$
- The _quantum effective action_, which generates _1PI diagrams_
$$\Gamma_{\lambda}[\Phi]=W_{\lambda}[\Phi]-J\Phi$$
## Quantum effective action in 4 dimensions
- In _4 dimensions_, the mean field is:
$$\Phi[J]=\frac{\delta W[J]}{\delta J}\sim \langle \phi \rangle_{J} $$
- The quantum effective action is then:
$$\Gamma[\Phi]=W[\Phi]-\int  d^4x\,J(x){\Phi(x)} $$
### Correspondence to classical action
- Consider the derivative of the quantum effective action:
$$\frac{\delta\Gamma[\Phi]}{\delta \Phi(x)}=\frac{\delta}{\delta \Phi(x)}\left(W[J]-\int  d^4y\,J(y)\Phi(y) \right)$$
- Using the definition of $\Phi$ and the functional chain rule, this becomes:
$$\begin{align}
\frac{\delta \Gamma [\Phi]}{\delta \Phi(x)}&=\int  d^4y \left(\Phi(y)\frac{\delta J(y)}{\delta \Phi(x)}- \frac{\delta J(y)}{\delta \Phi(x)}\Phi(y)\right)-J(x) \\ &=-J(x)
\end{align}$$
- This mirrors the _classical Euler-Lagrange equation_
- For $J(x)=0$:
$$\displaylines{\Phi(x)=\phi _\text{cl} \\ \frac{\delta\Gamma [\Phi]}{\delta \Phi(x)}\Bigg|_{\Phi=\phi _\text{cl}}=0}$$
### $\Gamma_2$ and the propagator
- The functional chain rule gives:
$$\frac{\delta}{\delta J(x)}=\int  d^4y\, \frac{\delta \Phi(y)}{\delta J(x)} \frac{\delta}{\delta \Phi(y)}=\int  d^4y\,\frac{\delta^{2}W[J]}{\delta J(x)\delta J(y)} \frac{\delta}{\delta \Phi(y)} $$
- From the above:
$$\frac{\delta}{\delta J(y)} \left( \frac{\delta\Gamma[\Phi]}{\delta \Phi(x)} \right)=-\delta^{4}(x-y)$$
- Expanding this:
$$\int  d^4z\, \frac{\delta^{2}W[J]}{\delta J(z)\delta J(y)}  \frac{\delta^{2}\Gamma[\Phi]}{\delta \Phi(z)\delta \Phi(x)}=-\delta^{4}(x-y)$$
- To shorten:
$$\int  d^4z\,W_{2}(z,y)\,\Gamma_{2}(z,x) =-\delta^{4}(x-y)$$
- This can also be written as:
	- Similar relation holds in the _zeroth dimensional case_
$$W_{2}\Gamma_{2}=-1$$

- Taking the _Feynman propagator_ $G_{2}(x-y)$:
$$-iW_{2}(y,z)=G_{2}(y-z)=\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}-M^{2}+i\epsilon}\exp[-ip(x-y)] $$
- Here, $M^{2}$ is the [[#Two-point correlation and the mass shift|shifted mass]] $m^{2}+\Pi_{1}$

- Substituting the _Fourier transform_ of $\Gamma_{2}$:
$$i \int  d^4z \frac{d^{4}p \,d^{4}q}{(2\pi)^{8}} \frac{\tilde{\Gamma}(q)}{p^{2}-M^{2}+i\epsilon} \exp[-ip(y-z)-iq(z-x)]=-\delta^{4}(x-y) $$
- Performing the integration:
$$\int  \frac{d^{4}p}{(2\pi)^{4}} \frac{\tilde{\Gamma}(p)}{p^{2}-M^{2}+i\epsilon}\exp[-ip(y-x)]=\delta^{4}(x-y) $$
- This gives:
$$\tilde{\Gamma}(p)=p^{2}-M^{2}+i\epsilon$$
- $\Gamma$ is the _inverse propagator_

### $\Gamma_3$ and higher order functions
- Functional differentiation of the above w.r.t. $w$
$$\frac{\delta}{\delta J(w)}\int  d^4z\, \frac{\delta^{2}W[J]}{\delta J(z)\delta J(y)}  \frac{\delta^{2}\Gamma[\Phi]}{\delta \Phi(z)\delta \Phi(x)}=0$$
- From the chain rule again (verify):
$$\int  d^4z\, W_{3}(w,y,z)\Gamma_{2}(z,x)=-\int  d^4\sigma \int  d^4z\,W_{2}(y,z)W_{2}(\sigma,w)\Gamma_{3}(z,x,\sigma)  $$
- Multiplying through by $W_{2}(x,\rho)$ and integrating by $x$, using the relation for $W_{2}\Gamma_{2}$:
$$W_{3}(x,y,z)=\int  d^4w_{1}\,d^{4}w_{2}\,d^{4}w_{3} \,W_{2}(x,w_{1})W_{2}(y,w_{2})W_{2}(z,w_{3})\Gamma_{3}(w_{1},w_{2},w_{3}) $$
- Or alternatively:
$$W_{3}=W_{2}^{3}\Gamma_{3}$$
- _Diagrammatically_, the _connected 3-point function_ is given by a _3-point 1PI_ with _three external legs_
![[3 point function decomposition.png|400]]

- Similarly, one can perform a decomposition on $W_{4}$
![[W4 decomposition.png]]
- These are all statements which _hold for any perturbation_

# Momentum cut-off regularisation
- Feynman diagrams often have _divergent contributions_, such as:
$$D_{F}(0)=\int  d^4p \frac{i}{p^{2}-m^{2}+i\epsilon} $$
- One can put an _upper cutoff in momentum_ to make the integrals _finite_:
$$p<\Lambda$$
- The _physical interpretation_ of the quantities must still make sense in the limit of _cut-off at infinity_
- This is known as _regularisation_

## The two-point correlation function
- A diagrammatic approach to the _connected loop corrections_ in $G_{2}(x,y)$
![[Propagator loop corrections.png|400]]

### 1PI contributions
- Consider the _sum of amputated 2-point 1PIs_ contributing to this:
![[2-point 1PIs.png|400]]
- In _momentum space_, the 2-point Greens function written _in terms of external propagators with the 1PIs_
$$\begin{align}
\tilde{G}_{2}(p)&=\frac{i}{p^{2}-m^{2}+i\epsilon}+\frac{i}{p^{2}-m^{2}+i\epsilon} \Pi \frac{i}{p^{2}-m^{2}+i\epsilon}  \\
&+ \frac{i}{p^{2}-m^{2}+i\epsilon} \Pi \frac{i}{p^{2}-m^{2}+i\epsilon} \Pi \frac{i}{p^{2}-m^{2}+i\epsilon}+\dots
\end{align}$$
![[Full Greens function with 1PIs.png|400]]

- This can be written as a _geometric progression_, which can be written as:
	- Technically, should only converge for $i\Pi/(p^{2}-m^{2}+i\epsilon)<1$
$$\tilde{G}_{2}(p)= \frac{i}{p^{2}-m^{2}-\tilde{\Pi}(p^{2})+i\epsilon}$$
- Formally, _all quantum effects_ can be inserted into a _mass shift_
$$\tilde{G}_{2}(p)=\frac{i}{p^{2}-M^{2}+i\epsilon } \qquad M^{2}=m^{2}+\Pi$$
- However, $\Pi$ is still _formally divergent_

## Wick rotation and Euclidean QFT
- The _analytic continuation_ of $G_{n}(\phi_{1}\dots \phi_{n})$ to _complex spacetime_

- Using _imaginary time_, one goes to a _Euclidean spacetime_
	- There are well-defined criteria for when Euclidean and Minkowski spacetime field theories are _isomorphic_
$$t\to \tau=it\implies ds^{2}=-(d\tau^{2}+dx^{2})$$
- Once Wick rotated, the Feynman propagator becomes:
$$D_{F}(x-y)=\int  \frac{d^4p}{(2\pi)^{4}} \frac{1}{p^{2}+m^{2}} \exp[ip(x-y)] $$
- The contour is _rotated_ such that the _poles_ are now on the _imaginary_ axis

### Euclidean Feynman rules in $\phi^4$ theory
- The action is still:
$$S_{E}[\phi]=\int  d^4x\,\left[ \frac{1}{2}\partial_{\mu}\phi\partial^{\mu}\phi+\frac{1}{2}m^{2}\phi^{2}+\frac{\lambda}{4!}\phi^{4} \right] $$
- The _new momentum Feynman rules_:
	- For each line, $\tilde{D}_{F}(p)=(p^{2}+m^{2})^{-1}$
	- For each vertex, there is a factor of $-\lambda$
	- Integrate over the unconstrained momenta
	- Divide by the _symmetry factor_
	- Impose _momentum conservation_ $$(2\pi)^{4}\delta^{4}\left( \sum_{i}p_{i} \right)$$
### A one-loop correction
- For example, the _one-loop correction_ to the propagator:
$$-\frac{\lambda}{2}\int  \frac{d^4k}{(2\pi)^{4}} \frac{1}{k^{2}+m^{2}} $$
- Denoting an _angular measure_ in 4D as $d\Omega_{4}$:
$$d^{4}k=k^{3}\,dk\,d\Omega_{4}$$
- Also _regularise_ by adding a _higher momentum cutoff_:
$$0<k^{2}<\Lambda^{2}$$
- From below: 
$$\int  d\Omega_{4}=S_{4}=2\pi^{2} $$
- Then consider the integral:
$$\int_{0}^{\Lambda}  dk \frac{k^{3}}{k^{2}+m^{2}} $$
- Doing the integral with substitution $u=k^{2}/m^{2}$:
$$\int_{0}^{\Lambda}  dk \frac{k^{3}}{k^{2}+m^{2}} =\frac{m^{2}}{2}\left[ \frac{\Lambda^{2}}{m^{2}}-\ln\left( 1+ \frac{\Lambda^{2}}{m^{2}} \right) \right]$$
- The one-loop correction is then:
$$\Pi=-\frac{\lambda}{32\pi^{2}}\left( \Lambda^{2}-m^{2}\ln\left( 1+\frac{\Lambda^{2}}{m^{2}} \right) \right)$$

- The _vertex_(inverse propagator) given by the [[#$ Gamma_2$ and the propagator|quantum effective action]]:
$$\Gamma_{2}(p)=p^{2}+m^{2}-\Pi$$
#### Diversion: area of a $d-$dimensional sphere
- In $d$ dimensions, for a function depending only on _radius_, one can write in terms of the _area of a sphere in $d$ dimensions_ $S_{d}$
$$\int  f(r)\,d^{d}r=S_{d}\int  f(r)r^{d-1}\,dr  $$
- Considering the _Gaussian integral_:
$$(\sqrt{ \pi })^{d}=\int_{\mathbb{R}^{d}}dx_{1}\dots dx_{d}\,e^{-(x_{1}^{2}+\dots x_{d}^{2})}=S_{d}\int  dr\,r^{d-1}e^{-r^{2}}  $$
- The _Gamma function_:
	- $\gamma$ is the _Euler-Mascheroni constant_
$$\displaylines{\Gamma(z)=\int_{0}^{\infty}  dt\,t^{z-1}e^{-t} \\ \Gamma(n)=(n-1)! \qquad \Gamma(z)=\frac{1}{z}-\gamma+\dots}$$
- Making the substitution $u=r^{2}$:
$$S_{d}=\frac{2\pi^{d/2}}{\Gamma(d/2)}$$
- From this, the area of a _4D sphere_ $S_{4}$ is $2\pi^{2}$

### 4-point divergence at one-loop
![[4 point one loop corrections.png|500]]
- For simplicity, only calculate the _loop integrals_ where $p_{i}=0$
- In this case, all 3 permutations have the same contribution:
$$\int_{\mathcal{B}_{\Lambda}}  \frac{d^4k}{(2\pi)^{4}}  \frac{1}{(k^{2}+m^{2})^{2}}$$
- Making the $u=k^{2}/m^{2}$ substitution again, the contribution from one loop integral:
$$\frac{\lambda^{2}}{32\pi^{2}}\left[ \ln\left( 1+\frac{\Lambda^{2}}{m^{2}} \right)- \frac{\Lambda^{2}}{\Lambda^{2}+m^{2}} \right]$$
- Therefore, the 4-point correlation for $p_{i}=0$:
$$-\lambda+\frac{3\lambda^{2}}{32\pi^{2}}\left[ \ln\left( 1+\frac{\Lambda^{2}}{m^{2}} \right)- \frac{\Lambda^{2}}{\Lambda^{2}+m^{2}} \right]$$
- From this, the contribution from the [[#$ Gamma_3$ and higher order functions|quantum effective action]] for $p_{i}=0$:
$$\Gamma_{4}(0,0,0,0)=\lambda-\frac{3\lambda^{2}}{32\pi^{2}}\left[ \ln\left( 1+\frac{\Lambda^{2}}{m^{2}} \right)- \frac{\Lambda^{2}}{\Lambda^{2}+m^{2}} \right]$$