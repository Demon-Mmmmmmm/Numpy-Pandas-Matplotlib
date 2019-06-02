

```python
import pandas as pd
import numpy as np
```


```python
s1 = pd.Series([4,7,-5,3]) #创建一个series,索引为默认值
print(s1)
```

    0    4
    1    7
    2   -5
    3    3
    dtype: int64



```python
s1.values
```




    array([ 4,  7, -5,  3])




```python
s1.index
```




    RangeIndex(start=0, stop=4, step=1)




```python
s2 = pd.Series([4,56,5,3,2], index = ['a', 'b','c','d','e'])
```


```python
print(s2)
```

    a     4
    b    56
    c     5
    d     3
    e     2
    dtype: int64



```python
s2.value_counts
```




    <bound method IndexOpsMixin.value_counts of a     4
    b    56
    c     5
    d     3
    e     2
    dtype: int64>




```python
s2.values
```




    array([ 4, 56,  5,  3,  2])




```python
#Series可以看成一个定长的有序字典
dic1 = {'apple':5, 'pen':3, 'applepen':10}
s3 = pd.Series(dic1)
print(s3)
```

    apple        5
    pen          3
    applepen    10
    dtype: int64



```python
#DataFrame
data = {'year':[2016,2017,2018,2019],
        'income':[10000,20000,30000,40000],
        'pay':[5000,20000,3000,300000]
       }
df1 = pd.DataFrame(data)
df1
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>year</th>
      <th>income</th>
      <th>pay</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2016</td>
      <td>10000</td>
      <td>5000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2017</td>
      <td>20000</td>
      <td>20000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2018</td>
      <td>30000</td>
      <td>3000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2019</td>
      <td>40000</td>
      <td>300000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2 = pd.DataFrame(np.arange(12).reshape((3,4)))
```


```python
df2
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3 = pd.DataFrame(np.arange(12).reshape((3,4)), index = ['a', 'b', 'c'], columns = [2,3,4,5])
df3
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>b</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>c</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3.index
```




    Index(['a', 'b', 'c'], dtype='object')




```python
df3.values
```




    array([[ 0,  1,  2,  3],
           [ 4,  5,  6,  7],
           [ 8,  9, 10, 11]])




```python
df3.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>3.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>4.0</td>
      <td>5.0</td>
      <td>6.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>std</th>
      <td>4.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2.0</td>
      <td>3.0</td>
      <td>4.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>4.0</td>
      <td>5.0</td>
      <td>6.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>6.0</td>
      <td>7.0</td>
      <td>8.0</td>
      <td>9.0</td>
    </tr>
    <tr>
      <th>max</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>11.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.T
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>year</th>
      <td>2016</td>
      <td>2017</td>
      <td>2018</td>
      <td>2019</td>
    </tr>
    <tr>
      <th>income</th>
      <td>10000</td>
      <td>20000</td>
      <td>30000</td>
      <td>40000</td>
    </tr>
    <tr>
      <th>pay</th>
      <td>5000</td>
      <td>20000</td>
      <td>3000</td>
      <td>300000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>year</th>
      <th>income</th>
      <th>pay</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>4.000000</td>
      <td>4.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2017.500000</td>
      <td>25000.000000</td>
      <td>82000.000000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>1.290994</td>
      <td>12909.944487</td>
      <td>145531.210856</td>
    </tr>
    <tr>
      <th>min</th>
      <td>2016.000000</td>
      <td>10000.000000</td>
      <td>3000.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2016.750000</td>
      <td>17500.000000</td>
      <td>4500.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>2017.500000</td>
      <td>25000.000000</td>
      <td>12500.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2018.250000</td>
      <td>32500.000000</td>
      <td>90000.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2019.000000</td>
      <td>40000.000000</td>
      <td>300000.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3.sort_index(axis = 0) #行排序
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>b</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>c</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3.sort_index(axis = 1) #列排序
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>b</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>c</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3.sort_values(by = 3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>b</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>c</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
#总体来说，Series相当于数组numpy.array类似，有默认索引或者自定义索引；DataFrame相当于有表格，有行表头和列表头
```
