```py
import numpy as np

def reshape_matrix(a: list[list[int | float]], new_shape: tuple[int, int]) -> list[list[int | float]]:
    original_elements = sum(len(row) for row in a)
    new_elements = new_shape[0] * new_shape[1]

    if original_elements != new_elements:
        return []

    array = np.array(a)
    reshaped_array = array.reshape(new_shape)
    return reshaped_array.tolist()
```
