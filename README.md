# matrix-without-numpy-
# Function to print a matrix
def print_matrix(matrix):
    for row in matrix:
        print(row)

# Function to add two matrices
def add_matrices(matrix1, matrix2):
    result = []
    for i in range(len(matrix1)):
        temp = []
        for j in range(len(matrix1[0])):
            temp.append(matrix1[i][j] + matrix2[i][j])
        result.append(temp)
    return result

# Function to subtract two matrices
def subtract_matrices(matrix1, matrix2):
    result = []
    for i in range(len(matrix1)):
        temp = []
        for j in range(len(matrix1[0])):
            temp.append(matrix1[i][j] - matrix2[i][j])
        result.append(temp)
    return result

# Function to multiply two matrices
def multiply_matrices(matrix1, matrix2):
    result = []
    for i in range(len(matrix1)):
        temp = []
        for j in range(len(matrix2[0])):
            val = 0
            for k in range(len(matrix2)):
                val += matrix1[i][k] * matrix2[k][j]
            temp.append(val)
        result.append(temp)
    return result

# Function to transpose a matrix
def transpose_matrix(matrix):
    result = []
    for i in range(len(matrix[0])):
        temp = []
        for j in range(len(matrix)):
            temp.append(matrix[j][i])
        result.append(temp)
    return result

# Sample matrices
matrix_A = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrix_B = [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

# Addition of matrices
print("Addition of matrices:")
result_addition = add_matrices(matrix_A, matrix_B)
print_matrix(result_addition)

# Subtraction of matrices
print("\nSubtraction of matrices:")
result_subtraction = subtract_matrices(matrix_A, matrix_B)
print_matrix(result_subtraction)

# Multiplication of matrices
print("\nMultiplication of matrices:")
result_multiplication = multiply_matrices(matrix_A, matrix_B)
print_matrix(result_multiplication)

# Transpose of a matrix
print("\nTranspose of matrix A:")
result_transpose = transpose_matrix(matrix_A)
print_matrix(result_transpose)


