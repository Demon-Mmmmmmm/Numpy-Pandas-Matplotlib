

```python
import numpy as np
```


```python
arr1 = np.array([1,2,3])
```


```python
arr2 = arr1 #共享一块内存（指针指向同一块内存，就是浅拷贝）
```


```python
arr2[0] = 5
```


```python
print(arr1)
print(arr2)
```

    [5 2 3]
    [5 2 3]



```python
arr3 = arr1.copy() #深拷贝
```


```python
arr3[0] = 10
print(arr1)
print(arr3)
```

    [5 2 3]
    [10  2  3]



```python
arr4 = arr1[np.newaxis,:]
print(arr4,arr4.shape)
```

    [[5 2 3]] (1, 3)



```python
arr4[0]
```




    array([5, 2, 3])




```python
arr5 = arr4
```


```python
arr5[0] = 199
```


```python
print(arr5)
print(arr4)
```

    [[199 199 199]]
    [[199 199 199]]



```python
arr5[0][0] = 10
```


```python
print(arr5)
print(arr4)
```

    [[ 10 199 199]]
    [[ 10 199 199]]



```python
arr5 = arr4.copy()
```


```python
print(arr5)
print(arr4)
```

    [[ 10 199 199]]
    [[ 10 199 199]]



```python
arr5[0][0] = 100
```


```python
print(arr5)
print(arr4)
```

    [[100 199 199]]
    [[ 10 199 199]]



```python

```
