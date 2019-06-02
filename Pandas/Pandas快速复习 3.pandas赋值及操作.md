

```python
import pandas as pd
import numpy as np
```


```python
dates = np.arange(20190101, 20190107)
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
      <th>20190101</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>12</td>
      <td>13</td>
      <td>14</td>
      <td>15</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>16</td>
      <td>17</td>
      <td>18</td>
      <td>19</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>20</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.iloc[2,3]
```




    11




```python
df1.iloc[2,3] = 100
```


```python
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
      <th>20190101</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>100</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>12</td>
      <td>13</td>
      <td>14</td>
      <td>15</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>16</td>
      <td>17</td>
      <td>18</td>
      <td>19</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>20</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.loc[20190102, 'B'] = 200
```


```python
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
      <th>20190101</th>
      <td>0.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>12.0</td>
      <td>13.0</td>
      <td>14.0</td>
      <td>15.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>16.0</td>
      <td>17.0</td>
      <td>18.0</td>
      <td>19.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>20.0</td>
      <td>21.0</td>
      <td>22.0</td>
      <td>23.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1[df1.A > 10] = 1
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
      <th>20190101</th>
      <td>0.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.A[df1.A == 0] = 1
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
      <th>20190101</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1['E'] = 10 #添加一列
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
      <th>E</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>10</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>10</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1['F'] = pd.Series([1,2,3,4,5,6], index = dates)
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
      <th>E</th>
      <th>F</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>10</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>10</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.loc[20190108, ['A', 'B', 'C']] = [1,2,3]
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
      <th>E</th>
      <th>F</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>10.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>10.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190108</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
s1 = pd.Series([1,2,3,4,5,6], index = ['A', 'V', 'C', 'D', 'E', 'F'])
s1.name = 'S1'
df2 = df1.append(s1)
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
      <th>F</th>
      <th>V</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>10.0</td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>10.0</td>
      <td>2.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>4.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>5.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>6.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190108</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>S1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>3.0</td>
      <td>4.0</td>
      <td>5.0</td>
      <td>6.0</td>
      <td>2.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.insert(1, 'G', df2['E']) #在第一列插入索引为G的df2中的E列
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
      <th>G</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
      <th>F</th>
      <th>V</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>1.0</td>
      <td>10.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>10.0</td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>10.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>10.0</td>
      <td>2.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>10.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>10.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>4.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>10.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>5.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>10.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>6.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>10.0</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190108</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>S1</th>
      <td>1.0</td>
      <td>5.0</td>
      <td>NaN</td>
      <td>3.0</td>
      <td>4.0</td>
      <td>5.0</td>
      <td>6.0</td>
      <td>2.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
g = df2.pop('G') #弹出G列
```


```python
df1.insert(6, 'G', g) #插入到最后
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
      <th>E</th>
      <th>F</th>
      <th>G</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>10.0</td>
      <td>1.0</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>10.0</td>
      <td>2.0</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>3.0</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>4.0</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>5.0</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>6.0</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10.0</td>
      <td>NaN</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>20190108</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
del df1['G'] #删除G
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
      <th>E</th>
      <th>F</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>10.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>10.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190108</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2 = df1.drop(['A', 'B'], axis = 1) #删除列
```


```python
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
      <th>E</th>
      <th>F</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>10.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>10.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190108</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




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
      <th>C</th>
      <th>D</th>
      <th>E</th>
      <th>F</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>2.0</td>
      <td>3.0</td>
      <td>10.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>6.0</td>
      <td>7.0</td>
      <td>10.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>10.0</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>10.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190108</th>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2 = df1.drop([20190101,20190102], axis = 0) #删除行
```


```python
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
      <th>E</th>
      <th>F</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190101</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>10.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>4.0</td>
      <td>200.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>10.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190108</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
      <th>F</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20190103</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>100.0</td>
      <td>10.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>20190104</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>20190105</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>20190106</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>10.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>20190102</th>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>10.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20190108</th>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
