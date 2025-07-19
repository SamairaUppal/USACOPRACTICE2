"""
Read two integers n and m then an integer matrix of size n by m from the input. In the next line, you will read an integer k and the next k lines will be 
the operations you need to apply to the matrix. Output the final matrix after applying the operations.

The operations are in the following format:

swap a b - where a and b are different integers. It swaps the rows a and b.
filter a b - where a and b are integers. In column a, it resets all numbers less than b to 0.
multiply a b - where a and b are integers. It multiplies row a with the value b.
Rows and columns start from 1. The size of the matrix will not be more than 50 by 50 and the number of operations will not be more than 50.
"""


# function that swaps rows a and b
def mSwap(a,b):
    for i in range(m):
        matrix[a][i],matrix[b][i] = matrix[b][i],matrix[a][i]

# function that filters numbers less than b in column a
def mFilter(a,b):
    for i in range(n):
        if matrix[i][a] < b:
            matrix[i][a] = 0

# function that multiplies all numbers in a row a with b
def mMultiply(a,b):
    for i in range(m):
        matrix[a][i] *= b

n,m = input().split()
n,m = int(n),int(m)
matrix = [0]*n

# read the matrix
for row in range(n):
    matrix[row] = input().split()
    for col in range(m):
         matrix[row][col] = int(matrix[row][col])

# read the operations and apply them immediately
k = int(input())
for i in range(k):
    op,a,b = input().split()
    a,b = int(a),int(b)
    if op == "swap":
        mSwap(a-1,b-1)
    elif op == "filter":
        mFilter(a-1,b)
    else:
        mMultiply(a-1,b)

# output the final matrix
for row in range(n):
    for col in range(m):
        print(matrix[row][col],end=" ")
    print()
