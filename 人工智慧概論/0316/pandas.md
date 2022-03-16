
# Pandas
在計算機編程中，pandas是Python程式語言的用於數據操縱和分析的軟體庫。
## 導入pands
```python
import pandas as pd
```
## 可以導入Series和DataFrame，因為這兩個經常被用到
```python
from pandas import Series, DataFrame
```
## 1 Series 
### series是一個類似陣列的物件。
#### 創建一個series： 
```python
obj = pd.Series([4, 7, -5, 3])
obj
```
```
0    4
1    7
2   -5
3    3
dtype: int64
```
#### 左邊表示索引(index)，右邊表示對應的值(value)。可以通過value和index屬性查看：
```python
obj.values
```
array([ 4,  7, -5,  3])
```python
obj.index
```
RangeIndex(start=0, stop=4, step=1)
#### 當然我們也可以自己指定index的標籤(label)：
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
```python

```
```python

```
