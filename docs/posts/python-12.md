# 推导式

推导式是一种强大且简洁的语法，适用于生成列表、字典、集合和生成器。

共有四种推导式（前面有介绍过）：
1. 列表(list)推导式
2. 字典(dict)推导式
3. 集合(set)推导式
4. 元组(tuple)推导式

例子：创建一个列表/集合/元组，共有10个元素，从1到10.


```python
lst1 = [i for i in range(1, 11)]
print(lst1)

# [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

    
    


```python
set1 = {i for i in range(1, 11)}
print(set1)

# {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
```

    
    


```python
tuple1 = (i for i in range(1, 11))  # 注意元组推导式生成的是一个生成器对象，需要多一步转化
print(tuple1)

# <generator object <genexpr> at 0x000001C8EC6C1E50>
```

    
    


```python
print(tuple(tuple1))

# (1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
```

    
    

例子：创建一个列表/集合/元组，共有5个元素，从1到11之间的偶数.


```python
lst2 = [i for i in range(1, 11) if i % 2 == 0]
print(lst2)

# [2, 4, 6, 8, 10]
```

    
    


```python
set2 = {i for i in range(1, 11) if i % 2 == 0}
print(set2)

# {2, 4, 6, 8, 10}
```

    
    


```python
tuple2 = (i for i in range(1, 11) if i % 2 == 0)
print(tuple(tuple2))

# (2, 4, 6, 8, 10)
```

    
    

例子：创建一个字典，共有5个元素，从1到10，奇数为键，偶数为值，比如{1：2}.


```python
dict1 = {i: i + 1 for i in range(1, 11, 2)}
print(dict1)

# {1: 2, 3: 4, 5: 6, 7: 8, 9: 10}
```

    
    

例子：创建一个字典，从1到10，奇数为键，偶数为值，比如{1：2}，要求键不能为5.


```python
dict2 = {i: i + 1 for i in range(1, 11, 2) if i != 5}
print(dict2)

# {1: 2, 3: 4, 7: 8, 9: 10}
```
