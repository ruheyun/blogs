# 初识

用 Scheme 简单计算加减乘除

打开 MIT Scheme 交互式解释器

```scheme
(+ 1 2)
```

```output
;Value: 3
```

```scheme
(- 5 2)
```

```output
;Value: 3
```

```scheme
(* 3 4)
```

```output
;Value: 12
```

```scheme
(/ 6 4)
```

```output
;Value: 3/2
```

```scheme
(exact->inexact (/ 6 4))
```

```output
1.5
```

> 为了方便，后续的输出不再粘贴 `;Value: ` 部分，只显示结果。

> [!tip]
> 对上述 5 个程序的运行，可以看出 Scheme 主要采用前缀表达式（Prefix Notation），即函数/运算符写在参数前面。小括号划分每个操作。

