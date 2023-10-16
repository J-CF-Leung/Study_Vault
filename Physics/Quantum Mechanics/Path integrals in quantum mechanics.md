# The propagator
- Consider a position-space wave function at time $t$, evolved from $\ket{\Psi(t_0)}$:
$$\begin{aligned}\Psi(x,t)=\braket{x|\Psi(t)}&=\sum_n\braket{x|E_n}\exp\left(-\frac{iE_n(t-t_0)}{\hbar}\right)\braket{E_n|\Psi(t_0)}\\ &= \int \sum_n\braket{x|E_n}\left(-\frac{iE_n(t-t_0)}{\hbar}\right)\braket{E_n|x'}\braket{x'|\Psi(t_0)}\,dx' \\
&=\int K(x,t,x',t_0)\Psi(x',t_0)\,dx'\end{aligned}$$
- The _kernel_ of the integral operator, $K(x,t,x',t_0)$ is known as the _propagator_, similar to the one in wave mechanics
- It dictates the _time-evolution of a position-space wave function given an initial state_
- The propagator is also equal to the _matrix elements of the time-evolution operator_ in the _position basis_:
$$K(x,t,x',t_0)=\sum_n\braket{x|E_n}\exp\left(-\frac{iE_n(t-t_0)}{\hbar}\right)\braket{E_n|x'}=\braket{x|\teo(t,t_0)|x'}$$
## The propagator as a transition amplitude
- It can also be thought of as a _[[Fundamental concepts of quantum mechanics#Transition amplitude|transition amplitude]]_ from the position eigenstate $\ket{x'}$ at time $t_0$ to the eigenstate $\ket{x}$ at time $t$:
$$K(x,t,x',t_0)=\sum_n\bra{x}\exp\left(-i\frac{E_nt}{\hbar}\right)\ket{E_n}\bra{E_n}\exp\left(i\frac{E_nt_0}{\hbar}\right)\ket{x'}=\braket{x,t|x',t_0}$$
	- where both base kets are interpreted as in the [[Fundamental concepts of quantum mechanics#The Schrödinger and Heisenberg pictures|Heisenberg picture]]
- $K(x,t,x',t_0)$ is the probability amplitude for a system to from eigenstate $\ket{x'}$ at $t_0$ to state $\ket{x}$ at time $t$
- The wave function at $(x,t)$ is a weighted total of all amplitudes to arrive at $x$ from every other point in space within interval $t-t_0$
- As position eigenkets at all times are complete, the transition amplitude obeys the composition property:
$$\braket{x'',t''|x,t}=\int\braket{x'',t''|x',t'}\braket{x',t'|x,t}\;dx'$$
- The composition property applies to infinitesimal intervals, allowing one to break down the transition amplitude between two points into:
$$\begin{aligned} \braket{x_N,t_N|x_1,t_1}&=\int dx_{N-1}\int dx_{N-2}\,...\int dx_2 \braket{x_N,t_N|x_{N-1},t_{N-1}} \\ &\;\;\;\;\; \times \braket{x_{N-1},t_{N-1}|x_{N-2},t_{N-2}}\, ...\braket{x_2,t_2|x_1,t_1}\end{aligned}$$
- This is known as _path integration_, as every possible point in space in every infinitesimal time interval (aka. every possible path) is considered

# Feynman's formulation
>[!info] Motivation
>In classical mechanics, only one path, the one with least action, is involved in a particle's motion. However, in quantum mechanics, all possible paths, even the most non-classical, can play a role. Yet, in the $\hbar \rightarrow 0$ limit, classical mechanics must somehow be reproduced.

- Consider the transition amplitude in an infinitesimal time interval $\epsilon=t_n-t_{n-1}$ :
$$\braket{x_n,t_n|x_{n-1},t_{n-1}}=\braket{x_n| \teo(t_n)\,\teo^\dagger(t_{n-1})|x_{n-1}}= \braket{x_n|\exp\left(-\frac{i\Ham\epsilon}{\hbar}\right)|x_{n-1}}$$
- Expanding $\Ham$ into $\hat{p}^2/(2m)+V$, one obtains:
$$\braket{x_n,t_n|x_{n-1},t_{n-1}}=\frac{1}{\sqrt{2i\pi\hbar\epsilon/m}}\exp\left(\frac{i\epsilon}{\hbar}\Lagr\right)$$
	- where $\Lagr$ is the [[Analytical classical mechanics|Lagrangian]]
- An alternative, less rigorous but elegant proof is presented by Dirac using using the Hamilton-Jacobi equations as a classical analogy
- $\epsilon\Lagr$ can be considered to be the _action_ from $t_{n-1}$ to $t_n$, or $S(n,n-1)$
- For the full transition amplitude $\braket{x_N,t_N|x_1,t_1}$:
$$\begin{aligned}\braket{x_N,t_N|x_1,t_1}&=\lim_{N\to\infty}\left(\frac{m}{2\pi i\hbar\epsilon}\right)^{(N-1)/2}\int\,dx_{N-1}\int\,dx_{N-2}\,...\int\,dx_2\\ &\;\;\;\;\times\prod_{n=2}^N\exp{\left(\frac{iS(n,n-1)}{\hbar}\right)}\end{aligned}$$
- This infinite-dimensional integral is known as _Feynman's path integral_, and can be written as:
$$\braket{x_N,t_N|x_1,t_1}=\int_{x_1}^{x_N}\mathcal{D}[x(t)]\exp{\left(i\int_{t_1}^{t_N}\frac{\Lagr(x,\dot{x})}{\hbar}\,dt\right)}$$
- The quantity $iS/\hbar$ can be understood as the "phase" of a particular path, with every possible path giving an equal contribution, but with a different phase
## Reproducing the Schrödinger equation
- Consider the Schrödinger equation over a very small time interval $\epsilon$:
$$\ket{\Psi(\epsilon)}-\ket{\Psi(0)}=-\frac{i\epsilon}{\hbar}\Ham\ket{\Psi(0)}$$
- Project the equation over the $x$ basis, then express $\Psi(x,\epsilon)$ using the propagator
## The classical limit
- Consider summing up two paths with different actions, which interfere with each other
- As $\hbar\to 0$, or (equivalently) as $S>>\hbar$, the difference in action required for 2 paths to destructively interfere gets smaller
- Eventually, all paths except the classical path destructively interfere with each other

# The free particle, with path integrals