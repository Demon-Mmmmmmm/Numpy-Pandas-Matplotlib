

```python
import pandas as pd
import numpy as np
```


```python
dates = np.arange(20190101, 20190105)
df1 = pd.DataFrame(np.arange(12).reshape((4,3)), index = dates, columns = ['A','B','C'])
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>3</td>
      <td>4</td>
      <td>5</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>6</td>
      <td>7</td>
      <td>8</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2 = pd.DataFrame(df1, index = dates, columns = ['A','B','C','D','E'])
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>6</td>
      <td>7</td>
      <td>8</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>9</td>
      <td>10</td>
      <td>11</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
s1 = pd.Series([3,4,6], index = dates[:3])
s2 = pd.Series([32,4,5], index = dates[1:])
df2['D'] = s1
df2['E'] = s2
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>4.0</td>
      <td>32.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>6</td>
      <td>7</td>
      <td>8</td>
      <td>6.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>9</td>
      <td>10</td>
      <td>11</td>
      <td>NaN</td>
      <td>5.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.dropna(axis = 0, how = 'any') #axis=[0,1] 0代表行，1代表列；how = ['any', 'all'] any是任意一个或多个，all是全部
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190102</th>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>4.0</td>
      <td>32.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>6</td>
      <td>7</td>
      <td>8</td>
      <td>6.0</td>
      <td>4.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.dropna(axis = 1, how = 'any') #axis=[0,1] 0代表行，1代表列；how = ['any', 'all'] any是任意一个或多个，all是全部
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>3</td>
      <td>4</td>
      <td>5</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>6</td>
      <td>7</td>
      <td>8</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.fillna(value=0) #把表中空值赋值为一个数
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>4.0</td>
      <td>32.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>6</td>
      <td>7</td>
      <td>8</td>
      <td>6.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>9</td>
      <td>10</td>
      <td>11</td>
      <td>0.0</td>
      <td>5.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.isnull() #True即为空值，False即为非空值
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
np.any(df2.isnull()) #只要有一个值是空值就会返回True
```




    True




```python
np.all(df2.isnull()) #所有值都是空值才会返回True，否则返回False
```




    False


