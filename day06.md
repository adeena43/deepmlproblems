```py
import numpy as np

def calculate_eigenvalues(matrix: list[list[float | int]]) -> list[float]:
    np_matrix = np.array(matrix)
    eigenvalues = np.linalg.eigvals(np_matrix)
    return eigenvalues.tolist()

```
