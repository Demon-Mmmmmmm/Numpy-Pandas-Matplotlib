

```python
import numpy as np
```


```python
sample1 = np.random.random(size = (3,2)) #生成3行2列从0到1的随机数
print(sample1)
```

    [[0.12715908 0.15259947]
     [0.8841623  0.88178362]
     [0.44408856 0.06004783]]



```python
sample2 = np.random.normal(size = (3,2)) #生成3行2列符合标准正态分布的随机数
print(sample2)
```

    [[-2.30350386  0.47466623]
     [ 0.1493125  -0.65405791]
     [-1.04687874 -0.18171339]]



```python
sample3 = np.random.randint(0, 10, size = (3,2)) #生成3行2列从0到10的随机整数，区间值包前不包后
print(sample3)
```

    [[4 1]
     [3 1]
     [0 0]]



```python
np.sum(sample1) #求和计算
```




    2.5498408570793183




```python
np.min(sample1) #求最小值
```




    0.06004783041066819




```python
np.max(sample1) #求最大值
```




    0.8841622972960099




```python
np.sum(sample3, axis = 1) #跨列求和（横着求和），axis叫做轴
```




    array([5, 4, 0])




```python
np.sum(sample3, axis = 0) #跨行求和（竖着求和）
```




    array([7, 2])




```python
np.argmin(sample3) #求最小值的索引,如果有多个最小值，取的是第一个
```




    4




```python
np.argmax(sample3) #求最大值的索引
```




    0




```python
print(np.mean(sample3)) #求平均值的两种方法
print(sample3.mean())
```

    1.5
    1.5



```python
np.median(sample3) #求中位数，个数为双会取中间两个值的平均值
```




    1.0




```python
np.sqrt(sample3) #开方
```




    array([[2.        , 1.        ],
           [1.73205081, 1.        ],
           [0.        , 0.        ]])




```python
sample4 = np.random.randint(0, 10, size = (1,10)) #随机生成1行10列的数
print(sample4)
```

    [[1 6 7 3 2 7 8 6 3 5]]



```python
np.sort(sample4) #排序
```




    array([[1, 2, 3, 3, 5, 6, 6, 7, 7, 8]])




```python
print(sample3)
print(sample3.mean())
np.std(sample3) #标准差
```

    [[4 1]
     [3 1]
     [0 0]]
    1.5





    1.5




```python
np.square(sample3) #平方
```




    array([[16,  1],
           [ 9,  1],
           [ 0,  0]])




```python
np.var(sample3) #方差
```




    2.25




```python
np.clip(sample4, 2,6) #小于2变成2，大于6变为6
```




    array([[2, 6, 6, 3, 2, 6, 6, 6, 3, 5]])




```python
sample5 = np.array([[1,2], [3,4]])
sample6 = np.array([[5,6], [7,8]])
```


```python
np.cumsum(sample6) #累积状态和
```




    array([ 5, 11, 18, 26])




```python
print(sample5)
```

    [[1 2]
     [3 4]]

