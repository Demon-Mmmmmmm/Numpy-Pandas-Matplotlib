

```python
import pandas as pd
import numpy as np
```


```python
file = pd.read_csv('投递公司及职位.csv', encoding = 'utf-8')
```


```python
file
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
file.iloc[2,0] = '艾瑞'
```


```python
file
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
file.iloc[2,0] = '艾瑞集团'
```


```python
file
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
file.fillna(value = '等待中')
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
  </tbody>
</table>
</div>




```python
file = file.fillna(value='等待中') #运用上节课的补充丢失数据的方法，fillna
file
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
  </tbody>
</table>
</div>




```python
file.to_csv('temp.csv') #保存文件为什么格式， to_csv等等
```


```python
file
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
  </tbody>
</table>
</div>




```python
file.values[4:6, 5] = ['Over']
file
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
  </tbody>
</table>
</div>




```python
file.to_csv('temp.csv') #保存文件为什么格式， to_csv等等
```


```python
file
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
  </tbody>
</table>
</div>




```python
file
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
  </tbody>
</table>
</div>




```python
file.insert(5,'状态',file.values[:,5])
file
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-42-72b5ac244937> in <module>
    ----> 1 file.insert(5,'状态',file.values[:,5])
          2 file


    ~/anaconda3/lib/python3.7/site-packages/pandas/core/frame.py in insert(self, loc, column, value, allow_duplicates)
       3220         value = self._sanitize_column(column, value, broadcast=False)
       3221         self._data.insert(loc, column, value,
    -> 3222                           allow_duplicates=allow_duplicates)
       3223 
       3224     def assign(self, **kwargs):


    ~/anaconda3/lib/python3.7/site-packages/pandas/core/internals.py in insert(self, loc, item, value, allow_duplicates)
       4336         if not allow_duplicates and item in self.items:
       4337             # Should this be a different kind of error??
    -> 4338             raise ValueError('cannot insert {}, already exists'.format(item))
       4339 
       4340         if not isinstance(loc, int):


    ValueError: cannot insert 状态, already exists



```python
file
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>状态</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
  </tbody>
</table>
</div>




```python
s1 = pd.Series(['深声科技', 'NLP算法实习生', '2019/5/29', '实习僧', '等待中', '等待中', '等待中'], index = ['投递公司', '职位', '投递日期', '投递平台', '有无面试机会', '状态', '面试结果'])
s1.name = '16'
```


```python
s2 = pd.Series(['广发证券', '自然语言处理工程师', '2019/5/29', '实习僧', '等待中', '等待中', '等待中'], index = ['投递公司', '职位', '投递日期', '投递平台', '有无面试机会', '状态', '面试结果'])
s2.name = '17'
```


```python
temp = file.append(s2)
```


```python
temp
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
      <th>投递公司</th>
      <th>职位</th>
      <th>投递日期</th>
      <th>投递平台</th>
      <th>有无面试机会</th>
      <th>状态</th>
      <th>面试结果</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>虎牙</td>
      <td>数据分析师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>1</th>
      <td>虎牙</td>
      <td>数据分析师（商业分析方向）</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>2</th>
      <td>艾瑞集团</td>
      <td>数据分析实习生</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>3</th>
      <td>火烈鸟网络</td>
      <td>数据挖掘工程师</td>
      <td>2019/5/19</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>4</th>
      <td>小黑屋</td>
      <td>数据分析师</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>5</th>
      <td>小黑屋</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>实习僧</td>
      <td>时间不合适</td>
      <td>Over</td>
      <td>Over</td>
    </tr>
    <tr>
      <th>6</th>
      <td>广州泰迪智能科技</td>
      <td>数据分析实习生</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>有面试机会</td>
      <td>已面试</td>
      <td>已面试</td>
    </tr>
    <tr>
      <th>7</th>
      <td>头文科技</td>
      <td>NLP实习</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>8</th>
      <td>小鹏汽车</td>
      <td>自然语言处理开发实习生</td>
      <td>2019/5/20   2019/5/25</td>
      <td>BOSS、拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>9</th>
      <td>元游信息</td>
      <td>python后台开发</td>
      <td>2019/5/20</td>
      <td>BOSS</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>10</th>
      <td>字节跳动</td>
      <td>后端开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>11</th>
      <td>搜狐</td>
      <td>python开发实习生</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>12</th>
      <td>荔枝</td>
      <td>机器学习算法实习</td>
      <td>2019/5/25</td>
      <td>拉勾招聘</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>13</th>
      <td>触宝</td>
      <td>python后端开发工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>14</th>
      <td>小鹏汽车</td>
      <td>数据分析实习生</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>15</th>
      <td>诚毅软件</td>
      <td>python工程师</td>
      <td>2019/5/28</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
    <tr>
      <th>17</th>
      <td>广发证券</td>
      <td>自然语言处理工程师</td>
      <td>2019/5/29</td>
      <td>实习僧</td>
      <td>等待中</td>
      <td>等待中</td>
      <td>等待中</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
