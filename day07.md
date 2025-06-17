```py
def inverse_2x2(matrix: list[list[float]]) -> list[list[float]] | None:
    if len(matrix) != 2 or len(matrix[0]) != 2 or len(matrix[1]) != 2:
        return None  # Not a 2x2 matrix
    
    a, b = matrix[0]
    c, d = matrix[1]
    
    determinant = a * d - b * c
    if determinant == 0:
        return None  # Not invertible
    
    inverse = [
        [d / determinant, -b / determinant],
        [-c / determinant, a / determinant]
    ]
    
    return inverse

```
