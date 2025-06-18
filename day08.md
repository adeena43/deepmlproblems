```py
def matrixmul(a: list[list[int | float]], b: list[list[int | float]]) -> list[list[int | float]]:

    # Check if number of columns in A equals number of rows in B
    if len(a[0]) != len(b):
        return -1

    # Initialize result matrix with zeros
    result = [[0 for _ in range(len(b[0]))] for _ in range(len(a))]

    # Matrix multiplication logic
    for i in range(len(a)):
        for j in range(len(b[0])):
            for k in range(len(b)):
                result[i][j] += a[i][k] * b[k][j]

    return result

```
