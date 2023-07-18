- Consider rotations as _acting on the observer_, a.k.a. changing the _axes_

## Vectors and the rotation matrix
- Let there be _two sets of Cartesian axes_, which _share an origin_, but with rotated angle $\theta$
- Let their sets of coordinates describe the _same point_ $P$
![[Rotated axes.png]]

- The coordinates are related by:
$$\begin{aligned}x'&=+\cos\theta \,x+\sin\theta\,y \\ y'&=-\sin\theta\,x+\cos\theta\,y\end{aligned}$$
- This _distance_ $OP$ remains unchanged
	- $\sqrt{x^2+y^2}=\sqrt{x'^2+y'^2}$
- Introduce the _column vectors_:
$$\bm{r}=\pmatrix{x \\ y} \hspace{1.5cm} \bm{r}'=\pmatrix{x'\\y'}$$
- They are related by the _rotation matrix_:
$$\displaylines{\bm{r}'=R(\theta)\,\bm{r} \\ R(\theta)=\pmatrix{\cos\theta & \sin\theta \\ -\sin\theta&\cos\theta}}$$
- A _vector_ is anything that _transforms like_ the above relation

## Rotations from invariance of length
- Let there be a transformation law $\bm{p}'=R\bm{p}$, describing a _rotation_, where the form of $R$ is unknown (ignore the above)

- The _length_ of _any vector_ $\bm{p}$ is _invariant_ under the rotation, as $p^2$ remains unchanged
- Consequently, the _scalar product_ $\bm{u}^T\cdot\bm{v}$ of any two vectors $\bm{u}$ and $\bm{v}$ is _also conserved_
	- Write some vector $\bm{p}$ as a _linear combination_ of two vectors, then expand $p^2$
- This also applies to _distances between points_, even _infinitesimal_ lengths

- From the invariance of the scalar product, and using the _transformation law_ above, a _restriction_ is imposed on $R$:
$$R^TR=I$$
- Matrices satisfying this are said to be _orthogonal_

- $2\times 2$ orthogonal matrices are _generators_ of the _orthogonal group of order $2$_, or $O(2)$, with multiplication law:
$$R(\theta_1)R(\theta_2)=R(\theta_1+\theta_2)$$

- The restriction above imposes that $|\det{R}|^2=1$, which means $\det{R}=\pm1$
- The _negative case_ involves _reflection_, as well as _compositions_ of reflection and rotation

- To restrict the transformation to _pure rotations_, impose that:
$$\det{R}=+1$$
- These matrices are both _special_ and _orthogonal_

- $2\times2$ matrices that are both special and orthogonal are the _generators_ of the _special orthogonal group of order $2$_, or $SO(2)$

## Lie's approach
- Let there be some rotation by an _infinitesimal angle_ $\theta$
- Then the rotation matrix can be written as:
$$R(\theta)\approx I+A(\theta)$$
- Where the _components_ of $A$ are of _order_ $\theta$, neglecting terms of $O(\theta^2)$ and smaller
	- This requirement also gives $\det{R}=+1$
- Using the requirement that $R$ is orthogonal:
$$R^TR\approx I+A^T+A=I$$

- At this point, assert that the rotation is in _2 dimensions_
- This requires that $A$ is _antisymmetric_, hence it must be _proportional_ to the _only $2\times 2$ antisymmetric matrix_ $\mathcal{J}$:
$$\displaylines{A=\theta\mathcal{J}=\pmatrix{0 & \theta \\ -\theta & 0} \\ R(\theta)=I+\theta\mathcal{J}+O(\theta^2)}$$
- $\mathcal{J}$ is also known as the _generator of the rotation group_
- This gives that under an infinitesimal rotation:
$$\displaylines{x\to x'=+x+\theta y \\ y\to y'=-\theta x+y}$$

- Then, any _finite rotation_ by angle $\theta$ is a _composition of infinitesimal rotations_:
$$R(\theta)=\lim_{N\to\infty}\left(R\left(\frac{\theta}{N}\right)\right)^N=\lim_{N\to\infty}\left(I+\frac{\theta\mathcal{J}}{N}\right)^N=\exp(\theta\mathcal{J})$$
- Then, using the fact that $\mathcal{J}^2=-I$, _separating_ the exponential series:
$$R(\theta)=\exp(\theta\mathcal{J})=\sum_{n=0}^\infty \frac{1}{n!}(\theta\mathcal{J})^n=\cos\theta\,I+\sin\theta\,\mathcal{J}=\pmatrix{\cos\theta&\sin\theta \\ -\sin\theta&\cos\theta}$$
- This can also be recognised by the fact that $\mathcal{J}$ plays the same role as $i$, as $i^2=-1$

- This approach can be generalised to _higher dimensions_, using larger antisymmetric matrices

## Higher dimensions