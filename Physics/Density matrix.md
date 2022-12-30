## The density matrix
- To test theories in quantum mechanics, one needs a quantum ensemble of $N$ systems to make [[Fundamentals and the matrix-based formulation of quantum mechanics#Measurement|measurements]] on
- It is difficult to make ensembles pure, i.e. all in one state $\wv$
- There may be a _mixed_ ensemble of $k$ different states, represented by kets $\ket{i}$, each with _occupancy number_ $n_i$
- The density operator/matrix is defined as:
$$\rho=\sum_i p_i\ket{i}\bra{i}$$
- Here, $p_i$ is the probability of occupancy $n_i/N$
- A _pure_ state has all $p_i=0$ except one
- The set of $\ket{i}$ don't have to be orthonormal, but the Hermiticity of $\rho$ allows an orthonormal basis to be found
- For an enemble uniformly distributed over $k$ states, $\rho=I/k$
- For an operator $\Omega$, the ensemble average (average of averages in each state) is:
$$\overline{\braket{\Omega}}=\sum_ip_i\braket{i|\Omega|i}=\text{Tr}(\Omega\rho)$$
- For example, to find the probability of getting a value $\omega$:
$$\overline{P(\omega)}=\overline{\braket{\mathcal{P}_\omega}}=\text{Tr}(\mathcal{P}_\omega\rho)$$
- As the trace is the same under any orthonormal basis, this value is _invariant_, as expected
- Several results can be easily derived:
$$\displaylines{\rho^\dagger=\rho \\ \text{Tr}(\rho) =1 \\ \text{Tr}(\rho^2)\leq 1}$$
- For a pure ensemble:
$$\displaylines{\rho^2=\rho \\ \text{Tr}(\rho^2)=1}$$

- The density matrix is used in statistical mechanics as the [[Fundamental principles of statistical mechanics#The statistical matrix|statistical matrix]]
- As the individual state kets making up $\rho$ still follow the [[Fundamentals and the matrix-based formulation of quantum mechanics#Time-evolution The Schrödinger equation|Schrödinger equation]], the time evolution of the density matrix is:
$$i\hbar\pd{\rho}{t}=-[\rho,\Ham]$$
- This is analagous to the classical [[Analytical classical mechanics#Liouville's Theorem|Liouville's equation]]$$\pd{\rho_{clas}}{t}=-\PB{\rho}{\Ham}$$
