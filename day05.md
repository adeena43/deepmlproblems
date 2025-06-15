```py
def scalar_multiply(matrix: list[list[int | float]], scalar: int | float) -> list[list[int | float]]:
    result = []
    for row in matrix:
        new_row = []
        for element in row:
            new_row.append(scalar * element)
        result.append(new_row)
    return result

```
