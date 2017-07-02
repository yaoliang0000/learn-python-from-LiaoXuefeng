# Python能够处理的数据类型：

- 整数

- 浮点数

	整数和浮点数在计算机内部存储的方式是不同的（？），整数运算永远是精确的，而浮点数运算则可能会有四舍五入的误差。
- 字符串

	字符串是单引号`'`或双引号`"`括起来的任意文本，如果字符串既包括`'`又包括`"`怎么办？这里需要用到转义字符`\`进行标识：
    
	`'I\'m \"OK\"!` 代表的字符串为 I'm "OK"!

	转义字符`\`可以转义很多字符，例如`\n`表示换行，`\t`标识制表符，`\\`表示`\`

`
	
	>>> print('I\'m ok.')
	I'm ok.
	>>> print('I\'m learning\nPython.')
	I'm learning
	Python.
	>>> print('\\\n\\')
	\
	\
	

当需要转义的`\`太多时，使用转义符就很麻烦，这是Python中的自然语言r就派上了用场，`r''`表示`''`中的内容都不转义

`

	>>> print('\\\t\\')
	\       \
	>>> print(r'\\\t\\')
	\\\t\\

同样的，`\n`可以使用`'''...'''`代替

`

	>>> print('''line1
	... line2
	... line3''')
	line1
	line2
	line3

- 布尔值

布尔值在Python中只有`True`，`False`两种值，**注意大小写**

`

	>>> True
	True
	>>> False
	False
	>>> 3 > 2
	True
	>>> 3 > 5
	False

布尔值可以用`and`，`or`，和`not`运算

`

	and运算是与运算，只有所有都为True，and运算结果才是True：

	>>> True and True
	True
	>>> True and False
	False
	>>> False and False
	False
	>>> 5 > 3 and 3 > 1
	True

	or运算是或运算，只要其中有一个为True，or运算结果就是True：

	>>> True or True
	True
	>>> True or False
	True
	>>> False or False
	False
	>>> 5 > 3 or 1 > 3
	True

	not运算是非运算，它是一个单目运算符，把True变成False，False变成True：

	>>> not True
	False
	>>> not False
	True
	>>> not 1 > 2
	True

- 空值

None <> 0,在Python中，None是一个特殊的空值


# Python中的变量


** 变量名必须是大小写英文、数字和`_`的组合，且不能用数字开头**

Python采用的是动态语言，变量本身类型不固定；
Jave是静态语言，定义变量时必须制定变量类型；

赋值语句是从右侧开始计算的，例如：

	x = 10
	x = x + 2

# Python中的常量

在习惯上，Pthon用全部大写的变量名表示常量（只是习惯用户，不固定，但应该被遵守）

- 除法的三种方式
	- `/` and `//` and `%`

`

	>>> 10 / 3  #整数的除法结果永远是浮点数
	3.3333333333333335
	>>> 9 / 3  #整数的除法结果永远是浮点数
	3.0
	
	>>> 10 // 3 # // 取整
	3

	>>> 10 % 3 # % 取余
	1