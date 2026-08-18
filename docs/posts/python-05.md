# 字符串
字符串是 Python 中最常用的数据类型，不可变类型数据，使用单引号或者双引号包裹（str）


```python
str1 = 'hello world'
print(str1)
```

> hello world
    


```python
str2 = 'h'  # python中没有字符，单个字符也是字符串
print(str2)
```

> h
    


```python
str3 = str1[1:4]  # 可以使用[]截取字符串，获得子字符串，语法：[头下标：尾下标] （前闭后开），第一个索引为0
print(str3)
```

> ell
    


```python
str4 = str1[-4:]  # 也可以从后往前截取，最后一个索引为-1
print(str4)
```

> orld
    


```python
a = 'hello'
b = 'world'
c1 = a + b  # 字符串可相加获得新字符串
print(c1)
```

> helloworld
    


```python
c2 = a * 3  # 与常数相乘，表示重复次数
print(c2)
```

> hellohellohello
    


```python
c3 = 'h' in a  # 成员运算符
print(c3)
```

> True
    


```python
c4 = 's' not in a 
print(c4)
```

> True
    


```python
name = '如何'
age = 25
print('我是 %s 今年 %d 岁。' % (name, age))  # 字符串格式化输出
```

> 我是 如何 今年 25 岁。
    


```python
print(f'我是 {name} 今年 {age} 岁。')  # 更简单的字符串格式化方法：f-string （3.6版本后支持）
```

> 我是 如何 今年 25 岁。
    
