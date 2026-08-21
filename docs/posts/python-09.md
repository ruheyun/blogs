# 集合

集合（set）是一个无序的不重复元素序列。


```python
set1 = {1, 2, 3, 4}
print(set1)

# {1, 2, 3, 4}
```
    

空集合不能使用 {} 来创建，只能使用 set() 创建，{} 是用来创建字典的


```python
set2 = {}
print(type(set2))
set3 = set()
print(type(set3))

'''
    <class 'dict'>
    <class 'set'>
'''
```
    


```python
set4 = set([1, 2, 3, 4, 1, 5, 6]) 
print(set4)  # 会自动去重

# {1, 2, 3, 4, 5, 6}
```
    


```python
print(1 in set4)  # 判断元素是否在集合内

# True
```
    


```python
# 两个集合间的运算
set5 = set('abracadabra')
set6 = set('alacazm')

print(set5)
print(set6)

'''
    {'b', 'r', 'a', 'c', 'd'}
    {'m', 'l', 'z', 'a', 'c'}
'''
```
    


```python
set5 - set6  # 集合 set5 中包含的元素，而集合 set6 中不包含的元素

# {'b', 'd', 'r'}
```


```python
set5 | set6  # 集合 set5 或 set6 中包含的元素

# {'a', 'b', 'c', 'd', 'l', 'm', 'r', 'z'}
```



```python
set5 & set6  # 集合 set5 和 set6 都包含的元素

# {'a', 'c'}
```


```python
set5 ^ set6  # 不同时包含于两个集合中的元素

# {'b', 'd', 'l', 'm', 'r', 'z'}
```


```python
set5 + set6  # 集合中不能进行 + 操作

'''
    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[10], line 1
    ----> 1 set5 + set6  # 集合中不能进行 + 操作
    

    TypeError: unsupported operand type(s) for +: 'set' and 'set'
'''
```





```python
set7 = {x for x in 'asdfghjklko' if x not in 'abc'}  # 集合推导式
print(set7)

# {'s', 'k', 'o', 'f', 'j', 'h', 'l', 'g', 'd'}
```
    


```python
# 集合的基本操作
set8 = set()
print(set8)

# set()
```
    


```python
set8.add('a')  # add 只能添加单个元素
print(set8)

# {'a'}
```
    


```python
set8.add(['b', 'c'])

'''
    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[15], line 1
    ----> 1 set8.add(['b', 'c'])
    

    TypeError: cannot use 'list' as a set element (unhashable type: 'list')
'''
```



```python
set8.add('a')  # 如果添加集合中已有的元素，则等价于不添加
print(set8)

# {'a'}
```
    


```python
set8.update([1, 2, 3])  # update 可以添加列表
print(set8)

# {3, 1, 2, 'a'}
```
    


```python
set8.remove('a')  # 从集合中删除元素，如果元素不存在则报错
print(set8)

# {3, 1, 2}
```
    


```python
set8.discard('a')  # 从集合中删除元素，如果元素不存在不会报错
print(set8)

# {3, 1, 2}
```
    


```python
x = set8.pop()  # 随机删除一个元素，且返回这个元素
print(x)

# 3
```
    


```python
len(set8)  # 计算元素个数

# 2
```




```python
set8.clear()  # 清空集合
print(set8)

# set()
```
