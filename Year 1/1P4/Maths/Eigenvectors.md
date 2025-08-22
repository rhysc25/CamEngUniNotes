# Eigenvectors and Eigenvalues

An eigenvector for a transformation is one in which its direction remains unchanged after the transformation, and is non zero, normally normalised. The eigenvalue is the scale factor of the magnitude.

$(A-\lambda I)\textbf{x}=0 \Rightarrow det(A-\lambda I)=0$, forming the characteristic equation.

A matrix is symmetric if $A^T=A$

Theorem: If $\textbf{S}$ is a real, symmetric matrix then we can find a complete set of real eigenvectors and real eigenvalues. If $\textbf{S}$ is a real, symmetric matrix then the eigenvectors of $\textbf{S}$ are orthogonal.

Antisymmetric matrix: $A^T=-A$

A defective nxn matrix is one without n linearly independent eigenvectors. It has too few eigenvectors for the dimensions of the space, so cannot form basis vectors.

Diagonalisation: $A=U\Lambda U^{-1}$. For a real symmetric matrix, $U^{-1}=U^T$

$S'=\Lambda=R^TS R, \Rightarrow$ the diagonal matrix $\Lambda$ represents the same physical transformation as $S$ but in a basis aligned with the eigenvectors.

det$S$ = $\lambda_1\lambda_2\lambda_3$

$A^n=U\Lambda^n U^{-1}$

As the eigenvectors are linearly dependant, or else no inverse would exist, any vector $\textbf{x}$ can be written in terms of the basis eigenvectors $\textbf{u}_1,\textbf{u}_2,\textbf{u}_3$. $\textbf{x}=\alpha \textbf{u}_1+ \beta \textbf{u}_2 + \gamma \textbf{u}_3$

$A\textbf{x}=A(\alpha \textbf{u}_1+ \beta \textbf{u}_2 + \gamma \textbf{u}_3)=\alpha \lambda_1 \textbf{u}_1+ \beta \lambda_2 \textbf{u}_2 + \gamma \lambda_3 \textbf{u}_3$

$A^n\textbf{x}=\alpha \lambda_1^n \textbf{u}_1+ \beta \lambda_2^n \textbf{u}_2 + \gamma \lambda_3^n \textbf{u}_3$

For big enough n, where $\lambda_1$ has the largest absolute value: $A^n \textbf{x} \approx \alpha \lambda_1^n \textbf{u}_1$

Repeated multiplication by a matrix eventually becomes simply multiplication by the largest eigenvalue, eventually picks the part of the vector parallel to the corresponding eigenvector.

When a characteristic equation has complex eigenvalues, such as for a rotation, we know that there is an eigenplane, where all vectors in the plane are transformed to another vector in the plane.

Generalised eigenvalue problem: $A\textbf{x}=\lambda M\textbf{x}$

If $M$ is invertible: $M^{-1}A\textbf{x}=\lambda \textbf{x}$

For the $i$th and $j$th eigenpair, if $i-j$ and $M$ and $A$ are symmetric: $\textbf{x}_i^TA \textbf{x}_i= \lambda_i \textbf{x}_i^T M \textbf{x}_i$.

If $M$ is symmetric positive definite (SPD), which means $\textbf{y}^TM\textbf{y}>0$ for all non-zero $\textbf{y}$, we can normalise the eigenvector using $\textbf{u}_i=\frac{\textbf{x}_i}{\sqrt{\textbf{x}_i^T M \textbf{x}_i}}$

$\Rightarrow \textbf{u}_i^T M \textbf{u}_i=1 \Rightarrow \textbf{u}_i^TA \textbf{u}_i= \lambda_i \textbf{u}_i^T M \textbf{u}_i=\lambda_1$

In summary, if $A$ and $M$ are symmetric, with appropriate normalisation:

$$\textbf{u}_i^TA \textbf{u}_i=
\begin{cases}
   \lambda_1 & i=j\\    
   0 & i \neq j    
\end{cases}$$

$$\textbf{u}_i^T M \textbf{u}_i=
\begin{cases}
   1 & i=j\\    
   0 & i \neq j    
\end{cases}$$
