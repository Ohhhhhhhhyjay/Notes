Cartisian coordinates $(\vec{i},\vec{j},\vec{k})^T$ becomes $(\vec{i'},\vec{j'},\vec{k'})^T$ after linear transformation $R$. For any vector in space $\vec x$ we have

$$\vec x
=
(x',y',z')
\begin{pmatrix}
\vec i'\\
\vec j'\\
\vec k'
\end{pmatrix}
=
(x',y',z')L
\begin{pmatrix}
\vec i\\
\vec j\\
\vec k
\end{pmatrix}
=
(x,y,z)
\begin{pmatrix}
\vec i\\
\vec j\\
\vec k
\end{pmatrix}.
$$

This is to say, linear transformation $L$ can be regarded either as a transformation of the vector coordinates or a transformation of the coordinates, depends on what you want to do.

This way the components of the same vector $\vec x$ in new coordinates is given by

$$(x',y',z') = (x,y,z)L^{-1}$$

The transposed form of above equations are used more often for the form of components tranformation is easier

$$ \vec x = (\vec i', \vec j', \vec k')
\begin{pmatrix}
x'\\
y'\\
z'
\end{pmatrix}
=
(\vec i, \vec j, \vec k)L^{T}
\begin{pmatrix}
x'\\
y'\\
z'
\end{pmatrix}
=
(\vec i, \vec j, \vec k)
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}.
$$

It follows that 

$$
LL^T
\begin{pmatrix}
x'\\
y'\\
z'
\end{pmatrix}
=
L
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}.
$$
If $L$ is orthogonal transformation (orthogonal matrix) then

$$\begin{pmatrix}
x'\\
y'\\
z'
\end{pmatrix}
=
L
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix},$$

which is the formula in 《天文学教程》and《球面天文学》.

## Rotation Matrix
$$Rx(\theta) = 
\begin{pmatrix}
1 & 0 & 0\\
0 & \cos\theta & \sin\theta\\
0 & -\sin\theta & \cos\theta\\
\end{pmatrix}$$

$$Ry(\theta) = 
\begin{pmatrix}
\cos\theta & 0 & -\sin\theta\\
0 & 1 & 0\\
\sin\theta & 0 & \cos\theta\\
\end{pmatrix}$$

$$Rz(\theta) = 
\begin{pmatrix}
\cos\theta & \sin\theta & 0\\
-\sin\theta & \cos\theta & 0\\
0 & 0 & 1\\
\end{pmatrix}$$
Rotational matrices are orthogonal matices.

## Orthogonal Matrix
A matrix $A$ is called orthogonal if

$$A^{T} = A^{-1}$$