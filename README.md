# Python快速入门指北

~~友情提示：专供可怜的中国高中生~~

## 1.1 编者前言

**这并不是一篇文章，而是一篇入门文档，重点针对的是高中信息会考，会有许多疏漏之处，请谅解。**

Python是一门极其容易的语言，相信在未来的所有专业中必将都有计算机的一席之地，现在学一点基础的内容也不是什么坏事吧。

本篇教程完全基于一个啥也不会的小白，当然由于是笔试而不是机试，所以Python安装等过程就略过了。

右侧存在目录，挑选自己不会的看。如果是啥都不会的，那就按顺序看。

**再次强调，本教程由于重点针对考试，对于实际的一些操作还有很多未介绍**

参考文档：[Learn Python with Penjee](https://penjee.com/)

[The Python Tutorial — Python 3.6.15 documentation](https://docs.python.org/3.6/tutorial/index.html)

[walter201230/Python: 最良心的 Python 教程(github.com)](https://github.com/walter201230/Python)

## 1.2 目录

[TOC]



## 1.3 基础知识

### 1.3.1 程序段

看这一段程序：

```python
a = 1
b = 2
if a>b:
    a,b = b,a
	print(a)
else:
	print(b)
```

Python的代码的易读性非常强，在同一段区块的程序都是一段，比如在这段程序中`a,b=b,a`和`print(a)`就是一段顺序执行的程序。

### 1.3.2 变量

就如同你做代数运算一样，当你算a+b的数值时就一定要知道a和b的具体数值。计算机在进行运算时也需要“记住”这些数值。

```python
a = 1
b = 1
c = a + b
```

这段代码的意思就是告诉计算机"a"里面存放的是数值1，“b”里面存放的是数值1，“c”里面存放的是a + b的数值，那么就是1+1=2。

> TIPS：1.变量名称由**数字、字母(包括大写字母和小写字母)、下划线**组成。
>
> 2.变量名不能以数字开头
>
> 3.变量名不能用python关键字（如print，if，else之类的）
>
> 4.变量命名严格区分大小写

### 1.3.3 变量类型

- `int`类型：存放整数（可正可负）
- `float`类型：存放浮点数（即普通小数，如1.1234）
- `string`类型：存放字符串

> TIPS：1.int和float类型都可以进行加减乘除。
>
> 2.string操作在下文。

### 1.3.4 算术运算符

以下假设变量： **a=10，b=20**：

| 运算符 | 描述                                            | 实例                                               |
| :----- | :---------------------------------------------- | :------------------------------------------------- |
| +      | 加 - 两个对象相加                               | a + b 输出结果 30                                  |
| -      | 减 - 得到负数或是一个数减去另一个数             | a - b 输出结果 -10                                 |
| *      | 乘 - 两个数相乘或是返回一个被重复若干次的字符串 | a * b 输出结果 200                                 |
| /      | 除 - x除以y                                     | b / a 输出结果 2                                   |
| %      | 取模 - 返回除法的余数                           | b % a 输出结果 0                                   |
| **     | 幂 - 返回x的y次幂                               | a**b 为10的20次方， 输出结果 100000000000000000000 |
| //     | 取整除 - 返回商的整数部分（**向下取整**）       | `9//2=4`                                           |

### 1.3.5 运算优先级

即运算的先后顺序

下表从大到小排列：

| 运算符      | 描述   |
| :---------- | :----- |
| ()          | 小括号 |
| **          | 乘方   |
| *、/、//、% | 乘除   |
| +、-        | 加减   |

### 1.3.6 比较运算符

**先说明一个概念：`True`或`False`**。很好理解，这个判断条件成立那么就是True，如果不成立就是False。

> TIPS:在if语句中，如果判断表达式的值为true，那么就执行条件下的语句，如果判断表达式的值为false，那么就执行else。

以下假设变量a为10，变量b为20：

| 运算符 | 描述                            | 实例                  |
| :----- | :------------------------------ | :-------------------- |
| ==     | 等于 - 比较对象是否相等         | (a == b) 返回 False。 |
| !=     | 不等于 - 比较两个对象是否不相等 | (a != b) 返回 true.   |
| >      | 大于 - 返回x是否大于y           | (a > b) 返回 False。  |
| <      | 小于 - 返回x是否小于y。         | (a < b) 返回 true。   |
| >=     | 大于等于 - 返回x是否大于等于y。 | (a >= b) 返回 False。 |
| <=     | 小于等于 - 返回x是否小于等于y。 | (a <= b) 返回 true。  |

### 1.3.7 赋值运算符

| 运算符 | 描述             | 实例                                  |
| :----- | :--------------- | :------------------------------------ |
| =      | 赋值运算符       | c = a + b 将 a + b 的运算结果赋值为 c |
| +=     | 加法赋值运算符   | c += a 等效于 c = c + a               |
| -=     | 减法赋值运算符   | c -= a 等效于 c = c - a               |
| *=     | 乘法赋值运算符   | c *= a 等效于 c = c * a               |
| /=     | 除法赋值运算符   | c /= a 等效于 c = c / a               |
| %=     | 取模赋值运算符   | c %= a 等效于 c = c % a               |
| **=    | 幂赋值运算符     | `c **= a 等效于 c = c ** a`           |
| //=    | 取整除赋值运算符 | c //= a 等效于 c = c // a             |

## 1.4 输入输出

在Python中获取键盘输入输出的函数非常简单，总结起来就是`input`和`print`

### 1.4.1 input

input是从键盘中获取输入，直到你按下回车键为止，它的返回值是一段字符串，例如：

```python
var = input()
```

此时你可以输入Hello World、1等等文本，最后var变量里存放的就是这么一段字符串。

当我们想要得到数字或浮点类型时，只需要在input外面套一层`int()`或`float()`，例如：

```python
var1 = int(input())
var2 = float(input())
```

那么变量var1里存放的就是int类型的整数，var2里存放的就是float类型的浮点数。

当然你也可以在input()里面加上一段话，作为输入的提示：

```python
var1 = input("Please Enter a word:")
```

> TIPS：有关数据类型请看上一章。

### 1.4.2 print

print是往屏幕上输出变量，通常情况下以回车结尾，例如：

```python
print("Hello World!")
```

那么输出的就是一个“Hello World!”

如果输出多个变量，那么Python会自动以空格隔开，例如：

```python
var1 = "Hello"
var2 = "World"
print(var1 ,var2)
```

那么输出的就是`Hello World`，注意到Hello和World之间存在一个空格。

你可以自定义你结尾的字符串，例如：

```python
print("Hello",end="")
print("World!")
```

那么在第一个`print()`操作完成之后，结尾不再是换行。

## 1.5 字符串操作

字符串是一种最为基础的数据类型，可以理解为“一段文本”。

### 1.5.1 创建与访问

创建字符串：`a = "Hello"`，那么变量a就是一个字符串了。

Python 访问子字符串，可以使用方括号 **[]** 来截取字符串，字符串的截取的语法格式如下：

```python
变量[头下标:尾下标]
```

![img](https://static.runoob.com/wp-content/uploads/123456-20200923-1.svg)

需要注意的是第一个字符的位置是0，如果从负数开始那么最后一个字符就是-1开始。

> TIPS：
>
> 在Python中无论是访问数组还是字符串都遵循**左闭右开**的原则。
>
> 例如在上图的字符串中如果标注var[0:3]，那么其实是0、1、2三个位置的字符，并不包含3位置的字符。

例如：

```python
var = "Hello World!"
print(var[1]) #输出的是第2个字符
print(var[0:5]) #输出的是从第1个到第5个字符
print(var[-1]) #输出的是最后一个字符
```

输出为：

```bash
e
Hello
!
```

### 1.5.2 拼接与复制

在Python中可以使用“+”来连接两个字符串，例如：

```python
var1 = "Hello"
var2 = "World"
var3 = var1 + var2
```

那么在上面这段程序中`var3`里面存放的就是`“HelloWorld”`

还可以使用“*”来复制字符串，例如：

```python
var1 = "Hello"
var2 = var1 * 2
```

那么变量`var2`中存放的就是`“HelloHello”`

### 1.5.3 字符串比较

在字符串同样可以进行比较操作，例如：

```python
a = "abed"
b = "abce"
if a>b:
	print(a)
else:
	print(b)
```

在字符串比较中，会从0位置开始依次、一一对应地比较。比较方式很简单，按照字母顺序比较（在本质上时ASCII码的比较，有兴趣自己查询），字符串的大小取决于计算机取到的第一个不相同的位置的字符大小。

例如在上面这个例子中，字符串a和字符串b的0、1位置都相同，在第2位置上“e”>"c"，所以字符串a比字符串b大，后续的位置无需比较。

###  1.5.4 常用函数

- `len()`函数获取字符串长度

  例如：

  ```bash
  >>>str = "runoob"
  >>> len(str)             # 字符串长度
  6
  >>> l = [1,2,3,4,5]
  >>> len(l)               # 列表元素个数
  5
  ```

## 1.6 数组(列表)操作

