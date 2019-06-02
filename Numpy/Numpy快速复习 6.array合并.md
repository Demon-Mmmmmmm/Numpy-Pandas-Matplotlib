

```python
import numpy as np

```


```python
arr1 = np.array([1,2,3])
arr2 = np.array([4,5,6])
arr3 = np.vstack((arr1, arr2)) #垂直合并
print(arr3)
```

    [[1 2 3]
     [4 5 6]]



```python
arr4 = np.hstack((arr1, arr2)) #水平合并
print(arr4)
```

    [1 2 3 4 5 6]



```python
np.vstack((arr1, arr2, arr3))
```




    array([[1, 2, 3],
           [4, 5, 6],
           [1, 2, 3],
           [4, 5, 6]])




```python
arr = np.concatenate((arr3, arr3),axis = 0) #竖着合并（垂直合并），要维数一样,还有一维数组不能转置
print(arr)
```

    [[1 2 3]
     [4 5 6]
     [1 2 3]
     [4 5 6]]



```python
arr = np.concatenate((arr3, arr3),axis = 1) #横着合并（水平合并）
print(arr)
```

    [[1 2 3 1 2 3]
     [4 5 6 4 5 6]]



```python
print(arr1.T)
```

    [1 2 3]



```python
arr1_1 = arr1[np.newaxis, :] #新增维度，一维变二维，注意加在行还是列
print(arr1_1.shape)
print(arr1_1)
print(arr1_1.T)
```

    (1, 3)
    [[1 2 3]]
    [[1]
     [2]
     [3]]



```python
arr1_2 = arr1[:, np.newaxis] #新增维度，一维变二维，注意加在行还是列
print(arr1_2)
print(arr1_2.shape)
print(arr1_2.T)
```

    [[1]
     [2]
     [3]]
    (3, 1)
    [[1 2 3]]



```python
arr1_3 = np.atleast_2d(arr1) #至少二维
print(arr1_3)
print(arr1_3.shape)
print(arr1_3.T)
```

    [[1 2 3]]
    (1, 3)
    [[1]
     [2]
     [3]]



```python
print(arr1.shape) #一维
print(arr1_1.shape) #二维
arr1_3 = np.atleast_3d(arr1) #至少三维
print(arr1_3.shape)
print(arr1_3)
```

    (3,)
    (1, 3)
    (1, 3, 1)
    [[[1]
      [2]
      [3]]]

