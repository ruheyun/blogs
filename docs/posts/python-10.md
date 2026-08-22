# 条件控制

条件语句是通过一条或多条语句的执行结果（True 或者 False）来决定执行的代码块。

例子：根据成绩输出不同等级(if-elif-else)


```python
score = 87

if score >= 90:
    print('A')
elif score >= 80:
    print('B')
elif score >= 70:
    print('C')
elif score >= 60:
    print('D')
else:
    print('E')

# B  
```
    

例子：Http 状态码匹配(match-case-_)


```python
status = 200

match status:
    case 400: print('Bad request')
    case 404: print('Not found')
    case 200: print('Success')
    case _: print('Not match')


# Success
```
