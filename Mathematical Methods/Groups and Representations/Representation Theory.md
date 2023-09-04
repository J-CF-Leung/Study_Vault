- The idea is to _represent group elements by matrices_
- The matrices must _reflect the [[Foundations of Group Theory#Multiplication tables|multiplicative table]] of the group_
- One _associates each element_ $g$ with its own $d\otimes d$ matrix $D(g)$ such that: 
$$D(g_1)D(g_2)=D(g_1g_2)$$
- From this, one can immediately tell that $D(I)=I_d$, where $I_d$ is the $d\otimes d$ _identity matrix_
- One can also prove that $D(g^{-1})=D(g)^{-1}$
## Representing the permutation group
- Consider $S_4$, the [[Foundations of Group Theory#Permutation Groups and Cayley's Theorem|permutation group]] of four objects
- Let the four objects be represented by _vectors_:
$$\bm{v}_1 = \pmatrix{1\\0\\0\\0} \hspace{1cm} \bm{v}_2 = \pmatrix{0\\1\\0\\0} \hspace{1cm} \bm{v}_3 = \pmatrix{0\\0\\1\\0} \hspace{1cm} \bm{v}_4 = \pmatrix{0\\0\\0\\1}$$
- For a 2-cycle $(ij)$, construct $D(ij)$ such that $D(ij)\bm{v}_i=\bm{v}_j$ and vice versa
- Similarly, $D(ijk)\bm{v}_k=\bm{v}_i$ and so on
- For example:
$$D(2413)=\pmatrix{0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0}$$
- One finds that these matrices _follow the multiplicative structure of permutations_
- As $S_4$ has 24 elements, there are 24 _distinct_ $4\otimes4$ matrices representing the group
