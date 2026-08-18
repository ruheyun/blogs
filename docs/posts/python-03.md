# 数据类型

**不可变数据（4 个）**

Number（数字）、String（字符串）、bool（布尔）、Tuple（元组）

**可变数据（3 个）**

List（列表）、Dictionary（字典）、Set（集合）

**数据类型转换**

1. 隐式类型转换 - 自动完成
2. 显式类型转换 - 需要使用类型函数来转换


**例子**

```python
num_1, num_2 = 5, 10.5
print(f'num_1 的数据类型是：{type(num_1)}')

num_3 = num_1 + num_2
# num_3 是 float 类型，低数据类型会自动向高数据类型转化
print(f'{type(num_1)}, {type(num_2)}, {type(num_3)}')  
```

> num_1 的数据类型是：<class 'int'>
>
> <class 'int'>, <class 'float'>, <class 'float'>
    


```python
str_1, str_2 = 'ruhe', '12'
num_4 = int(str_2)  # 手动强制类型转换
print(f'{type(str_1)}, {type(str_2)}, {type(num_4)}')
```

> <class 'str'>, <class 'str'>, <class 'int'>
    


```python
bl = True
print(f'bl 的数据类型是：{type(bl)}')
```

> bl 的数据类型是：<class 'bool'>
    


```python
tup = (1, 2, 3)
print(f'tup 的数据类型是：{type(tup)}')
```

> tup 的数据类型是：<class 'tuple'>
    


```python
lst = [1, 2, 3]
print(f'lst 的数据类型是：{type(lst)}')
```

> lst 的数据类型是：<class 'list'>
    


```python
dic = {'name': 'ruhe', 'age': 25}
print(f'dic 的数据类型是：{type(dic)}')
```

> dic 的数据类型是：<class 'dict'>
    


```python
st = {'python', 'java', 'js'}
print(f'st 的数据类型是：{type(st)}')
```

> st 的数据类型是：<class 'set'>


> [!tip]
> 1. 上述 type 方法可以得到数据的类型
> 2. 在 print 里使用了叫 f-format 格式化，可以将变量用 {} 包裹输出打印
> 3. 不用特意去记不同数据类型的高低，必要时可以使用 type 方法来判断
