# list

list是一种有序的和，可以随时添加和删除其中的元素。

使用索引来访问list中的每一个位置的元素，索引是`0`从开始的：
```
>>> classmates = ['Michael', 'Bob', 'Tracy']
>>> classmates
['Michael', 'Bob', 'Tracy']

>>> len(classmates)
3

>>> classmates[0]
'Michael'
>>> classmates[1]
'Bob'
>>> classmates[2]
'Tracy'
>>> classmates[3]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
```

list是一个可变的有序表，所以，可以往list中追加元素到末尾：
```
>>> classmates.append('Adam')
>>> classmates
['Michael', 'Bob', 'Tracy', 'Adam']
```
也可以把元素插入到指定位置，比如索引号为`1`的位置：
```
>>> classmates.insert(1, 'Jack')
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy', 'Adam']
```
要删除list末尾的元素，用pop()方法：
```
>>> classmates.pop()
'Adam'
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy']
```
pop(i)方法可以删除指定位置的元素

要把某个元素替换成别的元素，可以直接赋值给对应的索引位置：
```
>>> classmates[1] = 'Sarah'
>>> classmates
['Michael', 'Sarah', 'Tracy']
```

**list里的元素的数据类型可以不同**

list元素也可以是另一个list

如果一个list中一个元素也没有，它的长度为0。

# tuple

tuple和list类似，但tuple一旦初始化就不能修改，它没有append(),insert()这样的方法，其他获取元素的方法和list是一样的，但不支持赋值。

定义一个只有1个元素的tuple，必须加一个逗号`,`，来消除歧义：
```
>>> t = (1,)
>>> t
(1,)
```
如何做一个可变的tuple？

```
>>> t = ('a', 'b', ['A', 'B'])
>>> t[2][0] = 'X'
>>> t[2][1] = 'Y'
>>> t
('a', 'b', ['X', 'Y'])
```
如何理解上边的代码？
tuple所谓的不变，是指指向永远不变，即指向`a`，就不能指向`b`，指向一个list，就不能指向其他对象，但list本身是可以变的！

