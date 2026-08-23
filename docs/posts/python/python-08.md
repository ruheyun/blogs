# 字典

字典是另一种可变容器模型，且可存储任意类型对象。

字典的格式为 key: value (键值对)，每个键值对之间用逗号(,)分割，整个字典包括在花括号 {} 中

且 dict 是python中的关键字，不建议将变量命名为 dict


```python
dit = {'yuwen': 90, 'shuxue': 80, 'yingyu': 60}
print(dit)

# {'yuwen': 90, 'shuxue': 80, 'yingyu': 60}
```


```python
dit1 = dict()  # 定义一个空字典
print(dit1)

# {}
```
    


```python
dit2 = {}  # 定义一个空字典
print(dit2)

# {}
```
    

字典中键必须是唯一且不可变数据类型，值可以重复且可变


```python
dit3 = {'yuwen': 66, 'shuxue': 66}
print(dit3)

# {'yuwen': 66, 'shuxue': 66}
```


```python
dit4 = {'yuwen': 66, 'yuwen': 70}  # 在新版python中，当键重复时，取最后一个键所对应的键值对
print(dit4)

# {'yuwen': 70}
```
    


```python
dit5 = {[1]: 12}
print(dit5)

'''
---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[6], line 1
    ----> 1 dit5 = {[1]: 12}
          2 print(dit5)
    

    TypeError: cannot use 'list' as a dict key (unhashable type: 'list')
'''
```


```python
dit6 = {(1, 2): 12}  # 列表是可变数据类型，不能作为键，而元组是不可变数据类型
print(dit6)

# {(1, 2): 12}
```

