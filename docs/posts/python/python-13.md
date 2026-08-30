# 迭代器

迭代器是一个可以记住遍历的位置的对象。

迭代器对象从列表/元组/字符串的第一个元素开始访问，直到所有的元素被访问完结束。迭代器只能往前不会后退。

迭代器有两个基本的方法：iter() 和 next()。


```python
lst1 = [1, 3, 5, 8, 9]
it = iter(lst1)
it
```




    <list_iterator at 0x1699208dbd0>




```python
next(it)
```




    1




```python
for i in it:
    print(i)
```

    3
    5
    8
    9
    


```python
next(it)  # 已全部迭代完，超出索引了，StopIteration 异常用于标识迭代的完成
```


    ---------------------------------------------------------------------------

    StopIteration                             Traceback (most recent call last)

    Cell In[4], line 1
    ----> 1 next(it)  # 已全部迭代完，超出索引了，StopIteration 异常用于标识迭代的完成
    

    StopIteration: 


使用了 yield 的函数称为生成器，调用生成器会得到一个生成器对象，生成器对象是一种迭代器

生成器是一种可以暂停和恢复的迭代器。如果生成器函数内部写了无限循环，它就可以一直产出值。


```python
def gen():
    n = 1
    while True:
        yield n
        n += 1
```


```python
g = gen()
```


```python
next(g)
```




    1




```python
next(g)  # 可以一直 next 下去
```




    2


