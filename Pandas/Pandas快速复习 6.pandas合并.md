

```python
import pandas as pd
import numpy as np
```


```python
df1 = pd.DataFrame(np.arange(12).reshape((3,4)), columns = ['A', 'B', 'C', 'D'])
df2 = pd.DataFrame(np.arange(12, 24).reshape((3,4)), columns = ['A', 'B', 'C', 'D'])
df3 = pd.DataFrame(np.arange(24, 36).reshape((3,4)), columns = ['A', 'B', 'C', 'D'])
print(df1)
print(df2)
print(df3)
```

       A  B   C   D
    0  0  1   2   3
    1  4  5   6   7
    2  8  9  10  11
        A   B   C   D
    0  12  13  14  15
    1  16  17  18  19
    2  20  21  22  23
        A   B   C   D
    0  24  25  26  27
    1  28  29  30  31
    2  32  33  34  35



```python
df4 = pd.concat([df1, df2, df3], axis = 0) #纵向合并
df4
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
    <tr>
      <th>0</th>
      <td>12</td>
      <td>13</td>
      <td>14</td>
      <td>15</td>
    </tr>
    <tr>
      <th>1</th>
      <td>16</td>
      <td>17</td>
      <td>18</td>
      <td>19</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
    </tr>
    <tr>
      <th>0</th>
      <td>24</td>
      <td>25</td>
      <td>26</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1</th>
      <td>28</td>
      <td>29</td>
      <td>30</td>
      <td>31</td>
    </tr>
    <tr>
      <th>2</th>
      <td>32</td>
      <td>33</td>
      <td>34</td>
      <td>35</td>
    </tr>
  </tbody>
</table>
</div>




```python
df4 = pd.concat([df1, df2, df3], axis = 0, ignore_index = True) #纵向合并，忽略原来的index
df4
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
    <tr>
      <th>3</th>
      <td>12</td>
      <td>13</td>
      <td>14</td>
      <td>15</td>
    </tr>
    <tr>
      <th>4</th>
      <td>16</td>
      <td>17</td>
      <td>18</td>
      <td>19</td>
    </tr>
    <tr>
      <th>5</th>
      <td>20</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
    </tr>
    <tr>
      <th>6</th>
      <td>24</td>
      <td>25</td>
      <td>26</td>
      <td>27</td>
    </tr>
    <tr>
      <th>7</th>
      <td>28</td>
      <td>29</td>
      <td>30</td>
      <td>31</td>
    </tr>
    <tr>
      <th>8</th>
      <td>32</td>
      <td>33</td>
      <td>34</td>
      <td>35</td>
    </tr>
  </tbody>
</table>
</div>




```python
df5 = pd.concat([df1, df2, df3], axis = 1)
df5
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>12</td>
      <td>13</td>
      <td>14</td>
      <td>15</td>
      <td>24</td>
      <td>25</td>
      <td>26</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
      <td>16</td>
      <td>17</td>
      <td>18</td>
      <td>19</td>
      <td>28</td>
      <td>29</td>
      <td>30</td>
      <td>31</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
      <td>20</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
      <td>32</td>
      <td>33</td>
      <td>34</td>
      <td>35</td>
    </tr>
  </tbody>
</table>
</div>




```python
df5 = pd.concat([df1, df2, df3], axis = 1, ignore_index = True)
df5
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
      <th>4</th>
      <th>5</th>
      <th>6</th>
      <th>7</th>
      <th>8</th>
      <th>9</th>
      <th>10</th>
      <th>11</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>12</td>
      <td>13</td>
      <td>14</td>
      <td>15</td>
      <td>24</td>
      <td>25</td>
      <td>26</td>
      <td>27</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
      <td>16</td>
      <td>17</td>
      <td>18</td>
      <td>19</td>
      <td>28</td>
      <td>29</td>
      <td>30</td>
      <td>31</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
      <td>20</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
      <td>32</td>
      <td>33</td>
      <td>34</td>
      <td>35</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1 = pd.DataFrame(np.arange(12).reshape((3,4)), columns = ['A', 'B', 'C', 'F'])
df2 = pd.DataFrame(np.arange(12, 24).reshape((3,4)), columns = ['A', 'C', 'D', 'E'])
print(df1)
print(df2)
```

       A  B   C   F
    0  0  1   2   3
    1  4  5   6   7
    2  8  9  10  11
        A   C   D   E
    0  12  13  14  15
    1  16  17  18  19
    2  20  21  22  23



```python
df6 = pd.concat([df1, df2], join = 'outer', ignore_index = True) #合并两个表，缺少的部分填充NaN
df6
```

    /home/honorwh/anaconda3/lib/python3.7/site-packages/ipykernel_launcher.py:1: FutureWarning: Sorting because non-concatenation axis is not aligned. A future version
    of pandas will change to not sort by default.
    
    To accept the future behavior, pass 'sort=False'.
    
    To retain the current behavior and silence the warning, pass 'sort=True'.
    
      """Entry point for launching an IPython kernel.





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
      <th>0</th>
      <td>0</td>
      <td>1.0</td>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>5.0</td>
      <td>6</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>9.0</td>
      <td>10</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>11.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>12</td>
      <td>NaN</td>
      <td>13</td>
      <td>14.0</td>
      <td>15.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>16</td>
      <td>NaN</td>
      <td>17</td>
      <td>18.0</td>
      <td>19.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>20</td>
      <td>NaN</td>
      <td>21</td>
      <td>22.0</td>
      <td>23.0</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df7 = pd.concat([df1, df2], join = 'inner', ignore_index = True) #合并两个表，缺少的部分去掉
df7
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
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>6</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>10</td>
    </tr>
    <tr>
      <th>3</th>
      <td>12</td>
      <td>13</td>
    </tr>
    <tr>
      <th>4</th>
      <td>16</td>
      <td>17</td>
    </tr>
    <tr>
      <th>5</th>
      <td>20</td>
      <td>21</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1 = pd.DataFrame(np.arange(12).reshape((3,4)), columns = ['A', 'B', 'C', 'D'])
df2 = pd.DataFrame(np.arange(12, 24).reshape((4, 3)), columns = ['A', 'B', 'C'])
print(df1)
print(df2)
```

       A  B   C   D
    0  0  1   2   3
    1  4  5   6   7
    2  8  9  10  11
        A   B   C
    0  12  13  14
    1  15  16  17
    2  18  19  20
    3  21  22  23



```python
df8 = pd.concat([df1, df2], axis = 1, join_axes = [df1.index]) #横向合并，index使用df1的index
df8
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>12</td>
      <td>13</td>
      <td>14</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
      <td>15</td>
      <td>16</td>
      <td>17</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
      <td>18</td>
      <td>19</td>
      <td>20</td>
    </tr>
  </tbody>
</table>
</div>




```python
df8 = pd.concat([df1, df2], axis = 1, join_axes = [df2.index]) #横向合并，index使用df2的index
df8
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>12</td>
      <td>13</td>
      <td>14</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.0</td>
      <td>5.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>15</td>
      <td>16</td>
      <td>17</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>11.0</td>
      <td>18</td>
      <td>19</td>
      <td>20</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
    </tr>
  </tbody>
</table>
</div>




```python
df8 = pd.concat([df1, df2], axis = 1) #直接横向合并
df8
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>12</td>
      <td>13</td>
      <td>14</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.0</td>
      <td>5.0</td>
      <td>6.0</td>
      <td>7.0</td>
      <td>15</td>
      <td>16</td>
      <td>17</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8.0</td>
      <td>9.0</td>
      <td>10.0</td>
      <td>11.0</td>
      <td>18</td>
      <td>19</td>
      <td>20</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>21</td>
      <td>22</td>
      <td>23</td>
    </tr>
  </tbody>
</table>
</div>


