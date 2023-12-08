**Lecture**
$Ax=b$
_find solution_
Augmented matrix $=[\begin{array}{}A&b\end{array}]$
$$
\left[\begin{matrix}{}1&2&2&2&b_1\\2&4&6&8&b_2\\3&6&8&10&b_3\end{matrix}\right]
$$

$$
\left[\begin{array}{}1&2&2&2&b_1\\0&0&2&4&b_2-2b_1\\0&0&2&4&b_3-3b_1\end{array}\right]
$$
$0=b_3-b_2-b_1$
$$
b=
$$
Solvability Condition on b
$Ax=b$ Solvable when b is in $C(A)$
If a comb of rows of A gives zero rows
Then the same comb of the entries of b must give 0

To find complete sol'n to $Ax=b$
- $x_{particular}$: 
	- set all free variables to zero
	- solve $Ax=b$ for pivot variable
- $x_{nullspace}$:
	- $x=x_p+x_n$ 

$$
x_{complete}=\left[\begin{array}{}-2\\0\\\frac{3}{2}\\0\end{array}\right]+c_1\left[\begin{array}{}-2\\1\\0\\0\end{array}\right]+c_2\left[\begin{array}{}2\\0\\-2\\1\end{array}\right]
$$
Plot all solutions $x$ in $R^4$
![[Pasted image 20231025005054.png]]
$m$ by $n$ matrix $A$ of rank $r$ (know $r<=m$, $r<=n$)
Full column rank means $r=n$
$N(A)=\{zero vector\}$
unique solution if it exist
$x=x_p$

- $R=m=n$
	- inversible
	- $R=I$
	- $1\quad solution$
- $r=n<m$
	- $R=\left[\begin{array}{}I\\0\end{array}\right]$
	- $((0\quad or\quad 1\quad solution))$
- $r=m<n$
	- $R=[I\quad F]$
	- $((1\quad or\quad \infty))$
- $r<m,r<n$
	- $R=\left[\begin{array}{}I&F\\0&0\end{array}\right]$
	- $((0\quad or\quad \infty))$

$$
Ax=0
$$
_more unknown than equations_
Reason: There will be free variables!!

**Linear independent**
Vectors $x_1,x_2,\dots,x_n$ are independent if on combination gives zero vector(except The zero com all $c_i=0$)
$$
c_1x_1+c_2x_2+c_3x_3+\dots+c_nx_n=0
$$

_dependent_
![[Pasted image 20231026231340.png]]

independent
![[Pasted image 20231026231838.png]]

Repeat when $v_1,\dots,v_n$ are columns of A
They are independent if null-space of A is {zero vector}
- rank$=n$ 
- no free variables
- $N(A)=\{0\}$
They are dependent if $Ac=0$ for some 
- rank$<n$
- yes free variables

_Vectors_ $v_1,\dots,v_n$ span a space means: The space consist of all combs of These vectors

**basis** for a space is a sequence of vectors $v_1,\dots,v_d$ with two properties:
- they are independent
- they span the space
Example:
	Space is $R^3$
	One basis is\[standard basic]
	![[Pasted image 20231026233314.png]]
invertible

definition:
![[Pasted image 20231026234545.png]]

$2=rank(A)=\#pivot\ columns=dimension\ of\ C(A)$
$dimC(A)=r$
$dimN(A)=\#free\ variables=n-r$

4 Subspaces
- column space $C(A)$ in $R^m$
- null space $N(A)$ in $R^n$
- row space $N(A)$ = all comb of rows = all combs of the columns of $A^T=C(A^T)$ in $R^n$
- null space of $A^T=N(A^T)$=left null space of $A$ is $R^m$
$A\ is\ m\times n$
![[Pasted image 20231102001542.png]]
**basis?**
**dimension?**
$C(A)=rank\ r$
dim $C(A^T)=r$
dim $N(A)=n-r$
dim $N(A^T)=m-r$

$C(R)\not=C(A)$
different col.space
same row space
Basis for row space is first r rows of R
![[Pasted image 20231102090747.png]]

$4^{th}$space: $N(A^T)$
$A^Ty=0$
->$y^TA=0^T$
left null space
$E[A_{m\times n}I_{m\times m}]->[R_{m\times n}E_{m\times m}]$
![[Pasted image 20231102091541.png]]

new vector space $M$
All $3\times 3$ matrices
Subspaces of M | upper triangles | symmetric matrices | diagonal matrices
$dimM=9$
$dimS=6$
$dimU=6$
![[Pasted image 20231106234311.png]]
$dim(S\bigcap U)=3$
$S+U=$ any $3\times3's$
$dim(S\bigcup U)=3+dim(S+U)=9$
![[Pasted image 20231106235322.png]]

$$A=\left[\begin{matrix}1&4&5\\2&8&10\end{matrix}\right]=\left[\begin{matrix}1\\2\end{matrix}\right]\left[\begin{matrix}1&4&5\end{matrix}\right]$$
Subset of rank 1 matrices not a subspace

$Graph = {nodes,edges}$
![[Pasted image 20231107235642.png]]
Incidence Matrix
$$A=\left[\begin{matrix}-1&1&0&0\\0&-1&1&0\\-1&0&1&0\\-1&0&0&1\\0&0&-1&1\end{matrix}\right]$$
$dimN(A)=1$
$rank=3$
![[Pasted image 20231108003626.png]]
TREE: no loop graph
![[Pasted image 20231108005417.png]]
$dimN(A^T)=m-r$
$\#loops=\#edges(\#nodes-1)$
$(rank=n-1)$
$\#nodes-\#edges+\#loops=1$
Euler's formula
![[Pasted image 20231108005357.png]]
$A^TCAx=f$
![[Pasted image 20231108005708.png]]

#### Orthogonal
![[Pasted image 20231113233443.png]]
$x^Ty=0$
$x^Tx+y^Ty=(x+y)^T(x+y)$
![[Pasted image 20231113234414.png]]
##### Subspace S is orthogonal to subspace T
Means: every vector in S is orthogonal to every vector in T. 

Row space is orthogonal to null-space
![[Pasted image 20231113235507.png]]

![[Pasted image 20231114000555.png]]
Coming: $Ax=B$
"Solve" when there is no solution
![[Pasted image 20231114002207.png]]

### Projection
![[Pasted image 20231115234327.png]]
$xa^Ta=a^Tb$
$x =\frac{a^Tb}{a^Ta}\quad p=ax$
$p=a\frac{a^Tb}{a^Ta}$
$projp=Pb$
matrix
$P=\frac{aa^T}{a^Ta}$
$P^T=P$
$P^2=P$
#### Why project?
Because $Ax=b$ may have no solution
![[Pasted image 20231116000520.png]]
![[Pasted image 20231116001122.png]]
![[Pasted image 20231116001910.png]]

Least squares fitting by a line
$(1,2),(2,2),(3,2)$
$b=C+Dt$
$C+D=1$
$C+2D=2$
$C+3D=2$
$$
\left[\begin{array}{}1&1\\1&2\\1&3
\end{array}\right]\left[\begin{array}{ }C&D
\end{array}\right]=\left[\begin{array}{}1 \\
2 \\
2
\end{array}\right]
$$

![[Pasted image 20231121231429.png]]
![[Pasted image 20231121232629.png]]
Get best solution
Find $\hat{x}=\left[\begin{matrix}{}1\\2\end{matrix}\right]$
![[Pasted image 20231121234158.png]]
Just fund the derivatives
![[Pasted image 20231121235630.png]]
IDEA $x^TA^TAx=0=(Ax)^T(Ax)$ -> $Ax=0$ -> $x=0$
![[Pasted image 20231122000442.png]]

![[Pasted image 20231123174051.png]]
$q_{i}^Tq_{j}=\left\{\begin{matrix}1&i=j\\0i& \not =j\end{matrix}\right.$
![[Pasted image 20231123174401.png]]
![[Pasted image 20231123184937.png]]
$A=LU$ -> $A=QR$

Determinants $\det A=\mid A\mid$
- $\det I=1$
- Exchange rows: reverse sign of $\det$ 
- ![[Pasted image 20231127233748.png]]
- LINEAR EACH ROW
- ![[Pasted image 20231127234118.png]]

- 2 equal rows $\rightarrow$ $\det=0$
- Subtract $l \times row\ i$ from $row\ k$ $\rightarrow$  $\det$ don't change 
- ![[Pasted image 20231127235025.png]]
- ![[Pasted image 20231127235549.png]]
- $\det A=0$ when $A$ is singular
- ![[Pasted image 20231128233553.png]]
- $\det AB=(\det A)(\det B)$ 
	- $\det A^{-1}=\frac{1}{\det A}$
- $\det A^T=\det A$
	- $\#10\quad\mid A^T\mid=\mid A\mid$
	- $\mid U^TL^T\mid=\mid LU\mid$
	- $\mid U^T\mid\mid L^T\mid=\mid L\mid\mid U\mid$

Big formulation
$$
\det A=\sum\pm a_{1\alpha}a_{2\beta}a_{3\gamma}\cdots a_{n \omega}
$$
$$
(\alpha,\beta,\gamma,\dots,\omega)=perm\ of(1,2,3,\dots,n)
$$
Cofactors $3\times3$
$\det=a_{11}(a_{22}a_{33}-a_{23}a_{32})+a_{12}(\qquad)+\cdots$
Cofactors of $a_{ij}=C_{ij}$
$\pm \det(n-1\ \ with\ row\ i\ col\ j\ erased)$
Cofactors formula
$\det A=a_{11}C_{11}+a_{12}C_{12}+\cdots+a_{1n}C_{1n}$
$\mid A_{n}\mid=\mid A_{n-1}\mid-\mid A_{n-2}\mid$
$$
\begin{bmatrix}
a&b\\c&d
\end{bmatrix}=\frac{1}{ad-bc}\begin{bmatrix}
d&-b\\-c&a
\end{bmatrix}
$$
$$
A^{-1}=\frac{1}{\det A}C^T
$$
Check $AC^T=(\det A)I$

$$
\begin{bmatrix}
a_{11}\cdots a_{1n} \\
 \\
a_{n1}\cdots a_{nn}
\end{bmatrix}
\begin{bmatrix}
C_{11}&C_{n1} \\
\vdots& \vdots \\
C_{1n}&C_{nn}
\end{bmatrix}=\begin{bmatrix}
\det A&& \\
&\det A& \\
&&\det A
\end{bmatrix}
$$
