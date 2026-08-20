# 元组

元组与列表类似, 不同之处在于元组的元素不能修改, 元组使用小括号 ()


```python
tup1 = ('hello', 'world', 2026)
print(tup1)

# ('hello', 'world', 2026)
```
    

创建空元组时，用小括号表示，但是元组中只包含一个元素时，需要在元素后面添加逗号 , ，否则括号会被当作运算符使用


```python
tup2 = ()
tup3 = (3)
tup4 = (3,)
print(type(tup2))
print(type(tup3))
print(type(tup4))

'''
<class 'tuple'>
<class 'int'>
<class 'tuple'>
'''
```


    

元组可以索引和切片


```python
print(tup1)

# ('hello', 'world', 2026)
```
    


```python
print(tup1[0])

# hello
```
    


```python
print(tup1[:2])

# ('hello', 'world')
```
    

元组不能修改


```python
tup5 = (1, 2,3)
tup6 = (4, 5)
tup5[0] = 2  # 不能修改，会报错

'''
   ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[6], line 3
          1 tup5 = (1, 2,3)
          2 tup6 = (4, 5)
    ----> 3 tup5[0] = 2  # 不能修改，会报错
    

    TypeError: 'tuple' object does not support item assignment
'''
```



```python
tup7 = (1, 2, 3)
print(id(tup7))
tup7 = tup7 + tup6  # 通过拼接改变元组大小，但是元组所指向内存地址也会变化，也就是产生新的元组
print(id(tup7))
print(tup7)

'''
    1578677947584
    1578677742528
    (1, 2, 3, 4, 5)
'''
```


    

元组中的元素值是不允许删除的，但我们可以使用del语句来删除整个元组


```python
tup8 = (1, 2)
del tup8[0]

'''
    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[8], line 2
          1 tup8 = (1, 2)
    ----> 2 del tup8[0]
    

    TypeError: 'tuple' object doesn't support item deletion
'''
```






```python
del tup8  # 不会输出任何东西
```

列表对应的方法，元组也同样适用


```python
tup9 = (1, 2, 3, 0)
print(len(tup9))
print(max(tup9))
print(min(tup9))

'''
    4
    3
    0
'''
```


    


```python
tup10 = (1, 1)
print(tup10)

#     (1, 1)
```


    
