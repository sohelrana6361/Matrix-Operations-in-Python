Name: Md Sohel Rana
Edge ID: 13
Inf: Dept. of Mathematics, ID: MA-19035, MS-Session: 2022-23
Project IDEA: Matrix operations are fundamental in many fields of mathematics, computer science, physics, engineering, and data science. In Python, matrix operations can be performed manually or with the help of libraries such as NumPy. This project involves creating a program that can handle basic matrix operations, like addition, subtraction, multiplication, and more.
Project: 
# Matrix Operations in Python

def add_matrices(A, B):
    """Add two matrices."""
    # Check if matrices have the same dimensions
    if len(A) != len(B) or len(A[0]) != len(B[0]):
        raise ValueError("Matrices must have the same dimensions to be added.")

    # Matrix addition: A[i][j] + B[i][j]
    result = [[A[i][j] + B[i][j] for j in range(len(A[0]))] for i in range(len(A))]
    return result


def subtract_matrices(A, B):
    """Subtract matrix B from matrix A."""
    # Check if matrices have the same dimensions
    if len(A) != len(B) or len(A[0]) != len(B[0]):
        raise ValueError("Matrices must have the same dimensions to be subtracted.")

    # Matrix subtraction: A[i][j] - B[i][j]
    result = [[A[i][j] - B[i][j] for j in range(len(A[0]))] for i in range(len(A))]
    return result


def multiply_matrices(A, B):
    """Multiply two matrices."""
    # Check if the number of columns of A equals the number of rows of B
    if len(A[0]) != len(B):
        raise ValueError("Number of columns of A must be equal to the number of rows of B.")

    # Matrix multiplication: Result[i][j] = sum(A[i][k] * B[k][j] for k in range(cols of A))
    result = [[sum(A[i][k] * B[k][j] for k in range(len(A[0]))) for j in range(len(B[0]))] for i in range(len(A))]
    return result
