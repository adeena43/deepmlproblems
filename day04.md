```py
def calculate_matrix_mean(matrix: list[list[float]], mode: str) -> list[float]:
    if not matrix:
        return []

    if mode == "row":
        means = []
        for row in matrix:
            mean = sum(row) / len(row)
            means.append(mean)
        return means

    elif mode == "column":
        num_cols = len(matrix[0])
        means = []
        for col in range(num_cols):
            col_sum = sum(row[col] for row in matrix)
            means.append(col_sum / len(matrix))
        return means

    else:
        raise ValueError("Mode must be either 'row' or 'column'")

```
