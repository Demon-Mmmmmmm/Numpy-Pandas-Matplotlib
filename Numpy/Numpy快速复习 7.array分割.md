

```python
import numpy as np
```


```python
arr1 = np.arange(12).reshape((3,4))
print(arr1)
```

    [[ 0  1  2  3]
     [ 4  5  6  7]
     [ 8  9 10 11]]



```python
arr2, arr3 = np.split(arr1, 2, axis = 1)
print(arr2)
print(arr3)
```

    [[0 1]
     [4 5]
     [8 9]]
    [[ 2  3]
     [ 6  7]
     [10 11]]



```python
arr4, arr5, arr6 = np.split(arr1, 3, axis = 0)
print(arr4)
print(arr5)
print(arr6)
```

    [[0 1 2 3]]
    [[4 5 6 7]]
    [[ 8  9 10 11]]



```python
arr2, arr3, arr4, arr5 = np.split(arr1, 4, axis = 1) #等分切割
print(arr2)
print(arr3)
```

    [[0]
     [4]
     [8]]
    [[1]
     [5]
     [9]]



```python
arr7,arr8,arr9 = np.array_split(arr1, 3, axis = 1) #不等分割
print(arr7)
print(arr8)
print(arr9)
```

    [[0 1]
     [4 5]
     [8 9]]
    [[ 2]
     [ 6]
     [10]]
    [[ 3]
     [ 7]
     [11]]



```python
arrv1, arrv2, arrv3 = np.vsplit(arr1, 3) #垂直分割（竖着分割），等分
print(arrv1)
print(arrv2)
print(arrv3)
```

    [[0 1 2 3]]
    [[4 5 6 7]]
    [[ 8  9 10 11]]



```python
arrh1, arrh2 = np.hsplit(arr1, 2) #水平分割（横着分割），等分
print(arrh1)
print(arrh2)
```

    [[0 1]
     [4 5]
     [8 9]]
    [[ 2  3]
     [ 6  7]
     [10 11]]



```python

```
