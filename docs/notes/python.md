# Python基础知识

## 1. Python是什么？

Python是一种高级编程语言，由Guido van Rossum于1991年创建。它以简洁、易读的语法和强大的功能而闻名，被广泛应用于Web开发、数据分析、人工智能等领域。

## 2. Python的特点

- 简洁易读：Python采用简洁的语法，使得代码易于理解和编写。
- 面向对象：Python支持面向对象编程，可以使用类和对象来组织代码。
- 多功能：Python拥有丰富的标准库和第三方库，可以完成各种任务，如网络编程、图形界面开发、数据处理等。
- 跨平台：Python可以在多个操作系统上运行，包括Windows、Linux和Mac OS等。
- 动态类型：Python是一种动态类型语言，不需要显式声明变量类型，可以根据上下文自动推断。

## 3. 基本语法

### 变量和数据类型

Python中的变量不需要显式声明，可以直接赋值。常见的数据类型包括整数、浮点数、字符串、列表、元组和字典等。

```python
# 整数
x = 10

# 浮点数
y = 3.14

# 字符串
name = "Alice"

# 列表
numbers = [1, 2, 3, 4, 5]

# 元组
point = (2, 3)

# 字典
person = {"name": "Bob", "age": 25}
```

### 条件语句和循环

Python使用缩进来表示代码块，没有花括号。条件语句使用`if`、`elif`和`else`关键字，循环使用`for`和`while`关键字。

```python
# 条件语句
if x > 0:
    print("x is positive")
elif x < 0:
    print("x is negative")
else:
    print("x is zero")

# for循环
for number in numbers:
    print(number)

# while循环
i = 0
while i < 5:
    print(i)
    i += 1
```

### 函数定义和调用

可以使用`def`关键字定义函数，并使用`return`关键字返回值。

```python
# 函数定义
def add(x, y):
    return x + y

# 函数调用
result = add(3, 5)
print(result)  # 输出8
```

## 4. 库和模块

Python拥有丰富的标准库和第三方库，可以通过`import`关键字引入并使用。

```python
# 引入标准库中的math模块
import math

# 使用math模块中的函数
print(math.sqrt(16))  # 输出4.0

# 引入第三方库中的pandas模块
import pandas as pd

# 使用pandas模块中的函数
data = pd.read_csv("data.csv")
```

以上是Python的一些基础知识，希望对你有帮助！