

```python
import numpy as np
```


```python
arr1 = np.array([[1,2,3],
                 [4,5,6]])
```


```python
arr2 = np.array([[1,1,2],
                 [2,3,3]])
print(arr1)
print(arr2)
```

    [[1 2 3]
     [4 5 6]]
    [[1 1 2]
     [2 3 3]]



```python
print(arr1 + arr2) #矩阵加法
```

    [[2 3 5]
     [6 8 9]]



```python
print(arr1 - arr2) #矩阵减法
```

    [[0 1 1]
     [2 2 3]]



```python
print(arr1 * arr2) #矩阵乘法
```

    [[ 1  2  6]
     [ 8 15 18]]



```python
print(arr1 ** arr2) #求arr1的arr2次幂（即求幂运算）
```

    [[  1   2   9]
     [ 16 125 216]]



```python
print(arr1 / arr2) #矩阵除法
```

    [[1.         2.         1.5       ]
     [2.         1.66666667 2.        ]]



```python
print(arr1 // arr2) #矩阵取整
```

    [[1 2 1]
     [2 1 2]]



```python
print(arr1 % arr2) #矩阵取余
```

    [[0 0 1]
     [0 2 0]]



```python
print(arr1 + 2) #所有数都加2
```

    [[3 4 5]
     [6 7 8]]



```python
print(arr1 ** 10) #所有数都进行10次幂运算
```

    [[       1     1024    59049]
     [ 1048576  9765625 60466176]]



```python
arr3 = arr1 > 3 #元素大小判断
print(arr3)
```

    [[False False False]
     [ True  True  True]]



```python
arr4 = np.ones((3,5))
print(arr4)
```

    [[1. 1. 1. 1. 1.]
     [1. 1. 1. 1. 1.]
     [1. 1. 1. 1. 1.]]



```python
print(arr1)
```

    [[1 2 3]
     [4 5 6]]



```python
np.dot(arr1, arr4) #矩阵点积，对一维数组是点积，对二维数组是矩阵积
np.dot([1,2,3,4,5], [5,4,3,2,1])
```




    35




```python
arr1.dot(arr4) #同上
```




    array([[ 6.,  6.,  6.,  6.,  6.],
           [15., 15., 15., 15., 15.]])




```python
print(arr1) #转置矩阵，方法有这三个
print(arr1.T)
print(arr1.transpose())
```

    [[1 2 3]
     [4 5 6]]
    [[1 4]
     [2 5]
     [3 6]]
    [[1 4]
     [2 5]
     [3 6]]



```python

```
