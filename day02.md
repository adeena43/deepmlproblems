```py
a = [[1,2,3],[4,5,6]]
b = []

for i in range(len(a[0])):
    new_row = []
    for j in range(len(a)):
        new_row.append(a[j][i])
    b.append(new_row)
print(b)
```
