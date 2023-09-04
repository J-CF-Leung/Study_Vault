- - Consider rotations as _acting on the observer_, a.k.a. changing the _axes_

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

## Rotations from invariance of length and distance
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

- As vectors _between_ two points transform in the same way, one gets that the _distances_ between two points (no matter how close) are _unchanged_:
$$\displaylines{(\Delta x')^2+(\Delta y')^2=(\Delta x)^2+(\Delta y)^2 \\ dx'^2+dy'^2=dx^2+dy^2}$$

- Hence, rotations can also be defined as linear transformations $(x,y)\to(x',y')$ such that _distances are left unchanged_
	- This makes _no reference to a shared origin_ (or any origin)
## Lie's approach
- Let there be some rotation by an _infinitesimal angle_ $\theta$
- Then the rotation matrix can be written as:
$$R(\theta)\approx I+A(\theta)$$
- Where the _components_ of $A$ are of _order_ $\theta$, neglecting terms of $O(\theta^2)$ and smaller
	- This requirement also gives $\det{R}=+1$ as reflections are _not continuously related_ to the identity
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

## Higher dimensions and the rotation group
- As before, a rotation in $N-$dimensional space is a transformation which _leaves distance unchanged_:
$$\displaylines{d\bm{x}'=Rd\bm{x}\\ds^2=\sum_{i=1}^N(dx^i)^2=ds'^2}$$
- This gives the conditions:
$$R^TR=I \hspace{1.5cm} \det R=1$$
- This set of $N\times N$ matrices form the _special orthogonal group_ $SO(N)$
	- One can check that they satisfy all required axioms

- Following Lie's approach, for _small rotations_:
$$R\simeq I+A \hspace{1.5cm} A=-A^T$$
- The, one simply writes down _any antisymmetric matrix_ for $A$
- For $N=3$:
$$\displaylines{\mathcal{J}_x=\pmatrix{0&0&0\\0&0&1\\0&-1&0}\;\;\;\mathcal{J}_y=\pmatrix{0&0&-1\\0&0&0\\1&0&0}\;\;\;\mathcal{J}_z=\pmatrix{0&1&0\\-1&0&0\\0&0&0} \\ A=\theta_x\mathcal{J}_x+\theta_y\mathcal{J}_y+\theta_z\mathcal{J}_z}$$
- These 3 matrices are the _generators_ of rotation around axes in 3-dimensional space
- _Any_ 3-dimensional rotation can then be written as:
$$R(\theta)-\exp(\theta_x\mathcal{J}_x+\theta_y\mathcal{J}_y+\theta_z\mathcal{J}_z)=\exp\left(\sum_i\theta_i\mathcal{J}_i\right)$$
### Angular momentum
- Recall that in physics, [[Angular momentum in quantum mechanics|angular momentum]] is the _generator of rotations_
- Observable quantities in quantum mechanics are represented by _Hermitian_ matrices, hence the _angular momentum operators_ are:
$$J_x\equiv-i\mathcal{J}_x \hspace{1cm} J_y\equiv-i\mathcal{J}_y \hspace{1cm} J_z\equiv-i\mathcal{J}_z$$
- The rotation is then:
$$R(\theta)=\exp\left(i\sum_j\theta_jJ_j\right)=\exp(i\bm{\theta}\cdot\bm{J})$$

## Lie algebra
- In simple terms, the _Lie algebra_ is a way to understand how these groups behave
### Commutators and the Lie algebra of SO(3)
- Let there be two _infinitesimal rotations_:
$$R\simeq I+A \hspace{1cm} R'=I+B$$
- Then consider:
$$RR'R^T\simeq R'+AR'-R'A\simeq I+B+AB-BA$$
- Define the _commutator_:
$$[A,B]=AB-BA$$
- The commutators measure _how badly the rotations commute_

- In $SO(3)$, the matrices $J_i$ are known as the _generators of the Lie algebra of $SO(3)$
- Expanding:
$$\displaylines{A=i\sum_j\theta_jJ_j \hspace{1cm} B=i\sum_k\theta_k'J_k \\ [A,B]=i^2\sum_{i,j}\theta_i\theta_j'[J_i,J_j]}$$
- By performing the transpose, one finds that the commutator is _itself an antisymmetric matrix_ and can therefore be written as (using summation convention):
$$\displaylines{[J_j,J_k]=ic_{jkl}J_l \\ c_{kjl}=-c_{jkl}}$$
- Explicit calculations from the matrices [[#Higher dimensions and the rotation group|above]] gives:
$$\displaylines{[J_x,J_y]=iJ_z\hspace{1cm}[J_y,J_z]=iJ_x\hspace{1cm}[J_z,J_x]=iJ_y \\ [J_j,J_k]=i\epsilon_{jkl}J_l}$$
- The lower expression uses the [[Einstein notation#The Levi-Civita tensor|Levi-Civita symbol]] to express antisymmetry $(\epsilon_{kjl}=-\epsilon_{jkl})$

- This expression gives the _multiplicative structure_ of the generators, and hence _that of infinitesimal rotations_
- The multiplicative structure of _finite rotations_ are then given using _exponentiation_

### General Lie groups
- The above process is applicable for _any group_ whose elements $g(\theta_1,\theta_2,\dots)$ are labelled by a set of _continuous parameters_ such that $g(0,0\dots)=I$
- The group elements can be _expanded around the identity_ as the parameters _tend to zero_:
$$\displaylines{g\simeq I+A \\ A=i\sum_a \theta_a T_a}$$
- $T_a$ are the _generators_ of the group determined by its nature
- Then given two elements:
$$\displaylines{g_1\simeq I+A \hspace{1.5cm}g_2=\simeq I+B \\ g_1g_2g_1^{-1}\simeq I+B+[A,B]}$$
- Writing $B$ as a _different linear combination of generators_ $B=i\sum_b\theta_b'T_B$
- Then one gets the _commutation relations_
$$[T_a,T_b]=if_{abc}T_c$$
- The commutator between _any two generators_ can be written as a _linear combination of the generators_
- The constants $f_{abc}$ are known as the _structure constants_ of the _Lie algebra_, which determine the _Lie group_

- While the _Lie group_ is characterised by _multiplication_ (as seen in its [[Foundations of Group Theory#Presentations|presentation]]), the _Lie algebra_ is characterised by _commutation_
	- The real antisymmetric matrices $\mathcal{J}$ in the rotation group _do not close under multiplication_, only _commutation_
		- "One has to get out of the algebra before getting back in"

- _Formally_, the _Lie algebra_ is the _linear space_ spanned by _linear combinations of generators_ $\sum_i\theta_i\mathcal{J}_i$
	- In rotation groups, _linear combinations make no sense_, as composites are represented by _multiplication_
- It can also be described as a linear vector space $V$ with a map $f:V\otimes V\to V$, which satisfy $f(A,B)=-f(B,A)$

- The relation between the group and algebra are implied by the _Baker-Campbell-Hausdorff formula_:
$$\displaylines{e^Ae^B=e^C \\ C=A+B+\frac{1}{2}[A,B]+\frac{1}{12}([A,[A,B]]+[B,[B,A]])}$$

### The generators of SO(N)
- For _any number of dimensions_ $N$, the generators $J_{(mn)}$ are constructed by:
	- Have the entry in the $m$-th row and $n$-th column be $1$
	- Have the entry in the $n$-th row and $m$-th column be $-1$
	- Have _all other_ entries be 0
	- Multiply by $-i$ to be _Hermitian_
- Or, in index notation:
$$(J_{(mn)})^{ij}=-i(\delta^{mi}\delta^{nj}-\delta^{ni}\delta^{mj})$$
- Evidently, $J_{(mn)}=-J_{(nm)}$ and $J_{(mm)}=0$ 
- The _total number of unique generators_ is $N(N-1)/2$

- As before, any _infinitesimal rotation_ is written as:
$$\displaylines{R\simeq I+A \\ A=i\sum_{mn}\,\theta_{(mn)}J_{(mn)}}$$
- The _antisymmetric coefficients_ $\theta_{(mn)}=-\theta_{(nm)}$ denote the $N(N-1)/2$ _generalised angles_
- $J_{(mn)}$ are the _generators of the special orthogonal group_ $SO(N)$

#### Note on labelling
- Rotations are _not always uniquely labelled by an axis_, but are labelled by _planes_
- In 3-dimensional space, planes are _uniquely defined by vectors_
	- A rotation around the $z-$axis can be said to be in the $xy$ plane

### The Lie algebra of SO(N)
- The _commutators_ between $J_{(mn)}$ can be worked out to obtain the Lie algebra
- However, consider the general case $[J_{(mn)},J_{(pq)}]$
- If they have _no integers in common_, the rotations must _commute_
- If they have _two integers in common_, then the commutator is simply _zero_

- For _one integer in common_, assume $m=p$ without loss of generality
- This is the same as a commutator in the _subgroup_ [[#Commutators and the Lie algebra of SO(3)|SO(3)]], but relabelled:
$$[J_{(mn)},J_{(mq)}]=iJ_{(nq)}$$
- Then using the _antisymmetry_ of the generators:
$$[J_{(mn)},J_{(pq)}]=i\left[\delta^{mp}J_{(nq)}+\delta^{nq}J_{(np)}-\delta^{mq}J_{(np)}-\delta^{np}J_{(mq)}\right]$$

- The coefficients in front of the generators are the [[#General Lie groups|structure constants]]
	- Each generator can technically labelled with a _single index_, thus fitting the definition in the above section