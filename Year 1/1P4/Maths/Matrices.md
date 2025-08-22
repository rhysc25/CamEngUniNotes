# Matrices

Shear matrix: 
$$\begin{bmatrix}
1 & \tan(\alpha)\\
0 & 1\\
\end{bmatrix}$$ 
Where $\alpha$ is the shear angle from the $y$ axis.

Dot product = $\sum_i a_ib_i$

Matrix multiplication: $$(AB)_{ij}=\sum_{k=1}^n a_{ik}b_{kj}$$

Important Results:
$(ABC...F)^{T}=F^T...C^TB^TA^T$

$\textbf{a}\cdot \textbf{b}=\textbf{a}^T \textbf{b}$

On the other hand, $\textbf{a} \textbf{b}^T$ is a matrix

The cofactor of any element, $C_{ij}=(-1)^{i+j}M_{ij}$ where $M_{ij}$ is the determinant of the submatrix formed by removing the $i$th row and $j$th column.

Properties of the determinant:
1. Multiplication of any row or column by a constant, multiplies the determinant by the same constant
2. The determinant change sign when two rows or columns are exchanged, hence if two rows or columns are equal then det($\textbf{A}$) = 0.
3. Adding a multiple of one row to another leaves the determinant unchanged
4. det($\textbf{A}$)=det($\textbf{A}^T$)
5. If $\textbf{A},\textbf{B}$ are square matrices of equal dimensions, det($\textbf{AB}$) = det($\textbf{BA}$) = det($\textbf{A}$)det($\textbf{B}$)

The columns of a matrix are the mappings of the basis unit vectors after the transformation has been applied.

General rotational matrix, rotating at an angle $\alpha$ anticlockwise:
$$\begin{bmatrix}
\cos(\alpha) & -\sin(\alpha)\\
\sin(\alpha) & \cos(\alpha)\\
\end{bmatrix}$$

For any rotation: $\textbf{Q}^{-1}=\textbf{Q}^T \Rightarrow \textbf{Q}^T\textbf{Q}=\textbf{Q}\textbf{Q}^T=\textbf{I}$

A matrix with the property $\textbf{B}^{-1}=\textbf{B}^T$ is known as an orthogonal matrix.

Both reflections and rotations preserve the length of and angle between vectors. However the determinant of a rotational matrix is $1$, whereas the determinant of a reflection matrix is $-1$.

If the reflection is an arbitrary plane, we can rotate the coordinate frame so that it is reflected $z=0$ for example.

To check a matrix is a rotation: Check that the matrix is orthogonal, the dot product of all the columns is 0. Check that the columns are all unit vectors. Check that the determinant is 1.

If a vector $\textbf{a}$ is moved from coordinate system $\textbf{e}_i$ to $\textbf{e}_i'$, where $\textbf{e}_i'=\textbf{R}\textbf{e}_i$:
$\textbf{a}'=\textbf{R}^T\textbf{a}$ or $\textbf{a}'=\textbf{R}^{-1}\textbf{a}$ if not a rotation

If there is a matrix $\textbf{A}$ that transforms the vector $\textbf{b}$ to the vector $\textbf{c}$, in the new coordinate system, the matrix that transforms the vector $\textbf{b}'$ to vector $\textbf{c}'$ is given by:
$$\textbf{A}'=\textbf{R}^{-1}\textbf{A}\textbf{R}$$

If working in the other direction: $\textbf{A}=\textbf{R}\textbf{A}'\textbf{R}^{-1}$ or $\textbf{A}=\textbf{R}\textbf{A}'\textbf{R}^{T}$ if $\textbf{R}$ is a rotation
