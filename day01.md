```py
def matrix_dot_vector(a: list[list[int | float]], b: list[int | float]) -> list[int | float] | int:
    # Return a list where each element is the dot product of a row of 'a' with 'b'.
    # If the number of columns in 'a' does not match the length of 'b', return -1.
    
    if not a or len(b) != len(a[0]):
        return -1

    ans = []
    for row in a:
        res = 0
        for i in range(len(b)):
            res += row[i] * b[i]
        ans.append(res)
    
    return ans

```
