# 循环语句

循环语句是用来重复执行某一段代码的语句。只要满足条件，代码就会一遍一遍地执行，直到条件不满足为止。

例子：输出 1到100 这100个数的和(for/while)


```python
result = 0
for i in range(1, 101):
    result += i

print(result)

# 5050
```


```python
result = 0
i = 1
while i <= 100:
    result += i
    i += 1  # 如果忽略了这行代码，程序将陷入无限循环，注意！

print(result)

# 5050
```
