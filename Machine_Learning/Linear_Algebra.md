# Mind Map
- Matrices
  - Types of Matrices
    - Square Matrix
    - Row Matrix
    - Column Matrix
    - Zero Matrix
    - Identity Matrix
    - Diagonal Matrix
  - Basic Matrix Operations
    - Scalar Addition
    - Scalar Multiplication
    - Matrix Multiplication
    - Matrix Addition
  - Matrix Transpose
  - Determinant of a matrix
  - Matrix Inversion
3. Vectors
4. Eigenvalues and Eigenvectors
6. Matrix Factorization (SVD, QR decomposition)

# Matrices
# **Matrices in Data Science**

## **1. Introduction to Matrices**

A **matrix** is a rectangular array of numbers, symbols, or expressions, arranged in rows and columns. Matrices are a foundational tool in linear algebra, which plays a critical role in various fields of data science, such as machine learning, computer vision, optimization, and more.

### **Matrix Notation**
A matrix is denoted by a capital letter, say \( A \). For example, a matrix with \( m \) rows and \( n \) columns (an \( m \times n \) matrix) looks like this:
```math
\[
A = \begin{bmatrix} 
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{bmatrix}
\]
```
Here, \( a_{ij} \) is the element of the matrix at the \( i \)-th row and \( j \)-th column.

## **2. Types of Matrices**

1. **Row Matrix**: A matrix with only one row (\( 1 \times n \)).
2. **Column Matrix**: A matrix with only one column (\( m \times 1 \)).
3. **Square Matrix**: A matrix where the number of rows equals the number of columns (\( n \times n \)).
4. **Diagonal Matrix**: A square matrix in which all elements outside the main diagonal are zero.
5. **Identity Matrix**: A diagonal matrix where all diagonal elements are 1, denoted as \( I \).

## **3. Matrix Operations**

### **Addition and Subtraction of Matrices**
Two matrices of the same dimension can be added or subtracted by adding or subtracting their corresponding elements:
```math
\[
A + B = \begin{bmatrix} 
a_{11} + b_{11} & a_{12} + b_{12} \\
a_{21} + b_{21} & a_{22} + b_{22} 
\end{bmatrix}
\]
```
### **Matrix Multiplication**
Matrix multiplication is only possible if the number of columns in the first matrix equals the number of rows in the second matrix. For two matrices \( A \) and \( B \):
```math
\[
(A \times B)_{ij} = \sum_{k=1}^{n} a_{ik} \cdot b_{kj}
\]
```
### **Scalar Multiplication**
If \( \lambda \) is a scalar, multiplying a matrix \( A \) by \( \lambda \) scales every element in the matrix:
```math
\[
\lambda A = \begin{bmatrix} 
\lambda a_{11} & \lambda a_{12} \\
\lambda a_{21} & \lambda a_{22}
\end{bmatrix}
\]
```
## **4. Special Matrices**

1. **Zero Matrix**: A matrix where all elements are zero.
2. **Symmetric Matrix**: A matrix \( A \) is symmetric if \( A = A^T \) (i.e., \( A_{ij} = A_{ji} \)).
3. **Orthogonal Matrix**: A matrix \( A \) is orthogonal if \( A^T A = I \), where \( I \) is the identity matrix.

## **5. Determinant and Inverse of Matrices**

### **Determinant**
The determinant of a square matrix \( A \) provides important information, including whether the matrix is invertible. For a \( 2 \times 2 \) matrix:
```math
\[
\text{det}(A) = \begin{vmatrix} 
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{vmatrix} = a_{11}a_{22} - a_{12}a_{21}
\]
```
### **Inverse**
The inverse of a matrix \( A \) exists only if \( \text{det}(A) \neq 0 \). The inverse of a matrix \( A \), denoted \( A^{-1} \), satisfies \( A A^{-1} = I \).

For a \( 2 \times 2 \) matrix, the inverse is:
```math
\[
A^{-1} = \frac{1}{\text{det}(A)} \begin{bmatrix} 
a_{22} & -a_{12} \\
-a_{21} & a_{11}
\end{bmatrix}
\]
```
## **6. Significance of Matrices in Data Science**

Matrices are extensively used in data science and machine learning for tasks such as:

- **Data Representation**: Datasets are often stored as matrices, where rows represent samples and columns represent features.
- **Linear Transformations**: Matrices are used to apply transformations in machine learning algorithms.
- **Principal Component Analysis (PCA)**: PCA relies on matrix decompositions like eigenvalue and singular value decomposition (SVD) to reduce dimensionality.
- **Neural Networks**: Weights and inputs in neural networks are often represented as matrices, and matrix multiplication is used for forward and backward propagation.



# Vectors
- A vector is a mathematical object that has both magnitude and direction.
- Vector v is represented by v = [v1, v2, ........, vn]
- v = [1, 2, 3], represent a 3-dimensional vector
- vi is a vector component corresponding to a coordinate in a specific dimension.
- Types of vector
  - zero vector = [0, 0, 0, ......, 0]
  - unit vector = magnitude is 1
  - standard basis vector = 1 in one position and 0 in all others. ex:- e1 = [1, 0, 0], e2 = [0, 1, 0], e3 = [0, 0, 1]
- Basic Vector Operations
  - Addition
    - u = [u1, u2, u3, ..........., un], v = [v1, v2, v3, ......., vn]
    - u+v = [u1+v1, u2+v2, ........, un+vn]
  - Scalar Multiplication
    - c.v = [c.v1, c.v2, ......, c.vn]
  - Dot Product
    - u.v = u1v1 + u2v2 + ....... + unvn = ∑uivi
    - **Significance**
      - The dot product measures the degree of alignment between two vectors.
      - If the dot product is 0, the vectors are orthogonal (perpendicular).
      - If it’s positive, the vectors point in a similar direction; if negative, they point in opposite directions.
  - Cross Product
    - In 3D space, the cross product of two vectors u and v results in a vector that is orthogonal to both u and v. It is calculated as:
    - u x v = [[i   j  k]
               [u1 u2 u3]
               [v1 v2 v3]]
  - The magnitude gives the length of the vector, which is important for normalizing vectors and comparing distances in space.
  - Magnitude (Norm) of a vector
  ```math
      ||v|| =  \sqrt{v1^2 + v2^2 ........... + vn^2}
  ```
  - Unit Vector
    - A unit vector is a vector with a magnitude of 1. To convert a vector v into a unit vector, we divide it by its magnitude.
  - Projection of one vector onto another
    - projection of a vector u onto a vector v is a vector that lies along v, representing how much of u points in the direction of v.
```math

     proj_{(v)}u = \frac{u.v}{v.v}v

```
  - Angle between two vectors
```math
  cosθ = \frac{u.v}{||u||||v||}
```
  - Linear Independence and span
    - **Linear Independence **A set of vectors is said to be linearly independent if none of the vectors in the set can be written as a linear combination of the others.
      - v1, v2, v3 are vecctors and c1, c2, c3 are scalars if c1v1 + c2v2 + c3v3 = 0 only when c1, c2, c3 = 0
    - **Span **The span of a set of vectors is the set of all possible vectors that can be created by taking linear combinations of those vectors. For example, the span of two non-parallel vectors in 2D space is the entire 2D plane.

# Eigen Vectors
- They describe special types of linear transformations where vectors only get stretched or compressed, but not rotated when a matrix is applied to them.
- Given square matrix A of size n x n, an eigenvector is a non-zero vector v such that when A is applied to v then the vector is only scaled by a scalar factor λ (called the eigenvalue)
  - Av = λv
  - Av - λv = 0
  - (A-λI)v = 0
  - det(A-λI) = 0
- Geometric Interpretation
  - Eigenvectors: These vectors represent directions along which the transformation A stretches or compresses the vector space.
  - Eigenvalues: These scalars represent the amount of stretching or compression along the corresponding eigenvector. If the eigenvalue is positive, the vector is stretched; if it’s negative, the vector is flipped (reversed) and stretched.
   - Mathematical Significance
     - Principal Component Analysis (PCA): One of the most important applications of eigenvectors is PCA, which is used for dimensionality reduction. PCA finds the eigenvectors (called principal components) of the covariance matrix of data, and the corresponding eigenvalues tell us the amount of variance captured by each principal component.
     - Matrix Diagonalization: Eigenvalue decomposition is used to diagonalize matrices, which simplifies many computations in linear algebra, including solving systems of linear equations or computing matrix exponentials.
     - Markov Chains: In probabilistic models such as Markov chains, the steady-state distribution is given by the eigenvector corresponding to the eigenvalue 1 of the transition matrix.
     - Graph Theory: The eigenvalues of the adjacency matrix of a graph can provide insights into the structure of the graph, such as connectivity and clustering properties.
     - Data Compression: In data compression (e.g., image compression via Singular Value Decomposition), eigenvalues determine how much information is retained after compression.


# Matrix Factorization


