## Gyration tensor
- The gyration tensor describes the second moments of position for a collection of $N$ particles, or a continuous body 
$$S_{mn}=\frac{1}{N}\sum_{i=1}^Nr_m^{(i)}r_n^{(i)}=\frac{\int\rho(\bm{r})r_mr_nd\bm{r}}{\int\rho(\bm{r})\,d\bm{r}}$$
	- $\rho(\bm{r})$ is number density
- All coordinates are measured relative to the centre of mass
- In the case where all masses are identical, it is a scaled version of the [[Rotational mechanics|tensor of inertia]]
- Like the tensor of inertia, it can be diagonalised
	- As it is symmetric (real Hermitian), orthonormal eigenvectors (principal directions) can always be found
	- The diagonal elements are the principal moments
	- In the case of 3 dimensions:
$$S=\begin{bmatrix}\lambda_x^2 & 0 & 0 \\ 0 & \lambda_y^2 & 0 \\ 0 & 0 &\lambda_z^2\end{bmatrix}$$
		- By convention, $\lambda_x^2<\lambda_y^2<\lambda_z^2$
- The radius of gyration $R_g$ is defined as the trace of the gyration tensor:
$$R_g^2=S_{xx}+S_{yy}+S_{zz}=\lambda_x^2=\lambda_y^2=\lambda_z^2$$
## Descriptors of shape
- Asphericity: measures how symmetrical the distribution of particles is
$$b=\lambda_z^2-\frac{1}{2}\left(\lambda_x^2+\lambda_y^2\right)$$
	- Zero: perfectly spherical
	- Nomalise to be between 0 and 1: divide by $R_g^2$
- Acylindricity:
$$c=\lambda_y^2-\lambda_x^2$$
- Relative shape anisotropy:
$$\kappa^2=\frac{b^2+3c^2/4}{R_g^4}$$
	- 0 if spherically symmetrical
	- 1 if all points are on a line