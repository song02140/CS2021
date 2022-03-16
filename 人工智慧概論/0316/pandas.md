
# Pandas
在計算機編程中，pandas是Python程式語言的用於數據操縱和分析的軟體庫。
### 導入pands
```python
import pandas as pd
```
### 導入Series和DataFrame
```python
from pandas import Series, DataFrame
```
## 1 Series 的運算
### series是一個類似陣列的物件。
### 用pd.series()創建一個series： 
```python
obj = pd.Series([4, 7, -5, 3])
obj
```
#### 左側為索引(index),右側為值(value)
```
0    4
1    7
2   -5
3    3
dtype: int64
```

### 通過.value和.index屬性查看：
```python
obj.values
```
array([ 4,  7, -5,  3])
```python
obj.index
```
RangeIndex(start=0, stop=4, step=1)
### 指定index的標籤(label)：
```python
obj2 = pd.Series([4, 7, -5, 3], index=['d', 'b', 'a', 'c'])
obj2
```
```
d    4
b    7
a   -5
c    3
dtype: int64
```
```python
obj2.index
```
Index(['d', 'b', 'a', 'c'], dtype='object')
### 透過index搜尋
```python
obj2['a']
```
-5  
```python
obj2[['c', 'a', 'd']]
```
```
c    3
a   -5
d    6
dtype: int64
```
### 透過index設定
```pythoon
obj2['d'] = 6
```
```python
obj2[['c', 'a', 'd']]
```
```
c    3
a   -5
d    6
dtype: int64
```
### 其他運算
#### 只顯示值(value)>0
```python
obj2[obj2 > 0]
```
```
d    6
b    7
c    3
dtype: int64
```
#### 將值(value)*2
```python
obj2 * 2
```
```
d    12
b    14
a   -10
c     6
dtype: int64
```
```python
import numpy as np
np.exp(obj2)
```
```
d     403.428793
b    1096.633158
a       0.006738
c      20.085537
dtype: float64
```
### 利用dict來創建series
```python
sdata = {'Ohio': 35000, 'Texas': 71000, 'Oregon':16000, 'Utah': 5000}

obj3 = pd.Series(sdata)
obj3
```
```
Ohio      35000
Oregon    16000
Texas     71000
Utah       5000
dtype: int64
```
#### 也可以利用dict來排列，順序是按照states，但因為並沒有在sdata找到'California'，所以為NaN，表示數據缺失
```python
states = ['California', 'Ohio', 'Oregon', 'Texas']

obj4 = pd.Series(sdata, index=states)
obj4
```
```
California        NaN
Ohio          35000.0
Oregon        16000.0
Texas         71000.0
dtype: float64
```

### 使用pandas的isnull和notnull函數檢測MISSING Value(缺失資料)
#### pd.isnull(obj4)，檢測是否有資料缺失，若資料缺失，則顯示True
```python
pd.isnull(obj4)
```
```
California     True
Ohio          False
Oregon        False
Texas         False
dtype: bool
```
```python
pd.notnull(obj4)
```
```python
obj4.isnull()
```
```python

```
```python

```










