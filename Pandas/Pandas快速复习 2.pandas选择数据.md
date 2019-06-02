

```python
import pandas as pd
import numpy as np
```


```python
dates = pd.date_range('20190101', periods = 6)
df1 = pd.DataFrame(np.arange(24).reshape((6,4)), index = dates, columns = ['A','B','C','D'])
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
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2019-01-01</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2019-01-02</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>2019-01-03</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <th>2019-01-04</th>
      <td>12</td>
      <td>13</td>
      <td>14</td>
      <td>15</td>
    </tr>
    <tr>
      <th>2019-01-05</th>
      <td>16</td>
      <td>17</td>
      <td>18</td>
      <td>19</td>
    </tr>
    <tr>
      <th>2019-01-06</th>
      <td>20</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1['A'] #将DataFrame的列获取为一个Series
```




    2019-01-01     0
    2019-01-02     4
    2019-01-03     8
    2019-01-04    12
    2019-01-05    16
    2019-01-06    20
    Freq: D, Name: A, dtype: int64




```python
df1.A
```




    2019-01-01     0
    2019-01-02     4
    2019-01-03     8
    2019-01-04    12
    2019-01-05    16
    2019-01-06    20
    Freq: D, Name: A, dtype: int64




```python
df1[0:2]
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
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2019-01-01</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2019-01-02</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>




```python
#通过标签选择数据
df1.loc['20190101']
```




    A    0
    B    1
    C    2
    D    3
    Name: 2019-01-01 00:00:00, dtype: int64




```python
df1.loc['20190101', ['A', 'C']]
```




    A    0
    C    2
    Name: 2019-01-01 00:00:00, dtype: int64




```python
df1.loc[:, ['A','B']]
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
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2019-01-01</th>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2019-01-02</th>
      <td>4</td>
      <td>5</td>
    </tr>
    <tr>
      <th>2019-01-03</th>
      <td>8</td>
      <td>9</td>
    </tr>
    <tr>
      <th>2019-01-04</th>
      <td>12</td>
      <td>13</td>
    </tr>
    <tr>
      <th>2019-01-05</th>
      <td>16</td>
      <td>17</td>
    </tr>
    <tr>
      <th>2019-01-06</th>
      <td>20</td>
      <td>21</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.iloc[2] #通过位置选择数据,第三行
```




    A     8
    B     9
    C    10
    D    11
    Name: 2019-01-03 00:00:00, dtype: int64




```python
df1.iloc[1:3, 2:4]
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
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2019-01-02</th>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>2019-01-03</th>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.iloc[[1,2,4], [1,3]]
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
      <th>B</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2019-01-02</th>
      <td>5</td>
      <td>7</td>
    </tr>
    <tr>
      <th>2019-01-03</th>
      <td>9</td>
      <td>11</td>
    </tr>
    <tr>
      <th>2019-01-05</th>
      <td>17</td>
      <td>19</td>
    </tr>
  </tbody>
</table>
</div>




```python
#混合标签位置选择
df1.ix[2:4, ['A','C']] #DeprecationWarning：.ix已弃用。请用.loc用于基于标签的索引或.iloc用于位置索引
```

    /home/honorwh/anaconda3/lib/python3.7/site-packages/ipykernel_launcher.py:2: DeprecationWarning: 
    .ix is deprecated. Please use
    .loc for label based indexing or
    .iloc for positional indexing
    
    See the documentation here:
    http://pandas.pydata.org/pandas-docs/stable/indexing.html#ix-indexer-is-deprecated
      





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
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2019-01-03</th>
      <td>8</td>
      <td>10</td>
    </tr>
    <tr>
      <th>2019-01-04</th>
      <td>12</td>
      <td>14</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.A
```




    2019-01-01     0
    2019-01-02     4
    2019-01-03     8
    2019-01-04    12
    2019-01-05    16
    2019-01-06    20
    Freq: D, Name: A, dtype: int64




```python
df1.A >5
```




    2019-01-01    False
    2019-01-02    False
    2019-01-03     True
    2019-01-04     True
    2019-01-05     True
    2019-01-06     True
    Freq: D, Name: A, dtype: bool




```python
df1.C >10
```




    2019-01-01    False
    2019-01-02    False
    2019-01-03    False
    2019-01-04     True
    2019-01-05     True
    2019-01-06     True
    Freq: D, Name: C, dtype: bool




```python
df1.C
```




    2019-01-01     2
    2019-01-02     6
    2019-01-03    10
    2019-01-04    14
    2019-01-05    18
    2019-01-06    22
    Freq: D, Name: C, dtype: int64




```python
df1[df1.A > 6]
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
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2019-01-03</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <th>2019-01-04</th>
      <td>12</td>
      <td>13</td>
      <td>14</td>
      <td>15</td>
    </tr>
    <tr>
      <th>2019-01-05</th>
      <td>16</td>
      <td>17</td>
      <td>18</td>
      <td>19</td>
    </tr>
    <tr>
      <th>2019-01-06</th>
      <td>20</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
    </tr>
  </tbody>
</table>
</div>


