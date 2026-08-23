# 基础语法

**关键字**

Python 中定义了一些专有词汇，统称为“关键字”，比如 break、class、if、print 等，它们都具有特定的含义，只能用于特定的位置。
    
**标识符（变量）**

Python 语言中的类名、对象名、方法名和变量名等，统称为“标识符”。

要求：

1. 第一个字符必须是字母（a-z, A-Z）或下划线 _ 。
2. 标识符的其他的部分由字母、数字和下划线组成。
3. 标识符对大小写敏感，count 和 Count 是不同的标识符。
4. 禁止使用保留关键字，如 if、for、class 等不能作为标识符。

**基本数据类型**

1. 整数，例如：1, 2
2. 小数，例如：1.1, 1.2
3. 字符串，例如：'hello'
4. 布尔，例如：True, False
    
**输入、输出**

1. input
2. print

**例子**

```python
name = 'ruhe'  # '='：赋值

# input 语句会将输入变成字符串类型，因此年龄是整数类型，需要使用 int 转换
age = int(input('please input age:'))  

print(name, age)
print('hello', sep='', end='-->')
print('world')
```

> please input age: 15
>
> ruhe 15
>
> hello-->world
    
