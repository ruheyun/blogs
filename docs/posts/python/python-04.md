# 数字类型
1. int
2. float
3. complex

**例子**

```python
num1 = 10  # 整数
print(num1)
```

> 10
    


```python
num2 = 12.2  # 浮点数
print(num2)
```

> 12.2
    


```python
num3 = 2 + 3j  # 复数
print(num3)
```

> (2+3j)
    


```python
num4 = complex(2, 3)  # 复数的头部和虚部都是浮点型
print(num4)
```

> (2+3j)
    


```python
a = 1.2
a = int(a)  # 强制类型转换为整数类型，会损失精度
print(a)
```

> 1
    


```python
a = 1
a = float(a)  # 将整型转为浮点型
print(a)
```

> 1.0
    


```python
a = 1
a = complex(a)  # 将整型转化为复数，实部为a，虚部为0
print(a)
```

> (1+0j)
    


```python
a, b = 1, 2
c = complex(a, b)  # 将两个整数转为复数，实部为a，虚部为b
print(c)
```

> (1+2j)
    


```python
z = complex(2.1, 3)
x = z.real  # 返回复数的实部
y = z.imag  # 返回复数的虚部
print(x, y)  # 从输出可以看出复数的实部和虚部都属浮点数
```

> 2.1 3.0
    


```python
a = 0xA  # 整数有16进制形式，需要加前缀‘0x’
print(a)
```

> 10
    


```python
a = 0o10  # 整数有8进制形式，需要加前缀‘0o’
print(a)
```

> 8
    


```python
a = 9  # 默认是10进制，不需要加任何前缀
print(a)
```

> 9
    


```python
a = 0b0101  # 整数有2进制形式，需要加前缀‘0b’
print(a)
```

> 5
    


```python
a = 17
a = hex(a)  # 将十进制转为16进制，并以16进制输出
print(a)
```

> 0x11
    


```python
a = 8
a = oct(a)  # 将十进制转为8进制，并以8进制输出
print(a)
```

> 0o10
    


```python
a = 5
a = bin(a)  # 将十进制转为2进制，并以2进制输出  
print(a)
```

> 0b101
    


```python
a = '0x12'
a = int(a[2:], 16)  # 将16进制转为10进制，注意需要将16进制的前缀去掉，其余进制转为10进制同理，将后面16换为对应进制即可
print(a)
```

> 18
    


```python
a = 10
b = 3

c = a + b  # 加法运算
d = a - b  # 减法运算
f = a * b  # 乘法运算
g = a / b  # 除法运算
h = a // b  # 将除法运算结果的小数位置0

print(c, d, f, g, h)
```

> 13 7 30 3.3333333333333335 3
    
