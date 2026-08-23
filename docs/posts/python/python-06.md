# 列表

列表是最常用的 Python 数据类型，它可以作为一个方括号内的逗号分隔值出现。

列表的数据项不需要具有相同的类型


```python
lst = ['good', 'morning', 2026, 7.29]
print(lst)
```

> ['good', 'morning', 2026, 7.29]
    

字符串可以进行的操作包括索引，切片，加，乘，检查成员，这些列表也可以


```python
print(lst[0])  # 索引
```

> good
    


```python
print(lst[:-1])  # 切片
```

> ['good', 'morning', 2026]
    


```python
lst1 = ['hello', 'world']
print(lst1)
```

> ['hello', 'world']
    


```python
lst2 = lst + lst1  # 加
print(lst2)
```

> ['good', 'morning', 2026, 7.29, 'hello', 'world']
    


```python
lst3 = [0] * 5  # 乘
print(lst3)
```

> [0, 0, 0, 0, 0]
    


```python
flag = 'hello' in lst2  # 检查成员
print(flag)
```

> True
    

可以对列表进行增加元素和删除元素


```python
print(lst)
```

> ['good', 'morning', 2026, 7.29]
    


```python
lst.append('ruhe')  # 增
print(lst)
```

> ['good', 'morning', 2026, 7.29, 'ruhe']
    


```python
del lst[0]  # 删：按照索引删除
print(lst)
```

> ['morning', 2026, 7.29, 'ruhe']
    

列表可以嵌套列表

列表之间可以判断是否相等


```python
print(lst)
```

> ['morning', 2026, 7.29, 'ruhe']
    


```python
lst.append(['a', 'b'])
print(lst)
```

> ['morning', 2026, 7.29, 'ruhe', ['a', 'b']]
    


```python
import operator

lst4 = ['a', 'b']
lst5 = ['a', 'b']
lst6 = ['b', 'a']

print(operator.eq(lst4, lst5))
print(operator.eq(lst4, lst6))
```

> True
>
> False
    

列表常用方法


```python
print(len(lst))  # 
```

> 5
    


```python
lst7 = [4, 5, 9, 0, 1, 2, 4, 3, 4]
print(max(lst7))
```

> 9
    


```python
print(min(lst7))
```

> 0
    


```python
print(lst7.count(4))
```

> 3
    
