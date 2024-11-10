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
4. Eigenvalues
5. Eigenvectors
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
     \text{proj_{(v)}u} = \frac{u.v}{v.v}v
```

