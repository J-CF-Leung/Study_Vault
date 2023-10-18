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
$$\hat{H}\ket{n}=E_b\ket{b}$$
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
- Taking the inner product of the equation with $\ket{m^{(0)}}$, _for_ $n\neq m$:
$$E_m^{(0)}\braket{m^{(0)}|n^{(1)}}+\braket{m^{(0)}|\hat{H}^{(1)}|n^{(0)}}=E_n^{(0)}\braket{m^{(0)}|n^{(1)}}$$
- Provided the unperturbed states are _non-degenerate_:
$$\braket{m^{(0)}|n^{(1)}}=\frac{\braket{m^{(0)}|\hat{H}^{(1)}|n^{(0)}}}{E_n^{(0)}-E_m^{(0)}}$$



- Stuff


- This gives the _first order perturbed eigenstate_

## Second-order perturbation theory
- For the $\lambda^2$ terms:

- Taking the inner product with $\ket{n^{(0)}}$, one gets:
$$\braket{n^{(0)}|\hat{H}^{(1)}|n^{(1)}}=E_n^{(2)}$$
- Substituting the equation for $\ket{n^{(1)}}$:
$$E_n^{(2)}=\sum_{E_m^{(0)}\neq E_n^{(0)}} \braket{m^{(0)}|n^{(1)}}\braket{n^{(0)}|\hat{H}^{(1)}|m^{(0)}}$$
- Substituting for the inner products, and multiplying by $\lambda^2$ gives the _second order energy correction_:
$$\Delta E_n^{(2)}=\sum_{E_m^{(0)}\neq E_n^{(0)}} \frac{|\braket{m^{(0)}|\hat{H}'|n^{(0)}}|^2}{E_n^{(0)}-E_m^{(0)}}$$

## Example: Bump in the square well
