

```python
import numpy as np
```


```python
arr1 = np.arange(2,14)
print(arr1)
```

    [ 2  3  4  5  6  7  8  9 10 11 12 13]



```python
print(arr1[2])
```

    4



```python
#一维数组索引相对简单，直接对二维数组进行练习
```


```python
arr2 = arr1.reshape(3,4)
print(arr2)
```

    [[ 2  3  4  5]
     [ 6  7  8  9]
     [10 11 12 13]]



```python
print(arr2[1])
```

    [6 7 8 9]



```python
print(arr2[1][1]) #对二维的话，第一个参数表示行索引，第二个数表示列索引
```

    7



```python
print(arr2[1,1]) #同理
```

    7



```python
print(arr2[:, 2]) #冒号表示所有行索引
```

    [ 4  8 12]



```python
for i in arr2.T: #转置矩阵迭代
    print(i)
    
```

    [ 2  6 10]
    [ 3  7 11]
    [ 4  8 12]
    [ 5  9 13]



```python
for i in arr2.flat: #扁平化，一个一个元素迭代
    print(i)
```

    2
    3
    4
    5
    6
    7
    8
    9
    10
    11
    12
    13



```python

```
