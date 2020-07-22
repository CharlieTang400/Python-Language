# 变量、运算符与数据类型
## 1. 注释

### 01. 单行注释(行注释)

* 以 `#` 开头，`#` 右边的所有东西都被当做说明文字，而不是真正要执行的程序，只起到辅助说明作用

* 示例代码如下：

```python
# 这是第一个单行注释
print("hello python")
```

> 为了保证代码的可读性，`#` 后面建议先添加一个空格，然后再编写相应的说明文字

#### 在代码后面增加的单行注释

* 在程序开发时，同样可以使用 `#` 在代码的后面（旁边）增加说明性的文字
* 但是，需要注意的是，**为了保证代码的可读性**，**注释和代码之间** 至少要有 **两个空格**

* 示例代码如下：

```python
print("hello python")  # 输出 `hello python`
```


### 02. 多行注释（块注释）

* 如果希望编写的 **注释信息很多，一行无法显示**，就可以使用多行注释
* 要在 Python 程序中使用多行注释，可以用 **一对 连续的 三个 引号**(单引号和双引号都可以)

* 示例代码如下：

```python
"""
这是一个多行注释

在多行注释之间，可以写很多很多的内容……
""" 
print("hello python")
```




## 2. 运算符

### 01. 算数运算符

* 是完成基本的算术运算使用的符号，用来处理四则运算

| 运算符| 描述 | 实例 |
| :---: | :---: | --- |
| + | 加 | 10 + 20 = 30 |
| - | 减 | 10 - 20 = -10 |
| * | 乘 | 10 * 20 = 200 |
| / | 除 | 10 / 20 = 0.5 |
| // | 取整除 | 返回除法的整数部分（商） 9 // 2 输出结果 4 |
| % | 取余数 | 返回除法的余数 9 % 2 = 1 |
| ** | 幂 | 又称次方、乘方，2 ** 3 = 8 |

* 在 Python 中 `*` 运算符还可以用于字符串，计算结果就是字符串重复指定次数的结果

```python
In [1]: "-" * 50
Out[1]: '----------------------------------------' 
```

### 02. 比较（关系）运算符

| 运算符 | 描述 |
| --- | --- |
| == | 检查两个操作数的值是否 **相等**，如果是，则条件成立，返回 True |
| != | 检查两个操作数的值是否 **不相等**，如果是，则条件成立，返回 True |
| > | 检查左操作数的值是否 **大于** 右操作数的值，如果是，则条件成立，返回 True |
| < | 检查左操作数的值是否 **小于** 右操作数的值，如果是，则条件成立，返回 True |
| >= | 检查左操作数的值是否 **大于或等于** 右操作数的值，如果是，则条件成立，返回 True |
| <= | 检查左操作数的值是否 **小于或等于** 右操作数的值，如果是，则条件成立，返回 True |

> Python 2.x 中判断 **不等于** 还可以使用 `<>` 运算符
> 
> `!=` 在 Python 2.x 中同样可以用来判断 **不等于**

### 03. 逻辑运算符

| 运算符 | 逻辑表达式 | 描述 |
| --- | --- | --- |
| and | x and y | 只有 x 和 y 的值都为 True，才会返回 True<br />否则只要 x 或者 y 有一个值为 False，就返回 False |
| or | x or y | 只要 x 或者 y 有一个值为 True，就返回 True<br />只有 x 和 y 的值都为 False，才会返回 False |
| not | not x | 如果 x 为 True，返回 False<br />如果 x 为 False，返回 True |

### 04. 赋值运算符

* 在 Python 中，使用 `=` 可以给变量赋值
* 在算术运算时，为了简化代码的编写，`Python` 还提供了一系列的 与 **算术运算符** 对应的 **赋值运算符**
* 注意：**赋值运算符中间不能使用空格**

| 运算符 | 描述 | 实例 |
| --- | --- | --- |
| = | 简单的赋值运算符 | c = a + b 将 a + b 的运算结果赋值为 c |
| += | 加法赋值运算符 | c += a 等效于 c = c + a |
| -= | 减法赋值运算符 | c -= a 等效于 c = c - a |
| *= | 乘法赋值运算符	 | c *= a 等效于 c = c * a |
| /= | 除法赋值运算符 | c /= a 等效于 c = c / a |
| //= | 取整除赋值运算符 | c //= a 等效于 c = c // a |
| %= | 取 **模** (余数)赋值运算符 | c %= a 等效于 c = c % a |
| **= | 幂赋值运算符 | c **= a 等效于 c = c ** a |


### 05. 位运算符

操作符 | 名称 | 示例
:---:|:---:|:---:
`~` |按位取反|`~4`
`&` |按位与  |`4 & 5`
`|` |按位或  |`4 | 5`
`^` |按位异或|`4 ^ 5`
`<<`|左移    |`4 << 2`
`>>`|右移    |`4 >> 2`

【例子】有关二进制的运算，参见“位运算”部分的讲解。
```python
print(bin(4))  # 0b100
print(bin(5))  # 0b101
print(bin(~4), ~4)  # -0b101 -5
print(bin(4 & 5), 4 & 5)  # 0b100 4
print(bin(4 | 5), 4 | 5)  # 0b101 5
print(bin(4 ^ 5), 4 ^ 5)  # 0b1 1
print(bin(4 << 2), 4 << 2)  # 0b10000 16
print(bin(4 >> 2), 4 >> 2)  # 0b1 1
```


### 06. 三元运算符

【例子】
```python
x, y = 4, 5
if x < y:
    small = x
else:
    small = y

print(small)  # 4
```

有了这个三元操作符的条件表达式，你可以使用一条语句来完成以上的条件判断和赋值操作。

【例子】
```python
x, y = 4, 5
small = x if x < y else y
print(small)  # 4
```

### 07. 其他运算符
操作符 | 名称 | 示例
:---:|:---:|:---:
`in`|存在| `'A' in ['A', 'B', 'C']`
`not in`|不存在|`'h' not in ['A', 'B', 'C']`
`is`|是| `"hello" is "hello"`
`is not`|不是|`"hello" is not "hello"`


【例子】
```python
letters = ['A', 'B', 'C']
if 'A' in letters:
    print('A' + ' exists')
if 'h' not in letters:
    print('h' + ' not exists')

# A exists
# h not exists
```

【例子】比较的两个变量均指向不可变类型。
```python
a = "hello"
b = "hello"
print(a is b, a == b)  # True True
print(a is not b, a != b)  # False False
```

【例子】比较的两个变量均指向可变类型。
```python
a = ["hello"]
b = ["hello"]
print(a is b, a == b)  # False True
print(a is not b, a != b)  # True False
```

注意：
- is, is not 对比的是两个变量的内存地址
- ==, != 对比的是两个变量的值
- 比较的两个变量，指向的都是地址不可变的类型（str等），那么is，is not 和 ==，！= 是完全等价的。
- 对比的两个变量，指向的是地址可变的类型（list，dict，tuple等），则两者是有区别的。


## 运算符的优先级

* 以下表格的算数优先级由高到最低顺序排列

| 运算符 | 描述 |
| --- | --- |
| ** | 幂 (最高优先级) |
| * / % // | 乘、除、取余数、取整除 |
| + - | 加法、减法 |
| <= < > >= | 比较运算符 |
| == != | 等于运算符 |
| = %= /= //= -= += *= **= | 赋值运算符 |
| not or and | 逻辑运算符 |




## 3. 变量和赋值

- 在使用变量之前，需要对其先赋值。
- 变量名可以包括字母、数字、下划线、但变量名不能以数字开头。
- Python 变量名是大小写敏感的，foo != Foo。

【例子】
```python
teacher = "老马的程序人生"
print(teacher)  # 老马的程序人生
```

【例子】
```python
first = 2
second = 3
third = first + second
print(third)  # 5
```

【例子】
```python
myTeacher = "老马的程序人生"
yourTeacher = "小马的程序人生"
ourTeacher = myTeacher + ',' + yourTeacher
print(ourTeacher)  # 老马的程序人生,小马的程序人生
```




## 4. 数据类型与转换


类型 | 名称 | 示例
:---:|:---:|:---:
int | 整型 `<class 'int'>`| `-876, 10`
float | 浮点型`<class 'float'>`| `3.149, 11.11`
bool | 布尔型`<class 'bool'>` | `True, False`

<b>整型</b>

【例子】通过 `print()` 可看出 `a` 的值，以及类 (class) 是`int`。
```python
a = 1031
print(a, type(a))
# 1031 <class 'int'>
```


Python 里面万物皆对象（object），整型也不例外，只要是对象，就有相应的属性 （attributes） 和方法（methods）。

【例子】
```python
b = dir(int)
print(b)

# ['__abs__', '__add__', '__and__', '__bool__', '__ceil__', '__class__',
# '__delattr__', '__dir__', '__divmod__', '__doc__', '__eq__',
# '__float__', '__floor__', '__floordiv__', '__format__', '__ge__',
# '__getattribute__', '__getnewargs__', '__gt__', '__hash__',
# '__index__', '__init__', '__init_subclass__', '__int__', '__invert__',
# '__le__', '__lshift__', '__lt__', '__mod__', '__mul__', '__ne__',
# '__neg__', '__new__', '__or__', '__pos__', '__pow__', '__radd__',
# '__rand__', '__rdivmod__', '__reduce__', '__reduce_ex__', '__repr__',
# '__rfloordiv__', '__rlshift__', '__rmod__', '__rmul__', '__ror__',
# '__round__', '__rpow__', '__rrshift__', '__rshift__', '__rsub__',
# '__rtruediv__', '__rxor__', '__setattr__', '__sizeof__', '__str__',
# '__sub__', '__subclasshook__', '__truediv__', '__trunc__', '__xor__',
# 'bit_length', 'conjugate', 'denominator', 'from_bytes', 'imag',
# 'numerator', 'real', 'to_bytes']
```

对它们有个大概印象就可以了，具体怎么用，需要哪些参数 （argument），还需要查文档。看个`bit_length()`的例子。

【例子】找到一个整数的二进制表示，再返回其长度。

```python
a = 1031
print(bin(a))  # 0b10000000111
print(a.bit_length())  # 11
```


<b>浮点型</b>

【例子】
```python
print(1, type(1))
# 1 <class 'int'>

print(1., type(1.))
# 1.0 <class 'float'>

a = 0.00000023
b = 2.3e-7
print(a)  # 2.3e-07
print(b)  # 2.3e-07
```
有时候我们想保留浮点型的小数点后 `n` 位。可以用 `decimal` 包里的 `Decimal` 对象和 `getcontext()` 方法来实现。

```python
import decimal
from decimal import Decimal
```

Python 里面有很多用途广泛的包 (package)，用什么你就引进 (import) 什么。包也是对象，也可以用上面提到的`dir(decimal)` 来看其属性和方法。

【例子】`getcontext()` 显示了 `Decimal` 对象的默认精度值是 28 位 (`prec=28`)。

```python
a = decimal.getcontext()
print(a)

# Context(prec=28, rounding=ROUND_HALF_EVEN, Emin=-999999, Emax=999999,
# capitals=1, clamp=0, flags=[], 
# traps=[InvalidOperation, DivisionByZero, Overflow])
```


```python
b = Decimal(1) / Decimal(3)
print(b)

# 0.3333333333333333333333333333
```

【例子】使 1/3 保留 4 位，用 `getcontext().prec` 来调整精度。

```python
decimal.getcontext().prec = 4
c = Decimal(1) / Decimal(3)
print(c)

# 0.3333
```

<b>布尔型</b>

布尔 (boolean) 型变量只能取两个值，`True` 和 `False`。当把布尔型变量用在数字运算中，用 `1` 和 `0` 代表 `True` 和 `False`。

【例子】
```python
print(True + True)  # 2
print(True + False)  # 1
print(True * False)  # 0
```



除了直接给变量赋值 `True` 和 `False`，还可以用 `bool(X)` 来创建变量，其中 `X` 可以是

- 基本类型：整型、浮点型、布尔型
- 容器类型：字符串、元组、列表、字典和集合

【例子】`bool` 作用在基本类型变量：`X` 只要不是整型 `0`、浮点型 `0.0`，`bool(X)` 就是 `True`，其余就是 `False`。
```python
print(type(0), bool(0), bool(1))
# <class 'int'> False True

print(type(10.31), bool(0.00), bool(10.31))
# <class 'float'> False True

print(type(True), bool(False), bool(True))
# <class 'bool'> False True
```


【例子】`bool` 作用在容器类型变量：`X` 只要不是空的变量，`bool(X)` 就是 `True`，其余就是 `False`。

```python
print(type(''), bool(''), bool('python'))
# <class 'str'> False True

print(type(()), bool(()), bool((10,)))
# <class 'tuple'> False True

print(type([]), bool([]), bool([1, 2]))
# <class 'list'> False True

print(type({}), bool({}), bool({'a': 1, 'b': 2}))
# <class 'dict'> False True

print(type(set()), bool(set()), bool({1, 2}))
# <class 'set'> False True
```


确定`bool(X)` 的值是 `True` 还是 `False`，就看 `X` 是不是空，空的话就是 `False`，不空的话就是 `True`。

- 对于数值变量，`0`, `0.0` 都可认为是空的。
- 对于容器变量，里面没元素就是空的。


<b>获取类型信息</b>

- 获取类型信息 `type(object)`

【例子】
```python
print(type(1))  # <class 'int'>
print(type(5.2))  # <class 'float'>
print(type(True))  # <class 'bool'>
print(type('5.2'))  # <class 'str'>
```

- 获取类型信息 `isinstance(object, classinfo)`

【例子】
```python
print(isinstance(1, int))  # True
print(isinstance(5.2, float))  # True
print(isinstance(True, bool))  # True
print(isinstance('5.2', str))  # True
```

注：
- `type()` 不会认为子类是一种父类类型，不考虑继承关系。
- `isinstance()` 会认为子类是一种父类类型，考虑继承关系。

如果要判断两个类型是否相同推荐使用 `isinstance()`。


**类型转换**

- 转换为整型 `int(x, base=10)`
- 转换为字符串 `str(object='')`
- 转换为浮点型 `float(x)`

【例子】

```python
print(int('520'))  # 520
print(int(520.52))  # 520
print(float('520.52'))  # 520.52
print(float(520))  # 520.0
print(str(10 + 10))  # 20
print(str(10.1 + 5.2))  # 15.3
```


## 5. print() 函数

```python
print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
```
- 将对象以字符串表示的方式格式化输出到流文件对象file里。其中所有非关键字参数都按`str()`方式进行转换为字符串输出；
- 关键字参数`sep`是实现分隔符，比如多个参数输出时想要输出中间的分隔字符；
- 关键字参数`end`是输出结束时的字符，默认是换行符`\n`；
- 关键字参数`file`是定义流输出的文件，可以是标准的系统输出`sys.stdout`，也可以重定义为别的文件；
- 关键字参数`flush`是立即把内容输出到流文件，不作缓存。

【例子】没有参数时，每次输出后都会换行。
```python
shoplist = ['apple', 'mango', 'carrot', 'banana']
print("This is printed without 'end'and 'sep'.")
for item in shoplist:
    print(item)

# This is printed without 'end'and 'sep'.
# apple
# mango
# carrot
# banana
```

【例子】每次输出结束都用`end`设置的参数`&`结尾，并没有默认换行。

```python
shoplist = ['apple', 'mango', 'carrot', 'banana']
print("This is printed with 'end='&''.")
for item in shoplist:
    print(item, end='&')
print('hello world')

# This is printed with 'end='&''.
# apple&mango&carrot&banana&hello world
```


【例子】`item`值与`'another string'`两个值之间用`sep`设置的参数`&`分割。由于`end`参数没有设置，因此默认是输出解释后换行，即`end`参数的默认值为`\n`。


```python
shoplist = ['apple', 'mango', 'carrot', 'banana']
print("This is printed with 'sep='&''.")
for item in shoplist:
    print(item, 'another string', sep='&')

# This is printed with 'sep='&''.
# apple&another string
# mango&another string
# carrot&another string
# banana&another string
```


---
**参考文献**：
- https://www.runoob.com/python3/python3-tutorial.html
- https://www.bilibili.com/video/av4050443
- https://mp.weixin.qq.com/s/DZ589xEbOQ2QLtiq8mP1qQ
- https://www.cnblogs.com/OliverQin/p/7781019.html



---
**练习题**：

1. 怎样对python中的代码进行注释？
2. python有哪些运算符，这些运算符的优先级是怎样的？
3. python 中 `is`, `is not` 与 `==`, `!=` 的区别是什么？
4. python 中包含哪些数据类型？这些数据类型之间如何转换？
