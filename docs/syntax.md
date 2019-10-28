# Lisp
1958年，John McCarthy 设计了 Lisp 语言。Lisp 是一种记法形式，是为了能对某种特定形式的逻辑表达式（称为递归方程）的使用做推理。Lisp 的名字来自表处理（LISt Processing），其设计是为了提供符号计算的能力，以便能用于解决一些程序设计问题，例如代数表达式的符号微分和积分。

### Lisp 使用前缀表示法
``` lisp
(/ (* a (+ b c) ) d)
```

### 'Hello World' 程序
``` lisp
(write-line "Hello World")
```

### Lisp 基本语法
#### 1. Lisp 基本构建块
Lisp程序是由三个基本构建块：
- atom
- list
- string

一个原子是一个数字连续字符或字符串。它包括数字和特殊字符。
``` lisp
name
1234
*hello*
abc123
```

列表是包含在括号中的原子和/或其他列表的序列。
``` lisp
(a ( a b c) d e)
(hello world)
```

字符串是一组括在双引号字符。
``` lisp
"hello world"
```

#### 2. 添加注释
分号符号(;)是用于表示一个注释行。
``` lisp
(write-line "Hello World") ; greet the world
```