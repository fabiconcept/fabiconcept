Let's solve the system of equations using **Cramer's Rule**:

### 1. Write the system of equations:
\[
\begin{aligned}
x + y &= 2 \\
2x - z &= 1 \\
2y - 3z &= -1
\end{aligned}
\]

### 2. Represent the system in matrix form \( A \cdot X = B \):
\[
A = \begin{pmatrix} 
1 & 1 & 0 \\ 
2 & 0 & -1 \\ 
0 & 2 & -3 
\end{pmatrix}, \quad
X = \begin{pmatrix} 
x \\ 
y \\ 
z 
\end{pmatrix}, \quad
B = \begin{pmatrix} 
2 \\ 
1 \\ 
-1 
\end{pmatrix}
\]

### 3. Find the determinant of the coefficient matrix \( \text{det}(A) \):
\[
\text{det}(A) = \begin{vmatrix} 
1 & 1 & 0 \\ 
2 & 0 & -1 \\ 
0 & 2 & -3 
\end{vmatrix}
\]

Expanding this determinant:

\[
\text{det}(A) = 1 \begin{vmatrix} 0 & -1 \\ 2 & -3 \end{vmatrix}
- 1 \begin{vmatrix} 2 & -1 \\ 0 & -3 \end{vmatrix}
+ 0 \cdot \begin{vmatrix} 2 & 0 \\ 0 & 2 \end{vmatrix}
\]

We now compute the 2x2 determinants:

\[
\begin{vmatrix} 0 & -1 \\ 2 & -3 \end{vmatrix} = (0)(-3) - (-1)(2) = 0 + 2 = 2
\]
\[
\begin{vmatrix} 2 & -1 \\ 0 & -3 \end{vmatrix} = (2)(-3) - (-1)(0) = -6
\]

Now substitute these into the expansion:

\[
\text{det}(A) = 1(2) - 1(-6) + 0 = 2 + 6 = 8
\]

### 4. Compute determinants for \( D_x \), \( D_y \), and \( D_z \):

**For \( D_x \): Replace the first column of \( A \) with \( B \):**
\[
D_x = \begin{vmatrix} 
2 & 1 & 0 \\ 
1 & 0 & -1 \\ 
-1 & 2 & -3 
\end{vmatrix}
\]

Expanding this determinant:

\[
D_x = 2 \begin{vmatrix} 0 & -1 \\ 2 & -3 \end{vmatrix}
- 1 \begin{vmatrix} 1 & -1 \\ -1 & -3 \end{vmatrix}
+ 0 \cdot \begin{vmatrix} 1 & 0 \\ -1 & 2 \end{vmatrix}
\]

We now compute the 2x2 determinants:

\[
\begin{vmatrix} 0 & -1 \\ 2 & -3 \end{vmatrix} = 2 \quad \text{(already computed)}
\]
\[
\begin{vmatrix} 1 & -1 \\ -1 & -3 \end{vmatrix} = (1)(-3) - (-1)(-1) = -3 - 1 = -4
\]

Now substitute these into the expansion:

\[
D_x = 2(2) - 1(-4) + 0 = 4 + 4 = 8
\]

**For \( D_y \): Replace the second column of \( A \) with \( B \):**
\[
D_y = \begin{vmatrix} 
1 & 2 & 0 \\ 
2 & 1 & -1 \\ 
0 & -1 & -3 
\end{vmatrix}
\]

Expanding this determinant:

\[
D_y = 1 \begin{vmatrix} 1 & -1 \\ -1 & -3 \end{vmatrix}
- 2 \begin{vmatrix} 2 & -1 \\ 0 & -3 \end{vmatrix}
+ 0 \cdot \begin{vmatrix} 2 & 1 \\ 0 & -1 \end{vmatrix}
\]

We now compute the 2x2 determinants:

\[
\begin{vmatrix} 1 & -1 \\ -1 & -3 \end{vmatrix} = -4 \quad \text{(already computed)}
\]
\[
\begin{vmatrix} 2 & -1 \\ 0 & -3 \end{vmatrix} = -6 \quad \text{(already computed)}
\]

Now substitute these into the expansion:

\[
D_y = 1(-4) - 2(-6) + 0 = -4 + 12 = 8
\]

**For \( D_z \): Replace the third column of \( A \) with \( B \):**
\[
D_z = \begin{vmatrix} 
1 & 1 & 2 \\ 
2 & 0 & 1 \\ 
0 & 2 & -1 
\end{vmatrix}
\]

Expanding this determinant:

\[
D_z = 1 \begin{vmatrix} 0 & 1 \\ 2 & -1 \end{vmatrix}
- 1 \begin{vmatrix} 2 & 1 \\ 0 & -1 \end{vmatrix}
+ 2 \begin{vmatrix} 2 & 0 \\ 0 & 2 \end{vmatrix}
\]

We now compute the 2x2 determinants:

\[
\begin{vmatrix} 0 & 1 \\ 2 & -1 \end{vmatrix} = (0)(-1) - (1)(2) = -2
\]
\[
\begin{vmatrix} 2 & 1 \\ 0 & -1 \end{vmatrix} = (2)(-1) - (1)(0) = -2
\]
\[
\begin{vmatrix} 2 & 0 \\ 0 & 2 \end{vmatrix} = (2)(2) - (0)(0) = 4
\]

Now substitute these into the expansion:

\[
D_z = 1(-2) - 1(-2) + 2(4) = -2 + 2 + 8 = 8
\]

### 5. Compute \( x \), \( y \), and \( z \):
\[
x = \frac{D_x}{\text{det}(A)} = \frac{8}{8} = 1
\]
\[
y = \frac{D_y}{\text{det}(A)} = \frac{8}{8} = 1
\]
\[
z = \frac{D_z}{\text{det}(A)} = \frac{8}{8} = 1
\]

### Final Solution:
\[
x = 1, \quad y = 1, \quad z = 1
\]