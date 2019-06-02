

```python
import numpy as np
```


```python
a = np.array([1,2,3], dtype=np.int32)
print(a)
```

    [1 2 3]



```python
b = np.array([1,2,3], dtype = np.float)
print(a, a.dtype)
```

    [1 2 3] int32



```python
print(b, b.dtype)
```

    [1. 2. 3.] float64



```python
c = np.array([1,2,3]) #一维数组
```


```python
print(c)
```

    [1 2 3]



```python
d = np.array([[1,2,3],
              [4,5,6]]) #二维矩阵
print(d)
```

    [[1 2 3]
     [4 5 6]]



```python
zero = np.zeros((2,3)) #生成2行3列全为0的矩阵
print(zero)
```

    [[0. 0. 0.]
     [0. 0. 0.]]



```python
empty = np.empty((2,3)) #生成了2行3列的矩阵，看起来是0，但是接近于0（即不等于0），和np.zeros不同
print(empty)
```

    [[0. 0. 0.]
     [0. 0. 0.]]



```python
ones = np.ones((3,4)) #生成3行4列的全为1的矩阵
print(ones)
```

    [[1. 1. 1. 1.]
     [1. 1. 1. 1.]
     [1. 1. 1. 1.]]



```python
e = np.arange(10)
print(e)
```

    [0 1 2 3 4 5 6 7 8 9]



```python
f = np.arange(1,101)
print(f)
```

    [  1   2   3   4   5   6   7   8   9  10  11  12  13  14  15  16  17  18
      19  20  21  22  23  24  25  26  27  28  29  30  31  32  33  34  35  36
      37  38  39  40  41  42  43  44  45  46  47  48  49  50  51  52  53  54
      55  56  57  58  59  60  61  62  63  64  65  66  67  68  69  70  71  72
      73  74  75  76  77  78  79  80  81  82  83  84  85  86  87  88  89  90
      91  92  93  94  95  96  97  98  99 100]



```python
eye = np.eye(3) #生成对角线都是1的矩阵，即单位矩阵
print(eye)
```

    [[1. 0. 0.]
     [0. 1. 0.]
     [0. 0. 1.]]



```python
h = np.arange(8).reshape(4,2) #重新定义矩阵的形状
print(h)
```

    [[0 1]
     [2 3]
     [4 5]
     [6 7]]



```python

```
