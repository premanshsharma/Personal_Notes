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

\[
A = \begin{bmatrix} 
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{bmatrix}
\]

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

\[
A + B = \begin{bmatrix} 
a_{11} + b_{11} & a_{12} + b_{12} \\
a_{21} + b_{21} & a_{22} + b_{22} 
\end{bmatrix}
\]

### **Matrix Multiplication**
Matrix multiplication is only possible if the number of columns in the first matrix equals the number of rows in the second matrix. For two matrices \( A \) and \( B \):

\[
(A \times B)_{ij} = \sum_{k=1}^{n} a_{ik} \cdot b_{kj}
\]

### **Scalar Multiplication**
If \( \lambda \) is a scalar, multiplying a matrix \( A \) by \( \lambda \) scales every element in the matrix:

\[
\lambda A = \begin{bmatrix} 
\lambda a_{11} & \lambda a_{12} \\
\lambda a_{21} & \lambda a_{22}
\end{bmatrix}
\]

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