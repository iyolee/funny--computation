# Scheme

## 配置环境
#### 安装
```
sudo apt-get install mit-scheme

# Mac
brew install mit-scheme
```

#### 使用
- 进入 repl：在终端输入 ```mit-scheme``` 或 ```scheme```
- 执行程序：```scheme < test.scm```

## 语法
### 四种基本算术操作
形如这些由括号、标记（token）以及分隔符组成的式子，被称为S-表达式。

+、-、*和/分别代表加、减、乘、除。这些函数都接受任意多的参数。
``` scm
(- 10 3)    ;→ 7
(- 10 3 5)  ;→ 2
(* 2 3)     ;→ 6
(* 2 3 4)   ;→ 24
(/ 29 3)    ;→ 29/3
(/ 29 3 7)  ;→ 29/21
(/ 9 6)     ;→ 3/2
(* (+ 2 3) (- 5 3)) ;→ 10
(/ (+ 9 1) (+ 2 3)) ;→ 2
```

Scheme（以及大多数Lisp方言）都可以处理分数。

函数exact->inexact 用于把分数转换为浮点数。Scheme也可以处理复数。复数是形如a+bi的数，此处a称为实部，b称为虚部。

``` scm
(exact->inexact (/ 29 3 7)) ;→ 1.380952380952381
```

### 其它算术操作
#### quotient，remainder，modulo和sqrt
- 函数`quotient`用于求商数（quotient）。
- 函数`remainder`和modulo用于求余数（remainder）。
- 函数`sqrt`用于求参数的平方根（square root）。

``` scm
(quotient 7 3) ;→ 2
(modulo 7 3)   ;→ 1
(sqrt 8)       ;→ 2.8284271247461903
```

#### 三角函数
数学上的三角函数，诸如sin，cos，tan，asin，acos和atan都可以在Scheme中使用。atan接受1个或2个参数。如果atan的参数为1/2 π，那么就要使用两个参数来计算。

``` scm
(atan 1)   ;→ 0.7853981633974483
(atan 1 0) ;→ 1.5707963267948966
```

#### 指数和对数
指数通过exp函数运算，对数通过log函数运算。a的b次幂可以通过(expt a b)来计算。

### 生成表
作为Lisp语言大家族的一员，Scheme同样擅长于处理表。

#### Cons单元
Cons单元是一个存放了两个地址的内存空间。Cons单元可用函数cons生成。