# Python第一阶段
## 1. Python的安装和简介

### 1.1 Python基础常识

#### 1.1.1 简介

Python是一门面向对象的解释性计算机设计语言

#### 1.1.2 Python语言特色

1. python是一门解释性语言
   * 解释性语言：在系统中运行时需要使用解释器（如Java、php等）
   * 编译性语言：在系统中运行时不需要使用解释器（如C，C++）
2. 弱类型语言
   * 弱类型语言：变量在使用之前不需要提前声明变量的类型就可以直接使用
   * 强类型语言：变量在使用之前需要提前声明变量的类型
3. 面向对象的语言
   * Python支持面向对象的编程，也在一定程度上支持面向过程和面向函数
4. 胶水语言
   * Python的底层和扩张库都是由C语言写成，可以很好支持C和C++

#### 1.2.3 Python语言的优点

1. 简单
2. 易学
3. 速度快（这里指python的开发速度相对较快，python的运行速度相对一般）
4. 免费，开源
5. 高层语言（这里的高低指的是距离硬件的远近，python距离硬件相对比较远）
6. 可移植性（python在linux，windows，mac os都可以使用）
7. 可扩张性
8. 可嵌入性

### 1.2 Python安装及版本检测

#### 1.2.1 Python windows上安装需要注意事项

勾选add python to paith 若没有勾选就需要手动去配置环境变量

#### 1.2.2 Python版本检测

1. 方法一：在cmd中直接输入python，第一行会显示python的当前版本
2. 方法二：在cmd中输入python -V 
3. 方法三：打开idle

## 2. Python基本语法

### 2.1 注释、语句分类、关键字

#### 2.1.1 注释

* 定义：即注解，解释。分为单行注释和多行注释

* 作用：

  ```
  1.给代码做出标注，进行解释和说明。方便别人阅读和理解代码
  2.在debug的时候，可以通过注解来一行一行查找问题
  ```

##### 2.1.1.1 单行注释

以#号开始，#后面的内容就是注解的内容。计算机不会去阅读#后面的内容

##### 2.1.1.2 多行注释

以''' 或者""" 将注释内容包裹起来

##### 2.1.1.3 注释的选择原则

单行注释 # 里面可以使用多行注释 ''' 或者 """

多行注释''' 或者 """ 里面可以使用单行注释# 

多行注释中可以使用另一种多行注释。如：''' 中可以使用"""   在"""中可以使用'''

#### 2.1.2  Python 语句分类

Python语句分为 单行语句 和 代码组（代码块）

单行语句：一行python代码

代码组：特定的语言结构，标志是：和缩进（如if ，while等）

#### 2.1.3  关键字

* 定义：关键字指系统已经使用的具有特殊功能的保留标识符

* 查看系统保留关键字的方法：

  ```
  import keyword
  print（keyword.kwlist）
  ```

## 3. Python变量及数据类型

### 3.1 变量

* 变量的定义：变量就是可以变化的量（在Python中更像是把变量的值贴到值上面，之后使用这个值就直接用贴在它上面的名字即可）

* 变量赋值：（三种方式）

  ```
  方法一：（基本格式）
  	变量 = 值
  方法二：（给多个变量赋相同的值）
  	变量1 = 变量2 = 变量3 ... = 值
  方法三：（给多个变量赋不同的值）
  	变量1，变量2，变量3... = 值1，值2，值3...
  ```

* 获取变量的类型：（两种方法）

  ```
  1. type（）
  	print（type（变量））
  2. isinstance（）-------> isinstance（查看的变量，类型）  返回的值是bool True or False
  	print（isinstance（4，int））
  ```

* 获取变量在内存中的id：

  ```
  id（）
  	print（id（变量））
  ```

* 更改变量的值：（对变量重新赋值即可）

  ```
  val = 1
  val = 2
  print(val)
  ```

* 变量的命名规则：

  ```
  1. 使用英文，禁止使用中文
  2. 可以使用数字，但是不能用数字开头
  3. 特殊符号只能使用下划线_ 
  4. 区分大小写
  5. 命名必须要有意义
  6. 避免和系统保留的关键字冲突
  ```

### 3.2 数据类型

1. Number     整型		(包含 ：int、float、bool、complex)
2. String        字符串      
3. List            列表            
4. Tuple         元组       
5. Set            集合            
6. Dict           字典 

ps：

```
* Number中包含： int、float、bool、complex
* 容器数据类型： String、List、Tuple、Set、Dict
* 有序数据类型： String、List、Tuple
* 无序数据类型： Set、Dict
```

#### 3.2.1 Number类型

##### 3.2.1.1  Number类型：int

* int整型的声明方式：（十进制、二进制、八进制、十六进制）

  ```
  1. 十进制（0-9）
  	变量 = 十进制数字
  2. 二进制（0-1）
  	变量 = 0b二进制数字
  3. 八进制（0-7）
  	变量 = 0o八进制数字
  4. 十六进制（0-9a-f）
  	变量 = 0x十六进制数字
  ```

##### 3.2.1.2 Number类型：float

* float浮点型声明方式：（小数和科学记数法）

  ```
  1. 小数：
  	变量 = 带小数点的数字
  	num = 3.14
  2. 科学计数法   e相当于10    
  	变量 = 314e-2
  ```

##### 3.2.1.3 Number类型：bool

* bool类型只有两个值：True  和 False   （True和False的首字母都要大写！）
* True：表示肯定的，确定的答案
* False：表示否定的答案

##### 3.2.1.4 Number类型：complex

* 复数定义：由实数部分和虚数部分组成，实数部分是实际存在的数字，虚数部分是现实世界中不存在的数字。在计算机中虚数的单位为j。

* 声明一个复数的方法：

  ```
  方法一：
  	变量 = a + bj
  方法二：
  	变量 = complex（实数 + 虚数）           实数和虚数都只要填入纯数字即可，虚数部分不需要填入单位：j
  	如：
  	complex1 = complex（3，4）   ==     complex1 = 3 + 4j
  ```


##### 

#### 3.2.2 String 字符串类型

* String在所有语言中都是使用最多的数据类型

* String类型声明方式：（三种）

  ```
  方法一：单引号 ''
  	变量 = '字符串内容'
  方法二：双引号 " "
  	变量 = "字符串内容"
  方法三：三引号 ''' ''' 或者 """  """
  	变量 = '''字符串内容'''  或者   变量 = """字符串内容"""
  ```

* String声明方式选择原则：

  ```
  1. 单引号中可以使用双引号
  2. 双引号中可以使用单引号
  3. 三引号中可以使用单双引号
  ```

* 转义字符：\

  ```
  1. 转义单引号：\'   （使单引号失去原有的特殊意义）
  	str1 = '古人说：\'nnb\''
  2. 转义双引号：\"	  （使双引号失去原有的特殊意义）
  	str1 = "古人说，\"nnb\""
  3. 换行操作符：\n
  	str1 = "人之初，\n性本善。"
  4. 缩进操作符：\t
  	str1 = "\t人之初，性本善"
  5. 对\自身进行转义：\\
  	str1 = '在字符串中输出\\'
  6. 续行符：\
  	str1 = '在单行语句末尾加上\'
  			a = '你好'\
            '党元'
        >>>'你好党元'
  7. 原字符串：在字符串前面加上 r 或者 R ，转义字符串中所有的字符
  	str1 = r'你好，\n再见\t！'
  ```

#### 3.2.3 List 列表类型

* 列表类型的标志：[ ] 中括号

* 列表的声明方式：

  ```
  变量 = [值1，值2，值3......]
  ```

* 创建一个空列表：

  ```
  方法一：	变量 = []
  方法二：	变量 = list()
  ```

* 列表索引值

  ```
  正向索引： 0   1   2   3   4
  list1 = [100,200,300,400,500]
  反向索引：-5  -4  -3  -2  -1
  ```

* 通过索引访问和修改列表中特定的值

  ```
  列表[index]
  列表[index] = 新的值     可以通过下标来修改列表中的值
  ```

#### 3.2.4 Tuple 元组类型

* 元组类型的标志：，逗号

* 元组类型的声明方式：

  ```
  方法一：
  	变量 = (值1，值2，值3....)
  方法二：
  	变量 = 值1，值2，值3....
  ```

* 元组索引值

  ```
  正向索引    0   1   2   3   4
  tuple1 = (100,200,300,400,500)
  反向索引   -5  -4  -3  -2  -1
  ```

* 通过索引查看元组中的某个值

  ```
  元组[index]
  元组中的值不能随意修改
  ```

#### 3.2.5 Set 集合类型

* 集合的标志：无

* 集合是无序容器，无法通过索引来访问其中的某个值

* 集合中所有的数据都是唯一的，出现重复的会只保留唯一的其他删除

* 集合的声明方式：

  ```
  	变量 = {100,200,300,400,500}
  ```

* 创建空集合：

  ```
  	变量 = set（）
  ```

#### 3.2.6 Dict 字典类型

* 字典的标志：{ } 

* 字典是无序数据，无法通过索引来访问其中的某个值

* 字典的声明方式：

  ```
  	变量 = {键：值，键：值，键：值...}
  ```

* 访问和修改字典中的值 ：

  ```
  字典是无序容器，不能使用索引来访问字典中的值。但是可以通过字典特有的键来访问字典中的值：
  	dict[键]
  修改字典中的值：
  	dict[键] = 新的值
  ```

* 创建一个空字典：

  ```
  变量 = dict()
  	dict1 = dict()
  变量 = {}
  	dict1 = {}
  ```

#### 3.2.7 查看数据类型的方法

##### 3.2.7.1 type（）

正常工作的时候不能用，因为效率太低了。工作原理是把目标数据和所有数据类型一一匹配询问，找到同目标数据类型相同的类型。

```
	result = type（变量名）
	print（result）
```

##### 3.2.7.2 isinstance（）

工作效率比较高，把目标变量和指定的类型做比对，如果目标变量和指定类型为相同类型，则返回True；否则返回False

```
* 方法一，使用isinstance查看单一类型
	isinstance(变量，类型)
	如：
	var = 123
	result = isinstance(var,int)
	print(result)

* 方法二，使用isinstance查看目标变量是否属于两个类型中
	isinstance（变量，(类型一，类型二)）
	如：
	var = 123
  result = isinstance(var,(int,str))
  print(result)
```



### 3.3 数据类型转换

#### 3.3.1 自动数据类型转换

1. 自动数据类型转换是系统自发的，不需要人工干预的

2. 自动数据类型转换会从精确度较小的数据类型向精确度较高的数据类型进行转换

3. 自动数据类型转换多发生在运算或者判断的时候

   ```
   如：
   	num1 = 25
   	num2 = 25.0
   	print(num1 + num2)
   又如：
   	if 1:
   		print('1会自动转化成True')
   ```

#### 3.3.2 强制数据类型转换

##### 3.3.2.1 int（）

将其他数据类型转换成整型

```
整型：		 无需转换
浮点数：	去掉小数部分，只保留整数部分
布尔值：	True 转换成 1，False 转换成 0
复数：		 复数无法转换成整型
字符串：	只有纯整数字符串才能转换成int。
列表，元组，集合，字典都不能转换成整型
```

##### 3.3.2.2 float（）

将其他数据类型转换成浮点数

```
整型：		在整数后面加上.0
浮点数：    无需转换
布尔值：	True 转换成 1.0     False 转换成 0.0
复数：		复数无法转换成浮点数
字符串：	只有纯整数字符串和纯浮点数字符串才能转换成浮点数
列表，元组，集合，字典都不能转换成浮点数
```

##### 3.3.2.3 bool（）

其他类型中，相当于bool中的False的情况

```
整型：		  0
浮点型： 	 0.0
bool：	   False
复数：		 0j  或者  0+0j
字符串：	''(空字符串)
列表：		 [] 或者 list() 
元组：		 () 或者 tuple()
集合：		 set()
字典：	 	 {} 或者 dict()
```



##### 3.3.2.4 complex()

其他类型转换成复数complex（）

```
整型：		 整型+0j
浮点数：	浮点数+0j
布尔值：	True：1+0j    False：0j 或者 0+0j
复数：	 	 无需转换
字符串：	字符串中只有纯整数，纯浮点数或者纯复数才能转换成复数
列表、元组、集合、字典都不能转换成复数
```



##### 3.3.2.5 str（）

其他类型转换成字符串

```
所有类型都可以转换成字符串，系统会自动给其他类型加上''让它变成字符串
如果要打印出带引号的字符串，可以使用命令repr()
	如： 
	list1 = [1,2,3]
	list1 = str(list1)
	print(repr（list1）)
```



##### 3.3.2.6 list（）

其他类型转换成列表

```
整型、浮点型、复数、布尔值都不能转换成列表
字符串：字符串转换成列表，把字符串中的每个值转换成列表中的每一个值，顺序保持不变
列表： 无需转换
元组： 把元组中的每个值转换成列表中的值，顺序保持变
集合： 把集合转换成列表中的每一个值，顺序随机
字典： 把字典中的键转换成列表中的值，顺序随机
```



##### 3.3.2.7 tuple（）

其他类型转换成元组

```
整型、浮点数、复数、布尔值都不能转换成元组
字符串：字符串中的每个字符转换成元组中的一个值，顺序不变
列表： 列表中的每一个值转换成元组中的值，顺序不变
元组： 无需转换
集合： 集合中的每个值转换成元组中的每个值，顺序随机
字典： 字典中的每个键转换成元组中的一个值，顺序随机
```



##### 3.3.2.8 set（）

其他类型转换成集合

```
整型、浮点型、复数、布尔值都不能转换成集合
字符串： 字符串中的每个字符转换成集合中的一个值，顺序随机
列表： 列表中的每个值转换成集合中的一个值，顺序随机
元组： 元组中的每个值转换成集合中的一个值，顺序随机
集合： 无需转换
字典： 字典中的每个键转换成集合中的一个值，顺序随机
```



##### 3.3.2.9 dict（）

其他类型转换成字典

```&amp;amp;#39;&amp;amp;#39;
* 整型、浮点型、复数、布尔值都不能转换成字典
* 字符串： 不能转换成字典
* 列表： 只有特定的列表格式可以转换成字典
	1. 二级列表（且第二级容器的长度一样）
	list1 = [[键，值],[键，值],[键，值],[键，值],[键，值]]		or  	list1 = [(键，值),(键，值),(键，值),(键，值)]
	
	2. 一级列表：只含有两个字符的一级列表
	list1 = ['键值','键值','键值','键值']

* 元组： 只有特定的元组格式才可以转换成字典
	1. 二级元组（且第二级容器的长度一样）
	tuple1 = ((键，值),(键，值),(键，值),(键，值))
	
	2. 一级元组：只含有两个字符的一级元组
	tuple1 = （'键值','键值','键值','键值'）
	
* 集合： 只有特定的集合格式才可以转换成字典
	1. 二级集合（且第二级容器的长度一样）
	set1 = {(键，值),(键，值),(jia),()}
```
## 4. Python运算符

1. 算术运算符
2. 比较运算符（关系运算符）
3. 逻辑运算符
4. 位运算符
5. 赋值运算符
6. 成员运算符
7. 身份运算符

### 4.1 算术运算符

```
**		幂运算（最高优先级）
*		乘法运算
/		除法运算
//		取商运算（地板除）
%		取余运算
+		加法运算
-		减法运算
```

### 4.2 比较运算符（关系运算符）

比较运算符运算结果为布尔值：	True 、False

```
<=		小于等于
>=		大于等于
<		小于
>		大于
==		等于
!=		不等于
```

### 4.3 赋值运算符

变量 = 变量 操作符 值 -------------------------------> 变量 操作符= 值

```
**=		幂运算赋值
*=		乘法赋值
/=		除法赋值
//=		取商赋值
%=		取余赋值
+=		加法赋值
-= 		减法赋值
=		普通赋值
```

### 4.4 逻辑运算

逻辑运算是布尔值之间的运算

1. not 逻辑非运算 （逻辑运算中优先级最高）

   ```
   真变假，假变真
   not True == False
   not False == True
   ```

2. and 逻辑与运算

   ```
   有假则假
   只有当 and 左右的两个条件都满足的时候 and 的结果才是为真
   True and False == False
   True and True == True
   False and False == False
   ```

3. or 逻辑或运算

   ```
   有真则真
   当 or 左右两个条件有一个满足，则 or 的结果就是为真
   True or False == True
   False or False == False
   True or True == True
   ```

4. xor 逻辑异或运算

   ```
   不同为真，相同为假
   在python中不支持异或操作。
   True xor False == True
   True xor True == False
   False xor False == False
   ```

### 4.5 位运算符

位运算就是在二进制基础上进行的逻辑运算

```
&		按位与运算
|		按位或运算
~		按位反转
^		按位异或运算
<<		左移			<< 1 左移1位，相当于*2
>>		右移			>> 1 右移1位，相当于//2
```

### 4.6 成员运算符

检测变量是否在容器类数据中

```
in ：
	变量 in 容器类数据（string,list,tuple,set,dict），检测字典的时候，只检测字典的键
	检测变量是不是在容器中
	
not in :
	变量 not in 容器类数据
	检测变量是不是不在容器中
```

### 4.7 身份运算符

判断两个变量在内存中的地址是否相同。

```
is：
	检测两个变量是否是同一个值

is not：
	检测两个变量是否不是同一个值
```

```
当数值相同的时候，哪些数据类型的id会相同
1. 整数：	-5以上的整数
2. 浮点数： 0以上的浮点数
3. 布尔值： 永远相同
4. 复数：	实数部分为0，虚数部分在0j以上
5. 字符串： 永远相同 
```



## 5.流程控制

1. 流程:

   ```
   做事情的顺序就是流程,计算机中的流程就是代码执行的顺序.默认是从上到下
   ```

2. 流程分类:

   1. 顺序结构
   2. 分支结构(单向分支,双向分支,多向分支,巢状结构)
   3. 循环结构(while循环  死循环  for...in循环)

### 5.1 顺序结构

python默认的代码执行顺序,默认从上到下执行代码



### 5.2 分支结构

#### 5.2.1 单向分支

基本格式:

```
if 条件判断:
	条件为真时,执行语句
	...
```

如:

```
num = 10
if num > 9:
	print(num)
```



#### 5.2.2 双向分支

基本格式:

```
if 条件判断:
	条件为真的时候执行代码
	...
else:
	条件为假的时候执行代码
	...
```

如:

```
num = 10
if num > 10:
	print(num)
else:
	print(num,'比10小')
```



#### 5.2.3 多向分支

基本格式:

```
if 条件1判断:
	条件1为真的时候执行代码
	...
elif 条件2判断:
	条件2为真的时候执行代码
	...
elif 条件3判断:
	条件3为真的时候执行代码
	...
else:
	条件1,条件2,条件3都不满足执行代码
	...

```

如:

```
day = 1
if day == 1:
	print('黄焖鸡')
elif day == 2:
	print('面条')
elif day == 3:
	print('快餐')
elif day == 4:
	print('汉堡')
else:
	print('不吃了')
```



#### 5.2.4 巢状分支

基本结构:

```
if 条件1判断:
	条件1满足执行代码
	if 条件2判断:
		条件2满足执行代码
		if 条件3判断:
			条件1,条件2,条件3都满足执行代码
		else:
			条件3不满足执行代码
	else:
		条件2不满足执行代码
else:
	条件1不满足执行代码
```

如:

```
schooldoor = True
buildingdoor = True
classdoor = True


if schooldoor == True:
	print('校门开了,走到教学楼')
	if buildingdoor == True:
		print('教学楼门开了,走到教室')
		if classdoor == True:
			print('教室门开了,走进教室开始学习')
		else:
			print('教室门没开,班长帮忙开个门')
	else:
		print('教学楼门没开,班主任帮忙开个门')
else:
	print('校门没开,大爷帮忙开个门')
	
	
```



### 5.3 循环结构

#### 5.3.1 while 循环

基本格式:

```
while 条件判断:
	条件为真时,执行代码
	....
```

如: 计算0-100(包含100)所有数之和

```
num = 0
total = 0
while num <= 100:
	total += num
	num += 1
print(total)
```

又如: 输出十行十列的星星

```
i = 0
while i < 10:
	j = 0
	while j < 10:
		print('✨',end= '')
		j += 1
	
	print('\n',end='')
	i += 1
```

又如: 使用单循环输出10行10列的星星

```
i = 0
while i < 100:
	print('✨',end = '')
	if i % 10 == 9:
		print()
	i += 1
```

又如: 输出十行十列星星,隔行变色

```
i = 0 
while i < 10:
	j = 0
	while j < 10:
		if i % 2 == 0:
			print('✨',end = '')
		else:
			print('❤️',end = '')
		j += 1
		
	print()
	i += 1
```

又如: 使用单循环实现隔行变色

```
i = 0
while i < 100:
	if (i // 10) % 2 == 0: 
		print('✨',end = '')
	else:
		print('❤️',end = '')
	if i % 10 == 9:
		print()
	i += 1
```



#### 5.3.2 死循环

基本格式:

```
while True:
	循环内容
	...	
```

如: 判断用户输入的密码是否正确

```
error = False
passwd = 123

while True:
	userinput = input('请输入密码:')
	
	# 检查密码格式是否正确
	for each in userinput:
		if each not in '0987654321':
			error = True
			break
	
	if error == True:
		print('密码格式错误,请重新输入纯数字密码!')
		error = False
		continue
	else:
		if userinput == str(passwd):
			print('密码正确,登录成功!')
			break
		else:
			print('密码错误,请重新输入!')
		
```



#### 5.3.3 for … in 循环

基本格式:

```
for 变量 in 容器:
	循环体
	...
```



遍历除字典外的不等长的二级容器(列表,元组,集合)

```
for 变量1 in 容器:
	for 变量2 in 变量1:
		循环体
		...
```



遍历字典中的键和值:

```
for key in dict1:
	print(key,dict1[key])
	
或者

for key,value in dict1.items():
	print(key,value)
```



遍历等长的二级容器;

```
list1 = [
  ['a','b','c'],
  ['d','e','f'],
  ['g','h','i']
]
for x,y,z in list1:
	print(x,y,z)
```



#### 5.3.4 break 和 continue 

break: 终止循环

如: 输出0-100(包含100)的数字,遇到44则停止循环

```
i = 0:
while i <= 100:
	if i == 44:
		break
	print(i)
	i += 1
```



continue: 跳过本次循环,开始下一次循环. 开始下一次循环的同时要进行判断

如: 输出0 -100(包含100)的数字,遇到任何带4的则跳过

```
i = 0
while i <= 100:
	if i % 10 == 4 or i // 10 == 4:
		i += 1
		continue
	else:
		print(i)
		i += 1
```



## 6.函数

* 定义: 把具有特定功能的代码打包就是函数
* 作用
  1. 提高代码的复用率
  2. 提高开发效率
  3. 便于程序的维护

### 6.1 函数声明方式

def 函数名( ) :

​	pass(函数内容)



函数名( )	# 调用函数



### 6.2 函数名命名规则

1. 使用英文,禁止使用中文
2. 可以使用数字,但是不能用数字开头
3. 所有的符号只能用_下划线
4. 命名要有意义
5. 严格区别大小写
6. 避免和系统保留的关键字重名
7. 避免和系统保留的函数重名



### 6.3 函数的参数

#### 6.3.1 形参

函数在定义过程中,( )中的参数就是形参.形参没有实际意义,只是为了占位接收实参的值

##### 6.3.1.1 普通形参

* 没有实际意义,只是为了占位,等待接收实参对他赋值.
* 如果定义了形参,形参也没有设置默认值,那么在调用函数的时候如果没有实参就会报错

如:

```
def hanshu(a,b):
	print(a)
	print(b)
hanshu(1,2)
```

##### 6.3.1.2 带有默认值的形参

* 在函数定义的时候如果给了形参默认值,那么就是带有默认值的形参
* 那么如果调用的时候如果没有传入实参,形参会按默认值进行运算
* 若调用的时候传入了实参,那么实参的值会覆盖形参的默认值,按实参的值进行运算

如:

```
def hanshu(a = 1, b = 2):
	print(a)
	print(b)


hanshu()
hanshu(3,5)
```



##### 6.3.1.3 普通收集形参 * 

* 在不确定有多少实参传入的时候,可以使用普通收集形参:    * 变量名
* 收集到的实参会组成一个元组
* 形参优先级: 普通形参 > 普通收集形参 > 关键字收集形参

如:

```
def hanshu(*tuple1):
	total = 0
	for each in tuple1:
		total += each
	print(total)

hanshu(1,2,3,4,5,6,7)
```



##### 6.3.1.3 关键字收集形参 **

* 关键字收集形参只能收集关键字实参的值
* 收集到的关键字实参会组成一个字典,关键字作为字典的键,实参的值作为字典的值
* 形参优先级: 普通形参 > 普通收集形参 > 关键字收集形参

如: 传入人名和年纪,计算总和

```
def age(**dict1):
	total = 0
	for key in dict1:
		total += dict1[key]
	print(total)

age=(变量1=数值1,变量2=数值2,.....)
```



#### 6.3.2 实参

##### 6.3.2.1 普通实参

* 在调用函数的时候,( )中的值就是实参.若没有通过关键字的方式进行传参的就是普通实参
* 实参的优先级: 普通实参 > 关键字实参

如:

```
def hanshu(a):
	print(a)

hanshu('哗啦啦')
```



##### 6.3.2.2 关键字实参

* 在调用函数的时候,通过关键字=值的方式来进行传参,这就是关键字实参
* 实参的优先级: 普通实参 > 关键字实参

如:

```
def hanshu(a,b):
	print(a)
	print(b)

hanshu(a='关键',b='字')
```



### 6.4 函数的返回值

* 函数按照有无返回值可以分为两类:

   1. 有返回值的函数 — 含有return , 函数执行之后,会返回一个结果,可以用变量接受
    2. 执行过程的函数 — 没有返回值的函数, 没有return , 函数执行只有不会返回一个结果,用变量接受为 none

* return的作用

1. 为函数的运行返回一个结果
2. 终止函数执行,一旦函数运行到了return,则在return之后的代码将不会运行





### 6.5 函数文档

#### 6.5.1 查看函数文档的方法

* 方法一: 	help( ) —help(函数名)

  如: 

  ```
  help(print)

  help(id)

  help(type)

  ```

  ​



* 方法二:	函数名. _ _ _doc_ _ _ 

  如:

  ```
  print.__doc__

  id.__doc__

  type.__doc__
  ```



#### 6.5.2 定义函数文档的方法

```
def 函数名():
	'''
	功能:
	参数:
	返回值:
	'''
	
	函数内容...
	
	
```



### 6.6 变量的作用域

#### 6.6.1 全局变量

1. 在任何区域或者页面都有效的变量
2. 在全局环境中直接声明的变量就是全局变量
3. 在局部环境中修改全局变量的值需要使用global关键字

```
var = '我是全局变量'
def hanshu():
	jubuvar = '我是局部变量'
	
```



#### 6.6.2 局部变量

1. 在特定的局部区域有效的变量就是局部变量
2. 在函数内部(局部环境中)声明的变量就是局部变量
3. 在内部函数中修改内部函数外部的非全局变量,需要使用nonlocal关键字

#### 6.6.3 局部变量和全局变量的关系

1. 在全局环境中不能直接使用局部变量和内部函数,需要闭包之后才能使用
2. 在局部环境中可以访问全局变量,但是不能修改全局变量的值,需要使用global关键字

#### 6.6.4 global 关键字

1. 作用一: 使全局变量能进入局部环境

   ```
   var = '我是全局变量'

   def hanshu():
   	global var
   	var = '全局变量进入局部环境,修改全局变量'
   	
   hanshu()
   print(var)
   ```

2. 作用二: 将局部变量升级为全局变量

   ```
   def hanshu():
   	global var
   	var = '我升级成全局变量'

   hanshu()
   print(var)
   ```



#### 6.6.5 内部函数

1. 定义: 在一个函数的内部在定义一个函数,再定义的函数就是内部函数. 内部函数本质上相当于一个局部变量

   ```
   def outer():
   	def inner():
   		print('我是内部函数')
   	inner()

   outer()
   ```



2. 内部函数的作用域:
     1. 内部函数不能直接在全局环境中使用,需要使用闭包将它带到全局环境中
       2. 在函数内部可以调用内部函数
       3. 在函数内部需要先定义内部函数,之后才能调用



#### 6.6.6 闭包

1. 定义: 让局部变量和内部函数在函数的外部可以使用即闭包
2. 作用: 让局部变量和内部函数突破局部作用域

闭包实现方法:

       	1. 方法一: 使用global关键字实现闭包

```python
lists = []

def hanshu():
	global lists  # 利用global修改全局变量
	
	a = '局部变量a'
	b = '局部变量b'
	
	def inner1():
		print('内部函数inner1')
	def inner2():
		print('内部函数inner2')
	
	lists = [a,b,inner1,inner2]   # 将内部变量、函数封装在一个全局变量列表中，因为上面对全局变量lists定义了global

hanshu()

# 通过读取列表中元素，以达到调用局部变量函数的目的
num_a = lists[0]
num_b = lists[1]
neibu1 = lists[2]
neibu2 = lists[3]

# 最终达到局部函数在全局使用
neibu1()
neibu2()
```



2. 方法二: 使用return实现闭包

```python
def hanshu():
	
	a = '局部变量a'
	b = '局部变量b'
	
	def inner1():
		print('我是内部函数inner1')
	def inner2():
		print('我是内部函数inner2')
	
	return [a,b,inner1,inner2]  #使用return返回变量，函数去实现闭包

lists = hanshu()

num_a = lists[0]
num_b = lists[1]
neibu1 = lists[2]
neibu2 = lists[3]

neibu1()
neibu2()
```



3. 方法三: 使用return内部函数实现闭包

```python
def hanshu():
	
	a = '局部变量a'
	b = '局部变量b'
	
	def inner1():
		print('我是内部函数inner1')
	def inner2():
		print('我是内部函数inner2')
	
	def bibao():
        '''构建一个函数用于返回局部变量，局部函数'''
		return [a,b,inner1,inner2] 
	
	return bibao   #返回函数bibao以实现闭包
	

result = hanshu()
lists = result()

num_a = lists[0]
num_b = lists[1]
neibu1 = lists[2]
neibu2 = lists[3]

neibu1()
neibu2()
```



#### 6.6.7 nonlocal 关键字

用于在内部函数中修改内部函数外部的非全局变量的值

如:

```python
def user():
	
	jubuvar = '我是局部变量'
	
	def change(newvar):
		nonlocal jubuvar   # 修改内部局部变量的值
		jubuvar = newvar
	
	def look():
		print(jubuvar)
	
  # 用return实现闭包
	def bibao():
		return [jubuvar,change,look]
	
	return bibao

result = user()
lists = result()

jubu = lists[0]
modif = lists[1]  #change函数
kan = lists[2]

modif('修改局部变量')

kan()  #输出全局变脸的值

```

---

### 6.7 lambda(匿名函数)表达式

1. 基本格式:

   ```python
   函数名 = lambda 形参1,形参2,... : (自带return) 函数内容
   ```

   如:

   ```python
   total = lambda no1,no2,no3 : no1 + no2 + no3

   result = total(1,2,3)
   print(result)
   ```

2. 带有分支结构的lambda表达式:

   ```python
   函数名 = lambda 形参1,形参2,... : 条件为真时执行结果 if 条件判断 else 条件为假时执行结果
   ```

   如:

   ```python
   large = lambda no1,no2 : no1 if (no1 > no2) else no2
   ```

   又如:

   ```python
      # 匿名函数表示if...else嵌套
      large1 = lambda no1, no2, no3: no1 if (no1 > no2 and no1 > no3) else (no2) if no2 > no3 else no3
      # 调用匿名函数
      max1 = large1(5,56,8)
      print(max1)

      
      # 普通函数表示if...else嵌套
      def large2(a,b,c):
      if a>b and a>c:
          return a
      else:
          if b>c:
              return b
          else:
              return c
      #调用函数
      max2=large2(5,47,9)
      print(max2)
   ```


----

### 6.8 递归函数

在函数中调用函数自身的函数就叫做递归函数

如:

```python
def digui(num):
	
	print(num)
	
	if num > 0:
		digui(num - 1)
	else:
		print('-------------------')
	
	print(num)
```



----

## 7. 字符串

### 7.2 字符串基本操作

1. 字符串连接操作:	 +

   ```python
   string1 = '大风车'
   string2 = '吱呀吱呀转'
   result = string1 + string2 
   print(result)
   ```

2. 字符串复制操作:       *

   ```python
   string1 = '女神'
   result = string1 * 3
   print(result)
   ```

3. 字符串索引操作:      [ ]

   ```python
   string1 = '我是字符串'
   print(string1[4])
   print(string1[-1])
   ```

4. 字符串分片操作:      [::]

   ```python
   # 分片 [起始位置:结束位置:间隔]     --- 不包含结束位置

   string1 = '我是字符串'
   string2 = string1[1:3]
   string3 = string1[::2]
   ```


---

### 7.2 字符串函数

#### 7.2.1 大小写相关



##### capitalize( )	

使字符串第一个第一个字母大写

```python
string1 = 'i love you'
result = string1.capitalize()
print(result)
```



##### title( )

使字符串字母满足标题化格式(所有单词首字母大写)

```python
string1 = 'i love you'
result = string1.title()
print(result)
```



##### upper( )

使字符串中的所有字母都大写

```python
string1 = 'who is your dad ?'
result = string1.upper()
print(result)
```



##### lower( )

使字符串中所有字母都小写

```python
string1 = 'who is your Dad ? '
result = string1.lower()
print(result)
```



##### swapcase( )

将字符串中的大小写互换

```python
string1 = 'I am your Dad !'
result = string1.swapcase()
print(result)
```



#### 7.2.2 获取长度及出现次数

##### len( )

len( )为内置函数

获取字符串或其他容器的长度

```python
string1 = '我是字符串'
result = len(string1)
print(result)
```



##### count( )

count(指定字符,起始,终止)

获取指定字符在指定范围内出现的次数,若没有出现过,返回 0

```python
string1 = 'the only way to longer the day is to steal time from night!'
result = string1.count('o',2,6)
print(result)
```



#### 7.2.3 获取索引值

##### find( )

获取指定字符在字符串中指定范围内*第一次*出现的索引值. 若没有出现则返回 -1

find(指定字符,起始,终止)

```python
string1 = '8000 words in the world, only the love can kill man'
result = string1.find('a')
print(result)
```



##### index( )

获取指定字符在字符串中指定范围内*第一次*出现的索引值,若没有出现则直接报错(ValueError: substring not found)

```python
string1 = '8000 words in the world, only the love can kill man'
result = string1.index('o',2,10)
print(result)  # 6
```



#### 7.2.4 检测类字符串函数

##### startswith( )

检测字符串是否以指定字符在指定范围内*开头*,返回True和False


```python
# startswith(指定字符,起始,终止) 
string1 = 'you are the sun in the world'
result = string1.startswith('a',4,8)
print(result)
```



##### endswith( )

检测字符串是否以指定字符在指定范围内*结尾*,返回True和False


```python
# endswith(指定字符,开始,结束)
string1 = 'you are the sun in the world'
result = string1.endswith('w',-5)
print(result)
```



##### istitle( )

检测字符串是否满足标题格式:检测字符串中所有的单词拼写首字母是否为大写，且其他字母为小写。返回True和False

```python
string1 = 'we all forgot the story of the passtime'
result = string1.istitle()
print(result)
```



##### isupper( )

检测字符串是否满足全部大写，返回True和False

```python
string1 = 'WE ARE THE DOTA-ALLSTARS'
result = string1.isupper()
print(result)
```



##### islower( )

检测字符串是否满足全部字母小写，返回True和False

```python
string1 = 'we are dota-allstars'
result = string1.islower()
print(result)
```



##### isdigit( )  

和 isnumeric(  )  isdecimal(  ) 相同

判断字符串是否全部都是数字，返回True和False

```python
num = '123456'
result = num.isdigit()
print(result)
```



##### isalnum( )

判断字符串是否由字母或者其他文字或者数字组成	(不包含符号)，返回True和False

```python
string1 = 'sad is the reason of thinking too much'
result = string1.isalnum()
print(result)
```



##### isalpha( )

判断字符串是否由字母或者其他文字组成(不包含符号和数字)，返回True和False

```python
string1 = 'these are only words'
result = string1.isalpha()
print(result)
```



##### isspace( )

判断字符串是否由空白字符组成，返回True和False

```python
string1 = '\n\t\r\\ '
result = string1.isspace()
print(result)
```



#### 7.2.5 切割和拼接

##### split( )

将字符串按指定字符进行切割,切割之后放入 *列表* 内

split(指定字符)

```python
string1 = '我-有一剑-可开天门!'
list1 = string1.split('-')
print(list1)
```



##### join( )

用指定字符将*列表*中的元素 *拼接* 成字符串

'指定字符'.join(列表)

```python
list1 = ['我','有一剑','可开天门']
string2 = '!'.join(list1)
print(string2)
```



##### splitlines( )

使用字符串中的换行符号\n来切割字符串(\t制表符不可以)

```python
string1 = '天不生李淳罡,\n剑道万古如长夜'
list1 = string1.splitlines()
print(list1)
```



#### 7.2.6 填充类

##### zfill( )

指定字符长度,用0从左到右进行填充

```python
string1 = '123'
result = string1.zfill(10)
print(result)
0000000123
```



##### center( )

指定字符长度,原字符串 *居中* ,使用指定字符填充到指定长度
center(长度,指定字符)

```python
string1 = '呵呵姑娘'
result = string1.center(10,'_')
print(result)
---呵呵姑娘---
```



##### ljust( )

指定字符长度,原字符串 *居左*,使用指定字符填充至指定长度

ljust(长度,指定字符)

```python
string1 = '呵呵姑娘'
result = string1.ljust(10,'-')
print(result)
呵呵姑娘------
```



##### rjust( )

指定字符长度,原字符串 *居右* ,使用指定字符填充至指定长度

rjust(长度,指定字符)

```python
string1 = '呵呵姑娘'
result = string1.rjust(10,'-')
print(result)

------呵呵姑娘
```



#### 7.2.7 清除字符串类

##### strip( )

清除字符串 *左右两边* 的指定字符

```python
string1 = '___呵呵___'
result = string1.strip('_')
print(result)

呵呵
```



##### lstrip( )

清除字符串 *左边* 指定的字符

```python
string1 = '___呵呵___'
result = string1.lstrip('_')
print(result)

呵呵___
```

##### rstrip( )

清除字符串 *右边* 指定的字符

```python
string1 = '___呵呵___'
result = string1.rstrip('_')
print(reuslt)

___呵呵
```



#### 7.2.8 字符的替换操作

##### maketrans( ) & translate( )

1. maketrans() 方法用于创建字符映射的转换表，对于接受两个参数的最简单的调用方式，第一个参数是字符串，表示需要转换的字符，第二个参数也是字符串表示转换的目标。
注：两个字符串的长度必须相同，为一一对应的关系。
   * 参数：
intab -- 字符串中要替代的字符组成的字符串。
outtab -- 相应的映射字符的字符串。

2. 字符串.translate(字典名)
将字符串按照存有映射关系的字典进行修改

```python
'''这两个方法通常都放在一起使用'''
intab = "aeiou"
outtab = "12345"
str = "this is string example....wow!!!"

trantab =str.maketrans(intab,outtab)
print(trantab)   #>>> {97: 49, 101: 50, 105: 51, 111: 52, 117: 53}

print(str.translate(trantab))   # >>>th3s 3s str3ng 2x1mpl2....w4w!!!
```



#### 7.2.9 format( ) 格式化

##### format( ) 基本格式:

```python
string1 = '{}在{}看见了{}'
result = string1.format('我','莆田','刘姥姥')
print(result)

>>>我在莆田看见了刘姥姥
```

##### format( ) 四种传参方式:

1. 按位置进行传参

```python
string1 = '{}在{}看见了{}'
result = string1.format('我','莆田','刘姥姥')
print(result)

>>>我在莆田看见了刘姥姥
```



2. 按位置标识传参

```python
string1 = '{2}在{1}看见了{0}'
result = string1.format('刘姥姥','莆田','我')
print(result)

>>>我在莆田看见了刘姥姥
```



3. 按关键字传参

```python
string1 = '{who}在{where}看见了{what}'
result = string1.format(what='刘姥姥',where='莆田',who='我')
print(result)

>>>我在莆田看见了刘姥姥
```



4. 使用容器传参

```python
string1 = '{0[0]}在{0[1]}看见了{0[2]}'
result = string1.format(['我','莆田','刘姥姥'])
print(result)

>>>我在莆田看见了刘姥姥
```



##### format( )实现居中 居左 居右

1. 居中填充 center( )     { : 填充字符^长度}

```python
string1 = '我喜欢吃{:*^11}你喜欢么'
result = string1.format('小龙虾')
print(result)

我喜欢吃****小龙虾****你喜欢么
```



2. 居左填充 ljust( )	{ : 填充物<长度}

```python
string1 = '我喜欢吃{:*<11}你喜欢么'
result = string1.format('小龙虾')
print(result)

我喜欢吃小龙虾********你喜欢么
```



3. 居右填充 rjust( )	{ : 填充物>长度}

```python
string1 = '我喜欢吃{:*>11}你喜欢么'
result = string1.format('小龙虾')
print(result)

我喜欢吃*******小龙虾你喜欢么
```



##### format( ) 实现进制转换

1. 二进制 {:b}

```python
num = '{}转换成二进制为:{:b}'
result = num.format(10,10)
print(result)
```



2. 八进制 {:o}

```python
num = '{}转换成八进制为:{:o}'
result = num.format(10,10)
print(result)
```



3. 十进制: {:d}

```python
num = '{}转换成十进制为:{:d}'
result = num.format(10,10)
print(result)
```



4. 十六进制: {:x}

```python
num = '{}转换成十六进制为"{:x}'
result = num.format(10,10)
print(result)
```



## 8. 内建函数

### 8.1 类型转换相关

int( ):		

​	将其他类型转换成整型

float( ):		

​	将其他类型转换成浮点型

bool( ):		

​	将其他类型转换成布尔值

complex( ):	

​	将其他类型转换成复数

str( ):		

​	将其他类型转换成字符串

list( ):		

​	将其他类型转换成列表

tuple( ):		

​	将其他类型转换成元组

set( ):		

​	将其他类型转换成集合

dict( ): 		

​	将其他类型转换成字典



### 8.2 变量相关

type( ):		

​	查看变量的类型

id( ):			

​	查看变量的内存id

print( ):		

​	打印

locals( ):		

​	查看当前环境中的所有变量



### 8.3 数学相关

* abs( )		

  获取一个数值的绝对值

```python
num = -99
result = abs(num)
print(result)
```



* max( )		

  获取序列或者多个参数的最大值

```python
list1 = [1,2,3,4,5,6,7,8,9]
result = max(list1)
print(result)

result = max(1,2,3,4,5,6,7,88,0)
print(result)
```



* min( )		

  获取序列或者多个参数的最小值

```python
list1 = [1,2,5,6,4,1,345,68,2]
result = min(list1)
print(result)

result = min(1,214,5,6,7235,67)
print(result)
```



* round( )		

  四舍五入,可以加参数来指定 *保留几位小数* 

```python
num = 3.1415
result = round(num,3)  #3用来指定小数位数
print(num)
```



* pow( )

  计算指定数字的n次方

```python
result = pow(2,3)   # 2 ** 3
print(result)
```



* bin( )

  将数字转换成二进制

```python
result = bin(10)
print(result)
```

* oct( )

  将数字转换成八进制

```python
result = oct(10)
print(result)
```



* hex( )

  将数字转换成十六进制

```python
result = hex(10)
print(result)
```



### 8.4 Ascii码相关

* chr( )

  将指定的Ascii码转换成对应字符

```python
result = chr(97)
print(result)
>>>a
```

* ord( )

  将指定的字符转换成ascii码

```python
result = ord('a')
print(result)
>>>97
```

* eval( )

  将字符串转换成代码

```python
string1 = 'num + 1'
num = 1
num = eval(string1)
print(num)
>>>2
```



## 9. 数学模块

在使用数学模块之前需要先导入模块

import math



* ceil( )

  向上取整

```python
num = 0.1
result = math.ceil(num)
print(result)
```



* floor( )

  向下取整

```python
num = 1.9
result = math.floor(num)
print(result)
```



* pow( )	

  和内置函数功能一样,计算指定值的n次方,返回值是 *浮点数*

```python
result = math.pow(2,3)
print(result)
```



* sqrt( )

  开平方根

```python
result = math.sqrt(4)
print(result)
```



* fabs( )

  功能和内建函数abs( )功能一样,取绝对值,返回值是 *浮点数*

```python
num = -9
result = math.fabs(num)
print(result)
>>>9.0
```



* modf( )

  将指定数字拆分成两部分,一部分为小数部分,一部分为整数部分,返回值是 *浮点数*

```python
num = 12.55
result = math.modf(num)
print(result)
>>>(0.5500000000000007, 12.0)
```



* copysign( )

  让 前面数字 的符号和 后面数字 的*符号*始终保持一致,返回值是 *浮点数*

```python
result = math.copysign(9,-2)
print(result)
>>>-9.0
```



* fsum( )

  功能和sum( )一样,计算序列的和. 返回值是 *浮点数* 

```python
list1 = [1,2,3,4,5,6]
result = math.fabs(list1)
print(result)
```



* Pi 和 e

```python
result = math.pi
print(result)

result = math.e
print(result)
```



## 10. 随机数模块

使用随机数模块前需要先载入该模块

import random



* random( )

  随机获取 0-1 不包含1的随机浮点数

```python
num = random.random()
print(num)
```



* shuffle( )

  将给定的一个序列 随机打乱,直接改变原序列的顺序

```python
list1 = [1,2,4,5,6,7,8,9]
random.shuffle(list1)
print(list1)
```



* choice( )

  随机从一个序列中 *取出一个* 元素

```python
list1 = [1,2,4,5,7,8,5,3]
result = random.choice(list1)
print(result)
```



* uniform( )

  随机获取指定范围内的一个浮点数

```python
result = random.uniform(1,100)
print(result)
```



* randrange( ) & randint( )

  随机获得指定范围内的整数

```python
result = random.randrange(1,100)
print(result)

num = random.randint(1,100)
print(num)
```



## 11. 列表

### 11.1 列表基本操作

#### 11.1.1 创建列表

##### 11.1.1.1 创建空列表

```python
list1 = list()

list1 = []
```

##### 11.1.1.2 创建有数据的列表

```python
list1 = [1,2，3,4,5]
list2 = [1]
```

#### 11.1.2 访问列表中的值

列表名[索引值]

```python
list1 = ['徐凤年','姜泥','裴南苇','青鸟']
result = list1[1]
print(result)
```



#### 11.1.3 修改列表中的值

列表名[索引值] = 新的值

```python
list1[1] = '白狐'
print(list1[1])
```



#### 11.1.4 删除列表中的值

del 列表名[索引值]

```python
del list1[1]
pirnt(list1)
```



del 可以删除任何变量

```python
del list1
```



### 11.2 列表的序列操作

#### 11.2.1 序列相加 +

```python
list1 = [1,2,3]
list2 = [4,5,6]
list3 = list1 + list2
print(list3)

>>>[1, 2, 3, 4, 5, 6]
```



#### 11.2.2 序列相乘 *

```python
list1 = ['嘿嘿嘿']
list2 = list1 * 3
print(list2)

>>>['嘿嘿嘿', '嘿嘿嘿', '嘿嘿嘿']
```



#### 11.2.3 分片 [ : : ]

[起始:终止:间隔]  都不包含终止位置(左闭右开)

```python
list1 = [1,2,3,4,5,6,8,9]
result = list1[1:2]
print(result)
>>>[2]

result = list1[:4]
print(result)
>>>[1, 2, 3, 4]

result = list1[::2]
print(result)
>>>[1, 3, 5, 8]
```



#### 11.2.4 成员检测

in & not in 
返回值：True or False

```python
list1 = ['徐凤年','姜泥','王初东','裴南苇']
result = '徐凤年' in list1
print(result)
>>>True

result = '白狐脸' not in list1
print(result)
>>>False
```



#### 11.2.5 len( ) & max( )	& min( )

```python
list1 = [1,2,3,4,5,6,7,8]
result = len(list1)
print(result)

result = max(list1)
print(result)

result = min(list1)
print(result)
```



### 11.3 遍历列表

#### 11.3.1遍历一级列表

```python
list1 = ['徐凤年','姜泥','白狐脸','裴南苇','鱼幼薇','青鸟']
for each in list1
	print(each)
	

num = 0
while num < len(list1):
	print(list1[num])
```



#### 11.3.2遍历等长二级(二维)列表

```python
list1 = [
    [1,2,3],
    [4,5,6],
    [7,8,9],
]
# 方法一：
for x,y,z in list1:
    print(x,y,z)
# 方法二：
for i in list1:
    for list12 in i:
        print(list12)
```



####  11.3.3遍历不等长的二级列表

```python
list1 = [
    [1,2,3],
    [4,5,6,10,45],
    [7,8,9],
]

for i in list1:
    for j in i:
        print(j)
```



### 11.4 列表推导式

#### 11.4.1 普通格式

```python
list1 = [1,2,3,4,5,6,7,8,9]
list2 = [i * 2 for i in list1]
print(list2)
```



####  11.4.2 带有条件的列表推导式

```python
list1 = [1,2,3,4,5,6,7,8]
list2 = [i for i in list1 if i % 2 == 0]
print(list2)
```



#### 11.4.3 多循环列表推导式

```python
# 推导式表示法：
list1 = [1,2,3,4,5,6,7,8]
list2 = [9,10,11,12,13,14]
list3 = [i + j for i in list1 for j in list2]
print(list3)

# 常规方法：
list3=[]
for i in list1:
    for j in list2:
        list3.append(i+j)
print(list3)
```



#### 11.4.4 带条件的多循环列表推导式

```python
list1 = [1,2,3,4,5,6,7,8]
list2 = [9,10,11,12,13,14]
list3 = [i + j for i in list1 for j in list2 if list1.index(i) == list2.index(j)]
print(list3)
```



### 11.5 列表函数

* append( )

  向列表的末尾添加元素

  ```python
  list1 = [1,2,3,4]
  list1.append(5)
  print(list1)
  
  >>>[1,2,3,4,5]
  ```

* insert( )

  向列表指定索引位置前添加指定元素

  insert(索引,值)

  ```python
  list1 = [1,2,3,4]
  list1.insert(1,'人')
  print(list1)
  
  >>>[1,'人',2,3,4]
  ```

* extend( )

  使用一个列表去扩充另一个列表

  ```python
  list1 = [1,2,3,4,5,6]
  list2 = [7,8,9,10,11]
  list1.extend(list2)
  print(list1)

  >>>[1,2,3,4,5,6,7,8,9,10,11]
  ```

* pop( )

  将列表 *指定位置* 的值取出来.用pop删除的数据可以存储继续使用以及后续的操作，默认取出最后一位。

  ```python
  list1 = [1,2,3]
  result = list1.pop(0)
  print(result)
  print(list1)

  result = list1.pop()
  print(result)
  print(list1)
  ```

* remove( )

  将列表中的指定元素删除

  remove(值)

  ```python
  list1 = ['人猫','徐凤年','姜泥']
  list1.remove('人猫')
  print(list1)
  ```

* clear( )

  将列表清空

  ```python
  list1 = [1,2,3]
  list1.clear()
  print(list1)
  ```

* copy( )

  复制列表,复制得到的列表和原列表的内存id不同

  ```python
  list1 = [1,2,3,4]
  list2 = list1.copy()
  print(list2)
  print(id(list2))
  ```

* count( )

  计算字符串中 *指定字符* 出现的次数    不同于字符串的函数count(指定字符,起始,终止)  

  ```python
  list1 = [1,1,1,23,44,24,15,66,3]
  result = list1.count(1)
  print(result)
  ```

* index( )

  获取列表中指定元素出现的 *索引值*

  ```python
  list1 = ['徐骁','徐凤年','姜泥','裴南苇']
  result = list1.index('徐凤年')
  print(result)
  ```

* reverse( )

  将列表排列顺序颠倒,直接改变原列表

  ```python
  list1 = [1,2,3,4]
  list1.reverse()
  print(list1)
  ```

* sort( )

  将列表按从小到大的顺序排列. 可用参数key  & reverse 

  ```python
  list1 = [1,2,3,4,5]
  list1.sort()
  print(list1)
  ```

  将列表按从大到小的顺序排列

  ```python
  list1.sort(reverse=True)
  print(list1)
  ```

  将列表按自定义的规则排列

  ```python
  def func(num):	#一定要有形参
  	return num // 10		# 一定要有return

  list1.sort(key=func,reverse=True)
  print(list1)
  ```

  ​

## 12.元组

### 12.1 创建元组

#### 12.1.1 创建空元组

方法一: 使用tuple( )

```python
tuple1 = tuple()
print(tuple1,type(tuple1))
```

方法二:使用( )

```python
tuple1 = ()
print(tuple1,type(tuple1))
```

#### 12.1.2 创建一个元素的元组

```python
tuple1 = (1,)
print(tuple1,type(tuple1))

tuple1 = 1,
print(tuple1,type(tuple1))
```

#### 12.1.3 创建多个元素的元组

```python
tuple1 = (1,23,2,4,5)
print(tuple1,type(tuple1))
```



### 12.2 元组的基本操作(增删改查)

元组不能直接增加,删除,修改元素,

元组基本操作只支持查看元组内的元素: 元组名[索引]

```python
tuple1 = (1,23,4,5,5,67)
print(tuple1[1])
```



### 12.3 元组的序列操作

#### 12.3.1 序列相加

```python
tuple1 = (1,2,3,4)
tuple2 = (5,6,7,8)
result = tuple1 + tuple2
print(result)
```



#### 12.3.2 序列相乘

```python
tuple1 = (1,2,3)
result = tuple1 * 2
print(result)
```



#### 12.3.3 分片 [ : : ]

```python
tuple1 = ('徐凤年','徐骁','姜泥','青鸟','王仙之','曹长青','白狐脸儿')
print(tuple1[:2])	
print(tuple1[3:])	
print(tuple1[1:4])
print(tuple1[::2])	# [起始:终止(不包含):间隔]
```



#### 12.3.4 成员检测

```python
tuple1 = ('徐凤年','徐骁','姜泥','青鸟','王仙之','曹长青','白狐脸儿')
result = '徐凤年'in tuple1
print(result)

result = '啦啦啦' not in tuple1
print(result)
```



### 12.4 元组的序列函数

#### 12.4.1 len() , max(), min(), tuple()

```python
tuple1 = ('徐凤年','徐骁','姜泥','青鸟','王仙之','曹长青','白狐脸儿')

length = len(tuple1)
print(length)

tuple2 = (1,23,22,4,5,53,6)
print(max(tuple2))
print(min(tuple2))

list1 = [1,2,3]
tuple3 = tuple(list1)
print(tuple3)
```



### 12.5 元组的遍历

#### 12.5.1 遍历普通元组

```python
tuple1 = ('徐凤年','徐骁','姜泥','青鸟','王仙之','曹长青','白狐脸儿')
for i in tuple1:
	print(i)
```



#### 12.5.2 遍历等长的二级元组

```
tuple1 = ((1,2),(3,4),(5,6))
for x,y in tuple1:
	print(x,y)
```



#### 12.5.3 遍历不等长的二级元组

```
tuple1 = ((1,2),(3,4,5),(6,7,8,9))
for i in tuple1:
	for j in i:
		print(j)
```



#### 12.5.4 访问多级元组中的值

```
tuple1 = ((1,2),(3,4,5),(6,7,8,9))
print(tuple1[0][1])
```



### 12.6 元组推导式

元组推导式的结果是一个生成器,生成器如果不遍历一遍的话,是不会使用的.

#### 12.6.1 普通元组推导式

```
tuple1 = (1,2,3,4,5,6)

tuple2 = (i * 10 for i in tuple1)

for each in tuple2:  # 如果不遍历的话,tuple2这个生成器将一直存在但是不做任何操作
	print(each)
```



#### 12.6.2 带有条件的元组推导式

```
tuple1 = (1,2,3,4,5,6)

tuple2 = (i * 10 for i in tuple1 if i % 2 == 0)

for each in tuple2:
	print(each)
```



#### 12.6.3 多循环元组推导式

```
tuple1 = (1,2,3,4,5)
tuple2 = (10,20,30,40)

tuple3 = (i + j for i in tuple1 for j in tuple2)

for each in tuple3:
	print(each)
```



#### 12.6.4 带有条件判断的多循环元组推导式

```
tuple1 = (1,2,3,4)
tuple2 = (5,6,7,8)

tuple3 = (i * j for i in tuple1 for j in tuple2 if tuple1.index(i) == tuple2.index(j))

for each in tuple3:
	print(each)
```



### 12.7 元组专用函数

1. index( ) 查看指定元素在元组中的索引值

   ```
   tuple1 = ('华为','小米','大米','三星','iphone')

   print(tuple1.index('华为'))

   print(tuple1.index('三星'))
   ```


2. count( ) 计算指定元素在元组中出现的次数

   ```
   tuple1 = ('华为','华为','三星','三星','iphone')

   print(tuple1.count('华为'))

   print(tuple1.count('三星'))
   ```

   ​

## 13. 字典

### 13.1 创建字典

#### 13.1.1 创建空字典

方法一: 使用{ }来创建空字典

```
dict1 = {}
print(dict1,type(dict1))
```

方法二: 使用 dict( ) 来创建空字典

```
dict1 = dict()
print(dict1,type(ditc1))
```



#### 13.1.2 创建多个元素的字典

方法一: 使用 { } 来创建多个元素的字典

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
print(dict1,type(ditc1))
```



方法二: 使用dict( ) 来创建多个元素的字典

```
#1.dict(字典)
dict1 = {{'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}}
print(dict1,type(dict1))

#2.dict(等长二级容器)
tuple1 = (('小丽','马丽丽'),('静静','刘文静'),('瑶瑶','王瑶'),('紫薇','孙紫薇'))
dict1 = dict(tuple1)
print(ditc1,type(dict1))

#3.dict(关键字传参)
dict1 = dict(小丽='马丽丽',静静='刘文静',瑶瑶='王瑶',紫薇='孙紫薇')
print(dict1,type(dict1))

#4.dict(zip(键的容器,值的容器))
keys = ('小丽','静静','瑶瑶','紫薇')
values = ('马丽丽','刘文静','王瑶','孙紫薇')
dict1 = dict(zip(keys,values))
```



### 13.2 字典的基本操作(增删改查)

#### 13.2.1 字典中直接增加新元素

字典[键] = 值

如果键不存在在字典中,则直接将这个键值对添加到字典中作为新元素

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}

dict1['班长'] = '戴帅林'

print(dict1)
```



#### 13.2.2 字典中直接删除元素

del 字典[键] 

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
del dict1['小丽']
print(dict1)
```



#### 13.2.3 字典中直接修改元素

```
dict1 =  {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
dict1['小丽'] = '马冬梅'

print(dict1)
```



#### 13.2.4 字典中查看元素的值

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}

print(dict1['小丽'])
```



### 13.3 字典的序列操作

序列相加,序列相乘,分片这些序列操作字典都不支持

字典只能进行成员检测(只检测字典中的键)

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
result = '小丽' in dict1
print(result)

reslut = '王贷' not in dict1
print(result)
```



### 13.4 字典的序列函数

#### len( ) , max( ) , min( ), dict( ) 

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}

length = len(dict1)
print(length)

dict2 = {1:'数字',2:'数字',3:'数字',4:'数字',5:'数字',6:'数字',}
maxnum = max(dict2)
print(maxnum)

minnum = min(dict2)
print(minnum)
```



### 13.5 遍历字典

#### 13.5.1 遍历一级字典

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}

#方法一:
for i in dict1:
	print(i , dict1[i])

#方法二:
for i,j in dict1.items():
	print(i,j)
```



### 13.6 字典推导式

#### 13.6.1 基本字典推导式

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}

dict2 = {key:'@'+value for key,value in dict1.items()}

print(dict2)
```

#### 13.6.2 带有条件的字典推导式

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}

dict2 = {key:value for key,value in dict1.items() if len(key) == len(value)}

print(dict2)
```

####  13.6.3 带有循环的字典推导式

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
dict2 = {'班长':'戴帅林'}

dict3 = {key+i : value+j for key,value in dict1.items() for i,j in dict2.items()}

print(dict3)
```

#### 13.6.4 带有判断的多循环字典推导式

```
dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
dict2 = {'班长':'戴帅林'}

dict3 = {key+i : value+j for key,value in dict1.items() for i,j in dict2.items() if len(value) == len(j)}

print(dict3)

```



### 13.7 字典的专用函数

1. ### clear( )	清空字典

   ```
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   dict1.clear()
   print(dict1)
   ```

2. ### copy( )     复制字典

   ```
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   dict2 = dict1.copy()
   print(dict2)
   ```

3. ### fromkeys( ) 将容器中的值作为键,设定的第二个参数作为所有键的值,创建字典

   ```
   list1 = [1,2,3,4,5]
   dict1 = {}.fromkeys(list1,'数字')
   print(dict1)

   {1:'数字',2:'数字',3:'数字',4:'数字'}
   ```

4. ### get( ) 通过键获取字典中的值

   ```
   # 若键存在,则返回值
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   result = dict1.get('小丽')
   print(result)

   # 若键不存在,则返回None.
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   result = dict1.get('班长')
   print(result)

   # 若键不存在,但是设定了返回值.则返回返回值
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   result = dict1.get('班长','不在')
   print(result)
   ```

   ​

5. ### items( ) 将字典转换成等长的二级元组

   ```
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   result = dict1.items()
   print(result)
   ```

6. ### keys( ) 将字典中的键取出来,放进容器中 

   ```
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   list1 = dict1.keys()
   print(list1)
   ```

7. ### values( ) 将字典中的值取出来,放进容器中

   ```
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   list1 = dict1.values()
   print(list2)
   ```



8. ### pop( ) 删除字典中指定键值对  pop(指定的键,默认值)

   ```
   # 移除存在的键和值
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   result = dict1.pop('小丽')
   print(dict1,result)

   # 移除不存在的键,未设置默认值,则报错!!! pop(不存在的键,还tm没设置默认值) 等着报错吧!!!
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   result = dict1.pop('班长')
   print(dict1,result)

   # 移除不存在的键,设置了默认值 pop(不存在的键,设置了默认值),则返回默认值
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   result = dict1.pop('班长','不在')
   print(dict1,result)
   ```



9. ### popitem( ) 随机移除出字典中的一个键值对

   ```
   dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
   result = dict1.popitem()
   print(result)
   ```



10. ### setdefault( ) 向字典中添加元素

  ```
  # 若要添加的键不存在,则新增进字典中
  dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
  dict1.setdefault('班长','戴帅林')
  print(dict1)

  # 若要添加的键已经在字典中,则不做任何操作
  dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
  dict1.setdefault('小丽','马丽丽')
  print(dict1)
  ```



11. ### update( ) 更新字典,直接改变原字典

    ```
    # update(关键字传参)
    dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
    dict1.update(小丽='马丽丽',静静='刘文静',瑶瑶='大熊太美',紫薇='戏精')
    print(dict1)

    # update(新的字典)
    dict1 = {'小丽':'马丽丽','静静':'刘文静','瑶瑶':'王瑶','紫薇':'孙紫薇'}
    dict1.update({'小丽':'马里奥','静静':'静毛线','瑶瑶':'大熊太美','紫薇':'戏精'})
    print(dict1)
    ```

    # 14.集合

    集合的特征:

    * 集合是无序数据
    * 集合中所有元素都是唯一的,集合自带去重功能
    * 集合中可以包含Number(int,float,bool,complex) , string  , tuple 和 冰冻集合 

### 14.1 创建集合

#### 14.1.1 创建空集合

```
使用set() 来创建空集合

set1 = set() 
print(set1,type(set1))
```



#### 14.1.2 创建具有多个元素的集合

```
set1 = {1,2,3,4,5,6}
print(set1,type(set1))
```



### 14.2 集合的基本操作(增删改查都不行)



### 14.3 集合的序列操作

集合只支持成员检测这一个序列操作

#### 14.2.1 成员检测 in     not in

```
set1 = {1,2,3,44,51,6}
result = 1 in set1
print(result)

result = 222 not in set1
print(result)
```



### 14.5 集合的序列函数

#### len() , max() , min() , set() 

```
set1 = {1,2,3,4,5,6}

length = len(set1)
print(length)

maxnum = max(set1)
print(maxnum)

minnum = min(set1)
print(minnum)

list1 = [1,2,3,4,5,6,7]
set1 = set(list1)
print(set1,type(set1))
```



### 14.6 遍历集合

#### 14.6.1 遍历一级集合

```
set1 = {1,23,45,3,7,54}
for each in set1:
	print(each)
```



#### 14.6.2 遍历二级集合(等长)

```
set1 = {('徐骁','徐凤年'),('西楚姜皇帝','姜泥'),('谢灵云','白狐脸'),('无名氏','呵呵')}
for x,y in set1:
	print(x,y)
```



#### 14.6.3 遍历二级集合(不等长)

```
set1 = {('不才','任然'),('张楚','窦唯','何勇'),('陈粒')}

for i in set1:
	for j in i:
		print(j)
```



### 14.7 集合推导式

#### 14.7.1 基本集合推导式

```
set1 = {1,2,3,4,5,6,7,8}
result = {i*2 for i in set1}
print(result)
```



#### 14.7.2 带条件判断的集合推导式

```
set1 = {1,2,3,4,5,6,7,8}
result = {i * 10 for i in set1 if i % 2 == 0}
print(result)
```



#### 14.7.3 多循环集合推导式

```
set1 = {'窦唯','Gai','万晓利'}
set2 = {'女儿情','天干物燥','噢,乖'}

result = {i + j for i in set1 for j in set2}
print(result)
```



#### 14.7.4 带条件判断的多循环集合推导式

```
set1 = {'窦唯','Gai','万晓利'}
set2 = {'女儿情','天干物燥','噢,乖'}

result = {i + j for i in set1 for j in set2 if len(i) == len(j)}
```



### 14.7 集合的函数操作

#### add( ) 向集合中添加元素

```
set1 = {'窦唯','Gai','万晓利'}

set1.add('朴树')
print(set1)
```



#### pop( ) 从集合中随机取出一个元素

```
set1 = {'窦唯','Gai','万晓利'}
result = set1.pop()
print(result)
```



#### remove( ) 从集合中删除指定元素

```
set1 = {'窦唯','Gai','万晓利'}

# remove(不存在的元素)   ---  报错
set1.remove('窦唯老婆')

# remove(存在的元素)     --- 正常删除
set1.remove('窦唯')

```



#### discard( ) 从集合中删除指定元素

```
set1 = {'窦唯','Gai','万晓利'}

# discard(不存在的元素)  ---  不做任何操作
set1.discard('窦唯老婆')

# discard(存在的元素)    ---  正常删除
set1.discard('窦唯')
```



#### clear( ) 清空集合

```
set1 = {'窦唯','Gai','万晓利'}

set1.clear() 

print(set1)
```



#### copy( ) 复制集合

```
set1 = {'窦唯','Gai','万晓利'}
set2 = set1.copy()
print(set2,type(set2))
```



### 14.8 集合之间运算函数

#### difference( ) 计算一个集合相对另一个集合的差集

```
set1 = {'徐凤年','徐骁','李义山'}
set2 = {'徐凤年','姜泥','青鸟'}

result = set1.difference(set2)
print(result)
```



#### difference_update( ) 计算一个集合相对另一个集合的差集,并直接改变原集合

```
set1 = {'徐凤年','徐骁','李义山'}
set2 = {'徐凤年','姜泥','青鸟'}

set1.difference_update(set2)
print(set1)
```



#### intersection( ) 计算一个集合和另一个集合的差集

```
set1 = {'徐凤年','徐骁','李义山'}
set2 = {'徐凤年','姜泥','青鸟'}

result = set1.intersection(set2)
print(result)
```



#### intersection_update( ) 计算一个集合和另一个集合的交集,并直接改变原集合

```
set1 = {'徐凤年','徐骁','李义山'}
set2 = {'徐凤年','姜泥','青鸟'}

set1.intersection_update(set2)
print(set1)
```



#### union( ) 计算两个集合的并集

```
set1 = {'徐凤年','徐骁','李义山'}
set2 = {'徐凤年','姜泥','青鸟'}

result = set1.union(set2)
print(result)
```



#### update( ) 计算两个集合的并集,并更新原集合

```
set1 = {'徐凤年','徐骁','李义山'}
set2 = {'徐凤年','姜泥','青鸟'}

set1.update(set2)
print(set1)
```



#### symmetric_difference( ) 计算两个集合的对称差集

```
set1 = {'徐凤年','徐骁','李义山'}
set2 = {'徐凤年','姜泥','青鸟'}

result = set1.symmetric_difference(set2)
print(result)
```



#### symmetric_difference_update( ) 计算两个集合的对称差集并更新原集合

```
set1 = {'徐凤年','徐骁','李义山'}
set2 = {'徐凤年','姜泥','青鸟'}

set1.symmetric_difference_update(set2)
print(set1)
```



### 14.9 集合检测类函数

#### issuperset( ) 检测一个集合是否是另一个集合的超集

```
set1 = {'徐凤年','徐骁','李义山','姜泥','青鸟'}
set2 = {'徐凤年','姜泥','青鸟'}

result = set1.issuperset(set2)
print(result)
```



#### issubset( ) 检测一个集合是否是另一个集合的子集

```
set1 = {'徐凤年','徐骁','李义山','姜泥','青鸟'}
set2 = {'徐凤年','姜泥','青鸟'}

result = set2.issubset(set1)
print(result)
```



#### isdisjiont( ) 检测两个集合是否没有交集

```
set1 = {'徐凤年','徐骁','李义山','姜泥','青鸟'}
set2 = {'徐凤年','姜泥','青鸟'}

result = set1.isdisjoint(set2)
print(result)
```



### 14.10 冰冻集合

1. 创建空冰冻集合

```
set1 = frozenset()
print(set1,type(set1))
```



2. 创建多个元素的冰冻集合

```
set1 = frozenset({1,2,3,4,5,6,8,7,9})
print(set1,type(set1))
```



3. 遍历冰冻集合

```
set1 = frozenset({1,2,3,4,5,6,8,7,9})
for i in set1:
	print(i)
```



4. 冰冻集合推导式

```
result = {i+2 for i in set1}
print(result)
```



5. 冰冻集合函数

```
冰冻集合没有专用的函数
但是
冰冻集合可以使用所有不改变原集合的集合函数
```



## 15. 文件操作

### 15.1 文件操作的步骤

1. 打开文件
2. 对文件进行操作
3. 关闭文件

#### 15.1.1 文件写入操作

```
# 1. 使用open()打开指定文件
fp = open('/Users/apple/desktop/01.txt','w')

# 2. 对文件进行写入操作
fp.write('写入操作,输入........')

# 3. 关闭文件
fp.close()
```

#### 15.1.2 文件读取操作

```
# 1. 使用open()打开指定文件
fp = open('/Users/apple/desktop/01.txt','r')

# 2. 对文件进行读取操作
result = fp.read()
print(result)

# 3. 关闭文件
fp.close()
```



### 15.2 文件操作函数

#### 1. open() 打开或新建文件

```
变量 = open('文件绝对路径','打开模式')

打开模式:

基础模式:( w,a,x,r )
w:	write 	写入模式	若文件不存在,则新建. 若已经存在,打开文件并清空原有内容
a:  append 	追加模式	若文件不存在,则新建. 若已经存在,则打开文件,则原有内容基础上添加
x:	xor		异或模式	若文件不存在,则新建. 若已经存在,则报错
r:	read	读取模式	可执行读取文件的相关操作

增强模式( +,b ) 只能和基础模式配合使用 
+:	plus	读写模式	在w,a,x 或者 r 的基础上加+,则实现读写都可的功能
b:	byte	位模式		 在位模式下进行读或者写或者读写的操作

组合方式:
w:		若文件不存在,则新建文件等待写入操作. 若文件已存在,则打开文件并清空原内容,之后可以进行写入操作. 
a:  	若文件不存在,则新建文件等待写入操作. 若文件已存在,则打开文件并清空原内容,之后可以进行写入操作.
x: 		若文件不存在,则新建文件等待写入操作. 若文件已存在,则直接报错!
r: 		若文件不存在,则报错! 若文件已存在,则打开文件,并可进行读取相关的操作

w+:		若文件不存在,则新建文件等待写入操作. 若文件已经存在,则打开文件并清空内容,之后可执行写入或读取
r+:		若文件不存在,则报错! 若文件已经存在,则打开文件,之后可执行写入操作和读取操作
x+:		若文件不存在,则新建文件等待写入操作, 若文件已经存在,则报错!
a+:		若文件不存在,则新建文件等待写入操作, 若文件已经存在,则打开原文件,在原文件的基础上可追加或读取

wb:		若文件不存在,则新建文件等待写入操作.若文件已经存在,则打开文件并清空内容.所有写入需要用encode()编码
rb:		若文件不存在,则报错! 若文件已经存在,则打开文件可进行读取操作.所有读取内容要用decode()解码
ab:		若文件不存在,则新建文件等待写入操作,若文件已经存在,则打开文件并追加内容.所有写入需要用encode()编码
xb:		若文件不存在,则新建文件等待写入操作,若文件已经存在,则报错!

wb+:	若文件不存在,则新建文件且可读可写.若文件已存在,清空内容,可读可写.读要用decode()解码.写要用			encode()编码
rb+:	若文件不存在,则报错! 若文件已存在,则打开文件,可读可写.读要用decode()解码.写要用encode()编码
ab+:	若文件不存在,则新建文件且可读可写.若文件已存在,打开原内容,追加内容.读要用decode()解码.写要用			encode()编码
xb+:	若文件不存在,则新建文件且可读可写,若文件已存在,直接报错! 读要用decode()解码.写要用encode()编码
```



如: 	 使用r+模式打开文件

```
# 打开文件
fp = open('/Users/apple/desktop/01.txt','r+')   # 若此时01.txt不存在,则直接报错

# 先读取原有内容
content = fp.read()
print(content)

# 写入新内容
fp.write('写入内容')

# 移动指针
fp.seek(0) #单位是字节 0表示移动到开头位置

# 再读取现在的内容
content = fp.read()
print(content)

# 关闭文件
fp.close()
```



如: a+b模式打开或新建文件

```
# 打开文件
fp = open('/Users/apple/desktop/01.txt','a+b')

# 追加内容
fp.write('在原有基础上追加内容'.encode())

# 移动指针到开头
fp.seek(0)

# 读取全部内容
content = fp.read().decode()
print(content)

# 关闭文件
fp.close()
```



#### 2. read() 读取文件内容

1. 文件.read( ) 默认读取全部文件内容

```
fp = open('/Users/apple/desktop/01.xtx' ,'r')

content = fp.read()
print(content)

fp.close()
```



2. 文件.read(指定字符个数) 读取指定的字符个数

```
fp = open('/Users/apple/desktop/01.txt','r')

content = fp.read(20)
print(content)

fp.close()
```



#### 3. readline() 读取一行文件内容

文件.readline( ) 默认读取一行内容

文件.readline(指定字符个数) 默认读取指定字符长度内容,超过一行按一行算,不够一行就不够呗 

```
fp = open('/Users/apple/desktop/01.txt','r')

# 读取一行文件的内容
content = fp.readline()  
print(content)

# 移动指针
fp.seek(0)

# 读取指定字符长度,若不满足一行则只读5个字符,若超过一行,则只读一行字符
content = fp.readline(5) 
print(content)

# 关闭文件
fp.close()
```



#### 4. readlines() 一次读取多行内容

```
# 打开文件
fp = open.(''/Users/apple/desktop/01.txt','r')

# 默认读取全部行
content = fp.readlines()
print(content)

# 移动指针
fp.seek(0)

# 读取指定字符长度的行数
content = fp.readlines(20)  # 字符长度若不足一行,则按一行算,若超过一行,则显示下一整行
print(content)

# 关闭文件
fp.close()
```



#### 5. truncate() 文件截取

保留指定的字节长度,其他都删除   单位:字节!!!!

```
fp = open('/Users/apple/desktop/01.txt'.'r+')

fp.truncate(12)  # 保留指定的字节长度,其他都删除

fp.close()
```



#### 6. tell() 获取当前打开的文件的指针位置

```
fp = open('/Users/apple/desktop/01.txt','r')

num = fp.tell()
print(num)

fp.close()
```



#### 7. seek() 将指针移动指定的字节长度

```
fp = open('/Users/apple/desktop/01.txt','r')

fp.seek(21)

content = fp.read()   # read() 的内容是在指针之后的内容才能读取
print(content)   

fp.close()
```



#### 8. 自定义函数获取指定行数

```
# 自定义函数实现读取文件中的指定行数

def myReadLines(path,hang=-1,sep='\n'):  
# path:要打开的文件路径  hang:显示文件内容的行数  sep:当前操作系统中默认的换行符号

    # 打开指定文件
    fp = open(path,'r')

    # 获取文件内所有内容
    content = fp.read()

    # 使用换行符号切割字符串,放入列表lists中
    #若最后一行切完是一个空字符串,则需要分片去掉最后一个 lists = content.split(sep)[0:-1]
    lists = content.split(sep) 

    # 判断用户输入的行数,并确认最终输出的总行数
    maxhang = len(lists)

    if hang < 0 or hang >= maxhang:
        hang = maxhang
    else:
        hang = int(hang)

    result = [i + sep for i in lists[:hang]]  # 用分片来控制最终的列表的长度

    # 如果要用列表的形式直接呈现,直接输入result就可以了
    #print(result)

    # 遍历最终的列表result 输出内容
    for i in result:
        print(i,end='')

myReadLines('/Users/apple/desktop/01.txt',5)
```



## 16. os (操作系统)模块

使用os模块之前要先导入

import os

### 16.1 os模块函数



#### 16.1.1 文件夹类os操作

##### 1. os.listdir() 

功能: 获取指定路径文件夹下所有的文件及文件夹的列表

格式: os.listdir(目标文件夹路径)

返回值: 所有文件及文件夹的列表

```
lists = os.listdir(/Users/apple/desktop)
print(lsits)
```



##### 2. os.mkdir() 

功能: 在指定路径创建空文件夹

格式:os.mkdir(目录路径,0o权限数组) 未设定则按默认权限创建

返回值:创建的文件夹绝对路径

```
os.mkdir('/Users/apple/dekstop/a',0o755)

os.mkdir('/Users/apple/desktop/b)
```



##### 3. os.rmdir() 

功能: 删除指定路径的空文件夹

格式: os.rmdir(目录路径)

返回值:None

```
os.rmdir('/Users/apple/desktop/a')
```



##### 4. os.makedirs()

功能: 递归创建空文件夹

格式: os.makedirs(目录路径)

返回值: 创建的目录的字符串路径

```
os.makedirs('/Users/apple/desktop/aaa/bb/c')
```



##### 5. os.removedirs()

功能: 递归删除空文件夹

格式: os.removedirs(目录路径)

返回值: None

```
os.removedirs('/Users/apple/desktop/aaa/bb/c')
```



##### 6. os.getcwd() 

功能: 获取当前默认工作的文件夹路径

格式: os.getcwd() 

返回值:当前工作的目录路径字符串

```
pathnow = os.getcwd()
print(pathnow)
```



##### 7.os.chdir()

功能: 改变当前工作的文件夹路径

格式: os.chdir(目的地路径)

返回值:None

```
# 改变文件夹,在桌面创建新文件

os.chdir('/Users/apple/desktop')
fp = open('01.txt','w')
print(os.getcwd())
fp.close
```



#### 16.1.2 通用os操作

##### 1. os.rename( ) 

功能: 重命名文件夹

格式: os.rename(原文件夹或文件路径,新名文件夹或文件路径)

返回值: None

```
os.rename('/Users/apple/desktop/01.txt','/Users/apple/desktop/02.txt')
```



##### 2. os.stat( )

功能: 获取指定文件夹或文件的相关信息(属性)

格式: os.stat(指定文件夹或文件的目录)

返回值: 包含属性信息的元组

```
result = os.stat('/Users/apple/desktop/01.txt)
print(result)
```



##### 3. os.getenv()

功能: 获取当前系统的环境变量信息

格式: os.getenv(获取的环境变量名称) 'PATH' 要大写

返回值: 字符串

```
result = os.getenv('PATH')
print(result.split(':'))
```



##### 4. os.putenv()

功能: 设置环境变量信息

格式: os.putenv(环境变量参数,新增值)

返回值: None

```
os.putenv('PATH','/')
os.system('mydir')
```



##### 5. os.system()

功能: 在python中使用系统命令

格式: os.system(系统命令)

返回值: 系统命令返回的结果

```
os.system('ls')
```



#### 16.1.3 os模块中子模块path

##### 1. os.path.abspath() 

功能: 判断指定的路径是不是绝对路径

格式: os.path.abspath(指定路径)

返回值: True: 是绝对路径 False: 不是绝对路径

```
result = os.path.abspath('/Users/apple/desktop)
print(result)
```



##### 2. os.path.dirname() 

功能: 获取路径中的路径部分

格式: os.path.dirname(指定路径)

返回值: 返回路径部分

```
dname = os.path.dirname('/Users/apple/desktop')
print(dname)
```



##### 3. os.path.basename()

功能: 获取路径中文件的主体部分(文件名.扩展名)

格式: os.path.basename()

返回值: 返回指定路径的主体部分

```
bname = os.path.basename('/Users/apple/desktop)
print(bname)
```



##### 4. os.path.join()

功能: 将两个路径连接起来,合成一个路径

格式: os.path.join(路径1,路径2)

返回值: 合成之后的路径

```
fullpath = os.path.join('/Users/apple','desktop')
print(fullpath)
```



##### 5. os.path.split()

功能: 将指定路径的文件拆分成路径和主体部分,放入元组中

格式: os.path.split(指定绝对路径)

返回值: 元组 (路径部分,主体部分)

```
path1 = '/Users/apple/desktop/01.txt'
tuple1 = os.path.split(path1)
print(tuple1)
```



##### 6. os.path.splitext()

功能: 将指定路径的文件拆封成路径主体 和 扩展名,放入元组

格式: os.path.splitext(指定路径)

返回值: 元组 (名称,扩展名)

```
path1 = '/Users/apple/desktop/01.txt'
tuple1 = os.path.splitext(path1)
print(tuple1)
```



##### 7. os.path.getsize()

功能: 获取指定路径的文件大小.无法获取文件夹大小!

格式: os.path.getsize(指定文件路径)

返回值: 文件大小

```
path1 = '/Users/apple/desktop/01.txt'
size = os.path.getsize(path1)
print(size)
```



##### 8. os.path.isdir()

功能: 判断指定路径是不是文件夹

格式: os.path.isdir(指定路径)

返回值: True 是文件夹  False  不是文件夹

```
result = os.path.isdir('/Users/appple/desktop')
print(result)
```



##### 9. os.path.isfile()

功能: 判断指定路径是不是文件

格式: os.path.isfile(指定路径)

返回值: True 是文件  False 不是文件

```
result = os.path.isfile('/Users/apple/desktop/01.txt')
print(result)
```



##### 10. os.path.islink()

功能: 判断指定路径是不是快捷方式

格式: os.path.islink(指定路径)

返回值: True 是链接  False 不是链接

```
result = os.path.islink('/Users/apple/desktop/01.txt')
print(result)
```



##### 11. os.path.getctime()

功能: 获取指定路径的文件或者文件夹的创建时间

格式: os.path.getctime(指定路径)

返回值: 时间戳

```
creattime = os.path.getctime('/Users/apple/desktop/test/')
print(creattime)
```



##### 12. os.path.getatime()

功能: 获取指定路径的文件或者文件夹的访问时间

格式: os.path.getatime(指定路径)

返回值: 时间戳

```
activetime = os.path.getatime('/Users/apple/desktop')
print(activetime)
```



##### 13. os.path.getmtime() 

功能: 获取指定路径文件或者文件夹的修改时间

格式: os.path.getmtime(指定路径)

返回值: 时间戳

```
modifytime = os.path.getmtime('/Users/apple/desktop/01.txt)
print(modifytime)
```



##### 14. os.path.exists() 

功能: 判断指定路径的文件或者文件夹是否存在

格式: os.path.exists(指定路径)

返回值: True 存在  False 不存在

```
result = os.path.exists(指定路径)
print(result)
```



##### 15. os.path.isabs()

功能: 判断指定路径是不是一个绝对路径

格式: os.path.isabs(指定路径)

返回值: True 是绝对路径 False 不是绝对路径

```
result = os.path.isabs('/Users/apple/desktop/01.txt')
print(result)
```



##### 16. os.path.samefile()

功能: 判断两个路径指向的是不是同一个文件

格式: os.path.samefile(指定路径1,指定路径2)

返回值: True 是相同文件  False 不是同一个文件

```
path1 = '../../desktop/01.txt
path2 = '/Users/apple/desktop/01.txt'
result = os.path,sanmefile(path1,path2)
print(result)
```



#### 16.1.4 os模块中的值

##### 1. os.curdir

print(os.dir)

当前文件夹符号     

用 . 来表示



##### 2. os.pardir

print(os.pardir)

当前文件夹的上一层目录   即父级文件夹

用 .. 表示



##### 3. os.name

print(os.name)

当前系统的内核名称

win — > nt    linux/unix -> posix



##### 4. os.linsep

print(os.sep)

当前系统的默认换行符

win -> \r\n    linux/unix -> \n



##### 5.os.sep

print(os.sep)

当前系统的路径分隔符

win -> / or \    linux/unix -> /



##### 6. os.extsep

print(os.extsep)

当前系统的文件名和后缀之间的分隔符

win/linux/unix -> .



#### 16.1.5 自定义函数获取文件夹大小

```
# 自定义函数获取文件夹大小
import os

def get_dir_size(path):
    # 获取指定文件夹的文件信息
    lists = os.listdir(path)
    
    # 初始化大小计数
    size = 0
    # 通过拼接获取完整路径
    for i in lists:
        fullpath = os.path.join(path,i)
        
        # 判断路径是不是文件,是文件则获取大小并累加到size.
        if os.path.isfile(fullpath) or os.path.islink(fullpath):
            size += os.path.getsize(fullpath)
        
        # 判断路径是不是文件夹,如果是文件夹则递归计算大小,累加到size中
        elif os.path.isdir(fullpath):
            size += get_dir_size(fullpath)
    return size

# 调用函数
result = get_dir_size('/Users/apple/desktop/python教材')
print(result)
```



## 17. shutil 高级系统模块

使用shutil高级系统模块需要先导入该模块

import shutil

### 17.1 复制功能函数

#### 17.1.1 文件复制类函数

##### 1. shutil.copy()

功能: 将指定路径的文件复制到另一个路径

格式: shutil.copy('原文件路径','目标路径')

返回值: 目标路径

```
import shutil
shutil.copy('/Users/apple/desktop/01.py','/Users/apple/desktop/test/a.py')
```



##### 2. shutil.copy2()

功能: 复制指定路径的文件和文件信息到指定另一个路径

格式: shutil.copy2('原文件路径','目标路径')

返回值: 目标路径

```
import shutil
shutil.copy2('/Users/apple/desktop/01.py','/Users/apple/desktop/test/a.py')
```



##### 3. shutil copyfile()

功能: 复制指定文件的内容到另一个文件中(默认清空另一个文件)

格式: shutil.copyfile('原文件路径','目标路径')

返回值: 目标文件路径

```
import shutil
shutil.copyfile('/Users/apple/desktop/01.txt','/Users/apple/desktop/test/a.txt')
```



##### 4. shutil copyfileobj()

功能: 复制指定文件的内容到另一个文件中(可选择打开模式)

格式: shutil.copyfileobj(open('原文件路径','打开模式'),open('目标地址','打开模式'))

```
import shutil
shutil.copyfileobj(open('/Users/apple/desktop/01.txt','r'),open('/Users/apple/desktop/test/a.txt','a'))
```



#### 17.1.2 文件夹复制类函数

##### 1. copytree()

功能: 复制一个文件夹到指定位置

格式: shutil.copy('原文件夹路径','指定路径') 

```
import shutil
shutil.copytree('/Users/apple/desktop/test/','/Users/appple/desktop/a/')
```



##### 2. copymod()

功能: 复制一个文件夹的权限给另一个文件夹(两个必须都存在)

格式: shutil.copymod('原文件夹路径','指定路径')

```
import shutil
shutil.copymod('/Users/apple/desktop/test/','/Users/apple/deskt/a/)
```



##### 3. copystat()

功能: 复制一个文件夹的相关信息给另一个文件夹(两个都必须存在)

格式: shutil.copystat('原文件夹路径','目标文件夹路径')

```
import shutil
shutil.copystat('/Users/apple/desktop/a','/Users/apple/desktop/test/')
```



#### 17.1.3 文件夹(非空)递归删除函数

##### 1. rmtree()

功能: 递归删除非空文件夹 (os.removedirs()只能递归删除空文件夹)

格式: shutil.rmtree('删除文件夹的路径')

```
import shutil
shutil.rmtree('/Users/apple/desktop/test')
```



#### 17.1.4 文件和文件夹通用函数

##### 1. move() 

功能: 剪切,将指定文件剪切到另一个位置

格式: shutil.move('原文件路径','指定路径')

```
import shutil

shutil.move('/Users/apple/desktop/a/01.py','/Users/apple/desktop')

shutil.move('/Users/apple/PycharmProjects','/Users/apple/desktop/')
```



#### 17.1.5 系统相关函数

##### 1. which()

功能: 查找系统命令所在的文件路径

格式: shutil.which('系统命令')

返回值: 命令所在的系统变量PATH

```
import shutil
result = shutil.which('ls')
print(result)
```



##### 2. disk_usage()

功能: 获取指定系统磁盘的使用情况

格式: shutil.disk_usage('系统磁盘路径')

```
import shutil
result = shutil.disk_usage('/')
print(result)
```



#### 17.1.6 归档和解档函数

##### 1. shutil.make_archive()

功能: 创建一个归档文件,指定归档文件的格式.再将其他文件或文件夹放入归档文件中

格式: shutil.make_archive('归档文件路径','归档文件格式','放入的文件或文件夹路径')

```
import shutil
shutil.make_archive('/Users/apple/desktop/guidan','zip','/Users/apple/desktop/test')
```



##### 2. shutil.unpack_archive()

功能: 将归档文件夹中的全部文件解包到指定路径

格式: shutil.unpack_archive('归档文件路径','输出路径')

```
import shutil
shutil.unpack_archive('/Users/apple/desktop/guidan.zip','/Users/apple/desktop/nimabi')
```



##### 3. shutil.get_archive_formats()

功能: 获取当前系统允许的压缩文件格式

```
import shutil
result = shutil.get_archive_formats()
print(result)
```



##### 4. shutil.get_unpack_foramats()

功能: 获取当前系统中允许的解包格式

```
import shutil
result = shutil.get_unpack_formats()
print(result)
```





##### 18. zipfile模块-zip压缩

进行压缩操作之前要先导入压缩模块

import zipfile

### 18.1 zipfile模块常用函数



#### 1. zipfile.ZipFile() 

功能: 创建一个压缩文件

格式: zipfile.ZipFile(1.创建压缩文件位置, 2.打开模式, 3.是否压缩, 4.压缩文件是否大于2G)

```
参数:
1. 创建压缩文件绝对路径
2. 打开模式 
	w : 新建一个压缩文件夹,或者覆盖一个已有的zip文档
	a : 将数据追加到一个现存的zip文档中
	r : 打开一个已有的zip文件
3. 压缩方式:
	zipfile.ZIP_STORED 		不存储不进行压缩(默认)
	zipfile.ZIP_DEFLATED 	对文件进行压缩
4. 压缩文件是否大于2G
	若创建的压缩文件要大于2G,则将zip64 设为 True
	若创建的压缩文件不需要2G,则默认False
```



#### 2. zipfile.write()

功能: 将指定文件添加到zip文件中

格式: zipfile.write(要添加的文件,添加后新名字,压缩方式)

```
参数:
1. 要添加的文件:  
	要写入压缩文件中的添加文件的绝对路径
2. 添加后的新名字:
	在压缩文件中的名字,如果不需要更改则不需要传参即可
3. 压缩方式:
	压缩方式,若指定则可以单独设定,不指定则按创建zip文件时设定的进行
```



#### 3. extractall()

功能: 从zip压缩文件中解压缩所有的文件

格式: zipfile.extractall(指定输出路径)



#### 4. extarct()

功能: 从zip压缩文件中取出指定的文件

格式: zipfile.extract(指定文件,指定输出路径)



### 18.2 压缩文件操作范例

```
import zipfile

# 打开或者创建一个压缩文件
zp = zipfile.ZipFile('/Users/apple/desktop/01.zip','w',zipfile.ZIP_DEFLATED)

# 向创建好的压缩文件中添加要压缩的文件
zp.write('/Users/apple/desktop/01.txt)
zp.write('/Users/apple/desktop/test.py','hellotest.py')

# 关闭压缩文件
zp.close()
```



### 18.3 解压文件操作范例

```
import zipfile

# 打开压缩文件
zp = zipfile.ZipFile('/Users/apple/desktop/01.zip','r')
# 将需要的指定文件或者全部文件解压缩出来
zp.extract('01.txt','/Users/apple/desktop/aa')
zp.extractall('/Users/apple/desktop/bbb')

# 关闭压缩文件
zp.close()
```



### 18.4 zipfile模块其他函数

#### 1. zipfile.namelist()

功能: 获取zip文件中的所有文件列表

格式: zipfile.namelist()

```
zp = zipfile.ZipFile('/Users/apple/desktop/01.zip','r')

print(zp.namelist())

zp.close()
```



#### 2. zipfile.infolist()

功能: 获取zip文件中的所有信息列表

格式: zipfile.infolist()

```
zp = zipfile.ZipFile('/Users/apple/desktop/01.zip','r')

print(zp.infolist())

zp.close()
```



#### 3. zipfile.getinfo()

功能: 获取zip文件中指定文件的信息

格式: zipfile.getinfo(指定文件)

```
zp = zipfile.ZipFile('/Users/apple/desktop/01.zip','r')

print(zp.getinfo('test.txt'))

zp.close()
```



## 19. tar 模块

使用tar模块之前需要先导入模块

import tar

### 19.1 tar 模块常用函数

#### 1. tar.open()

功能: 创建或者打开压缩文件

格式: tar.open('创建或者打开的压缩文件名','打开模式')

注意: 打开模式中 使用w则默认不压缩  要压缩的话使用w:gz等压缩格式



#### 2. tar.add() 

功能: 向压缩文件中添加内容

格式: tar.add('添加到压缩文件中的文件或文件夹路径','可为空新名字')



#### 3. tar.extract() 

功能: 将压缩文件中的指定文件解压到指定路径

格式: tar.extract('指定路径','解压目标路径')



#### 4. tar.extractall()

功能: 将压缩文件中的所有文件解压到指定路径

格式: tar.extarctall('解压目标路径')



#### 5. tar压缩范例

```
import tar
tarfp = tar.open('/Users/apple/desktop/01.tar','w:gz')

tarfp.add('/Users/apple/desktop/01.py')
tarfp.add('/Users/apple/desktop/test/')


tarfp.close()
```



#### 6. tar解压范例

```
import tar
tarfp = tar.open('/Users/apple/desktop/01.tar','r')

tarfp.extract('01.py','/Users/apple/desktop/')
tarfp.extarctall('/Users/apple/desktop/a/')

tarfp.close()
```



## 20. calendar 日历模块

使用日历模块之前需要先导入日历模块

import calendar

### 20.1 日历模块函数

#### 1. calendar.calendar()

功能: 获取指定年份的日历字符串

格式: calendar.calendar(年份)

```
import calendar
result = calendar.calendar(2017)
print(result)
```



#### 2. calendar.month()

功能: 获取指定年月的日历字符串

格式: calendar.month(年份,月份)

```
import calendar
result = calendar.month(2017,10)
print(result)
```



#### 3. calendar.monthcalendar()

功能: 指定年份和月份获取一个时间矩阵列表

格式: calendar.monthcalendar(年份,月份)

```
import calendar
result = calendar.monthcalendar(2017,10)
print(result)
```



#### 4. calendar.monthrange()

功能: 通过指定的年月,获取该月份第一天是周几,一共多少天

格式: calendar.monthrange(年份,月份)

```
import calendar
result = calendar.monthrange(2017,10)
print(result)
```



#### 5. calendar.isleap()

功能: 判断指定年份是不是闰年

格式: calendar.isleap(年份)

```
import calendar
result = calendar.isleap(2017)
print(result)
```



#### 6. calendar.leapdays()

功能: 判断两个指定年份之间有多少个闰年

格式: calendar.leapdays(开始年份,结束年份)

```
import calendar
result = calendar.leapdays(2000,2011)
print(result)
```



#### 7. calendar.weekday()

功能: 通过指定年月日,计算这一天是周几

格式: calendar.weekday(年份,月份,日期)

注意: 0–6 表示 周一 — 周天

```
import calendar
result = calendar.weekday(2017,10,13)
print(result)
```



#### 8. calendar.timegm()

功能: 将时间元组转换成时间戳

格式: calendar.timegm(时间元组)

```
import calendar
ttp = (2018,1,1,0,0,0,0,0,0)
result = calendar.timegm(ttp)
print(result)
```



## 21. time 日历模块

### 21.1 时间术语解释

#### 21.1.1 UTC时间

```
UTC时间又称为世界协调时间,特指格林尼治天文台所在的位置的时间,也叫格林尼治时间.
中国的时区是东八区,比世界协调时间快了8个小时
```



#### 21.1.2 夏令时

```
夏令时就是通过在夏季将时间人为调快1个小时.
```



#### 21.1.3 时间元组

```
ttp = (年,月,日,时,分,秒,周几,第几天,是否夏令时)
年 : 4位数字
月 : 1-12
日 : 1-31
时 : 0-23
分 : 0-59
秒 : 0-59
周几 : 0-6 对应 周一 - 周天
是否不是夏令时: 0是,其他不是
```



### 21.2 时间模块的值

#### 1. timezone

功能: 获取UTC和当前时区时间戳的差值 (UTC时间戳 - 当前时区时间戳)

```
import time 
print(time.timezone)
```



#### 2. altzone

功能: 在夏令时的情况下,获取UTC时间和当前时区的差值

```
import time 
print(time.altzone)
```



#### 3. daylight

功能: 检测是否是夏令时,0 就是 夏令时  非零不是夏令时

```
import time 
print(time.daylight)
```



### 21.3 时间模块的函数

#### 1. time.asctime() 

功能: 把时间元组转换成可读字符串

格式: time.asctime(时间元组)

```
import time 
result = time.asctime((1992,2,1,21,33,44,0,0,0))
print(result)
```



#### 2. time.localtime()

功能: 获取当前的时间元组

格式一: time.localtime()

​	返回值: 当前的时间元组

格式二: time.localtime(时间戳)

​	返回值: 指定时间戳转换成本地时间元组

```
import time 
result = time.localtime()
print(result)

result = time.localtime(1231424)
print(result)
```



#### 3. time.gmtime()

功能: 获取当前UTC时间元组

格式一: time.gmtime()

​	返回值: 当前UTC时间元组

格式二: time.gmtime(12414413)

​	返回值: 将指定时间戳转换成UTC时间元组

```
import time
result = time.gmtime()
print(result)

result = time.gmtime(135454426)
print(result)
```



#### 4. time.ctime()

功能: 获取本地时间的字符串格式

time.ctime() == time.asctime(time.locatime())

```
import time 
result = time.ctime()
print(result)
```



#### 5. time.mktime()

功能: 将时间元组转换成时间戳

格式: time.mktime(时间元组)

```
import time
result = time.mktime((1992,2,1,23,45,22,0,0,0))
print(result)
```



#### 6. time.clock()

功能: 获取当前cpu时间,多用于计算程序运行时间

格式: time,clock()

```
import time

starttime = time.clock()

lists = [i *  2 for i in range(1,10000)]

endtime = time.clock()

ptime = endtime - starttime
print(ptime)
```



#### 7. time.perf_counter()

功能: 获取当前cpu时间,可计算sleep()的时间.推荐使用

格式: time.perf_counter

```
import time

starttime = time.perfcounter()

time.sleep(2)

endtime = time.perf_counter()

ptime = endtime - starttime
print(ptime)
```



#### 8. time.sleep() 

功能: 使程序睡眠,在此处等待指定的秒数

格式: time.sleep(秒数)

```
import time

time.sleep(15)

print('有完没完了测试需要15s么!?')
```



#### 9. time.strftime()

功能: 指定时间字符的格式,将指定的时间元组转换成指定格式字符

格式: time.strftime('字符格式',时间元组)

字符格式中:

​	%Y		代表年

​	%m		代表月

​	%d		代表日

​	%H		代表时

​	%M		代表分

​	%S		代表秒

```
import time
ttp = (1992,2,1,0,2,3,0,0,0)

result = time.strftime('%Y年%m月%d日,%H时%M分%S秒',ttp)
print(result)
```



#### 10. time.strptime()

功能: 将格式化之后的时间字符按之前的格式还原到时间元组

格式: time.strptime('格式化之后的字符串','格式化的格式')

```
import time

result = time.strptime('1992年2月1日,0时2分3秒','%Y年%m月%d日,%H时%M分%S秒')

print(result)
```



#### 11. time.time()

功能: 获取本地的时间戳

格式: time.time()

```
import time
print(time.time())
```


# Python第二阶段
***
## 1、多进程
### 1.1进程创建方法一—fork
fork系统自带方法，仅用于Linux系统
* 程序执行到os.fork时,操作系统会创建一个新的进程(子进程),然后复制父进程的所有信息到子进程中
* 然后父进程和子进程都会从fork()函数中得到一个返回值,在子进程中这个值一定是0,而父进程中是子进程的id号
```
import os

p = os.fork()
print(p)
```
* os.getpid():当前进程的ID

* os.getppid():当前进程的父进程ID--parent:双亲,忽略性别(father,只是父亲的意思),这里用parent更严谨
```
os.getpid()  #获取子进程的ID
os.getppid()  #获取父进程的ID
```
### 1.2多次fork问题
子进程在复制父进程资源的时候，也将父进程的执行进程也复制过去了，所以子进程中的代码并非全部从头到尾执行。
### 1.3多进程修改全局变量
多进程中,每个进程中所有的数据(包括变量)都各拥有一份,互不影响
### 1.4进程创建方法二—multiprocessing
multiprocessing模块提供了一个Process类来代表一个进程对象
### 1.5自定义进程类—继承  Process
1.从multiprocessing模块中导入Process类
2.进程操作
1.创建
创建子进程时，只需要传入一个执行函数和函数的参数，创建一个Process实例

创建格式：p=Process(target=函数名)
2.启动
启动格式：进程对象名.start()
```
Process([group[,target[,name[,args[,kwargs]]]]])

   target:表示这个进程实例所调用的对象
   arge:表示调用对象的位置参数元祖
   kwargs:表示调用对象的关键字参数字典
   name:为当前进程实例

常用方法:
   start():启动进程实例(创建子进程);
   join([timeout]):是否等待进程执行结束,或等待多少秒,阻塞
```
```python
#例子：
from multiprocessing import Process
import os

# 子进程要执行的代码
def download():
    print("开启进程id:%d"%os.getpid())
if __name__=="__main__":
    print("主进程id:%d"%os.getpid())
    p=Process(target=download) #函数名不加括号

    p.start()
```
*** 
- 实例：从键盘输入一个整数,分别开启两个进程来计算这个数的累加和和阶乘
第一个进程用系统提供给我们的类
第二个进程需要自己定义
```python

from multiprocessing import Process

def sum(msg):
    j=0
    for i in range(1,msg+1):
        j+=i
    print('%d的累加和是%d'%(msg,j))

if __name__=="__main__":
    num=input('请输入一个整数：')
    num=int(num)

    p1=Process(target=sum,args=(num,))
    p1.start()
    p1.join()
    print('都计算完毕')
****************************

# 创建进程实例2
# 阶乘
from multiprocessing import Process

class JieChen(Process):
    def __init__(self  ): # 参数a用来传入一个数，控制所求阶乘的范围
        Process.__init__(self)

    def run(self):
        pass

    def jiechen(self,a):
        j=1
        for i in range(1,a+1):
            j*=i
        print('%d的阶乘是%d'%(a,j))



# 主进程的入口
if __name__=="__main__":
    # 实例化自定义的类
    p=JieChen()
    p.start()
    p.jiechen(20)
    p.join()
    print('进程执行完毕')


```
*** 
### 1.6进程池pool
* 使用multiprocessing模块提供的Pool方法.

```python
#开启进程池
def shangchuang(msg):
    print('开始上传第%d音乐'% msg)
    time.sleep(1)
    print('上传第%d首音乐成功'% msg)

if __name__=='__main__':
    # 创建进程池
    p = Pool(5)

    for i in range(0,10):
        p.apply_async(func=shangchuang,args=(i,))
    p.close()
    p.join()
    print('上传所有音乐成功')
```
### 1.7进程间通信—Queue
* 使用multiprocessing模块的Queue实现多进程之间的数据传递
*** 
```
初始化Queue()对象时（例如：q=Queue()），若括号中没有指定最大可接收的消息数量，或数量为负值，那么就代表可接受的消息数量没有上限（直到内存的尽头）；
Queue.qsize()：返回当前队列包含的消息数量；
Queue.empty()：如果队列为空，返回True，反之False ；
Queue.full()：如果队列满了，返回True,反之False；
Queue.get([block[, timeout]])：获取队列中的一条消息，然后将其从列队中移除，block默认值为True；
1）如果block使用默认值，且没有设置timeout（单位秒），消息列队如果为空，此时程序将被阻塞（停在读取状态），直到从消息列队读到消息为止，如果设置了timeout，则会等待timeout秒，若还没读取到任何消息，则抛出"Queue.Empty"异常；
2）如果block值为False，消息列队如果为空，则会立刻抛出"Queue.Empty"异常；
Queue.get_nowait()：相当Queue.get(False)；
Queue.put(item,[block[, timeout]])：将item消息写入队列，block默认值为True；
1）如果block使用默认值，且没有设置timeout（单位秒），消息列队如果已经没有空间可写入，此时程序将被阻塞（停在写入状态），直到从消息列队腾出空间为止，如果设置了timeout，则会等待timeout秒，若还没空间，则抛出"Queue.Full"异常；
2）如果block值为False，消息列队如果没有空间可写入，则会立刻抛出"Queue.Full"异常；
Queue.put_nowait(item)：相当Queue.put(item, False)；
```
***

```python
from multiprocessing import  Pool,Process,Queue,Manager

#开启2个进程，向进程池里读写信息，不是使用进程池pool****************
def write(q):
    for i in ['小米','苹果','华为','VIVO']:
        print('Starting! Write %s' % i)
        q.put('%s公司好屌的样子！' % i)
        print('写入%s成功' % i)

def read(q):
    while True:
        if not q.empty():
            for msg in range(q.qsize()):
                message = q.get()
                print('读出消息%s'%message)
        else:
            break


if __name__=='__main__':
    q = Queue()
    # 写入
    q_write = Process(target=write, args=(q,))
    q_write.start()
    q_write.join()

    # 读取
    q_read = Process(target=read, args=(q,))
    q_read.start()
    q_read.join()

```
* 使用进程池Pool创建进程 
如果要使用Pool创建进程，就需要使用multiprocessing.Manager()中的Queue()，而不是multiprocessing.Queue()。
```python
from multiprocessing import  Pool,Process,Queue,Manager
# ***************开启2个进程，使用进程池pool*********************
def write(q):
    for i in ['小米', '苹果', '华为', 'VIVO']:
        print('Starting! Write %s' % i)
        q.put('%s公司好屌的样子！' % i)
        print('写入%s成功' % i)

def read(q):
    while True:
        if not q.empty():
            for msg in range(q.qsize()):
                message = q.get()
                print('读出消息%s' % message)
        else:
            break


if __name__ == '__main__':
    q = Manager().Queue()
    p = Pool()

    p.apply_async(func=write,args=(q,))
    p.apply_async(func=read,args=(q,))

    p.close()
    p.join()
```
***
## 2、多线程
* 进程是系统进行资源分配和调度的一个独立单位.
* 线程是进程的一个实体,是CPU调度和分派的基本单位,它是比进程更小的能独立运行的基本单位.线程自己基本上不拥有系统资源,只拥有一点在运行中必不可少的资源(如程序计数器,一组寄存器和栈),但是它可与同属一个进程的其他的线程共享进程所拥有的全部资源.
* 多线程的五种状态
```markdown
（1）run（运行状态）：正在运行的进程或在等待队列中对待的进程，等待的进程只要以得到cpu就可以运行
（2）Sleep（可中断休眠状态）：相当于阻塞或在等待的状态
（3）D（不可中断休眠状态）：在磁盘上的进程
（4）T（停止状态）：这中状态无法直观的看见，因为是进程停止后就释放了资源，所以不会留在linux中
（5）Z（僵尸状态）：子进程先与父进程结束，但父进程没有调用wait或waitpid来回收子进程的资源，所以子进程就成了僵尸进程，如果父进程结束后任然没有回收子进程的资源，那么1号进程将回收
```
### 2.1创建多线程
* 多线程的创建方法：用threading模块创建多线程。
1、第一种方式：把一个函数传入并创建Thread实例，然后调用start方法开始执行；
2、第二种方式：直接从threading.Thread继承并创建线程类，然后重写__init__方法和run()方法。
* 创建的两个实例:
```python
# 第一种方式,创建Thread实例
import random
import time, threading

def thread_run(urls):
	# threading.current_thread()后面不仅仅有.name属性,而且还有.getName()方法,虽然两者结果一样，但是性质不同
	# name 是当前线程的属性， getName 是当前线程的方法
	# 还可以修改当前线程name，threading.current_thread().name ＝ 'First'
	threading.current_thread().name = 'First_Thread'
	print('Current %s is running...'% threading.current_thread().name)
	for url in urls:
		print('%s ---->>>%s' % (threading.current_thread().name,url))
		time.sleep(random.random())
	print('%s ended.'% threading.current_thread().name)

if __name__ == '__main__':

	print('%s is running...'% threading.current_thread().name)
	t1 = threading.Thread(target=thread_run, name='Thread_1',args= (['url1','url2','url3'],))
	t2 = threading.Thread(target=thread_run, name='Thread_2',args=(['url4','url5','url6'],))

	t1.start() #开启线程一	
	t2.start() #开启线程二

	t1.join()
	t2.join()
	print('%s ended.'% threading.current_thread().name)



#第二种方式，创建类，重写__init__方法和run方法
import random, threading, time

class BigThread(threading.Thread):
	"""docstring for BigThread"""
	def __init__(self, name, urls):
		super(BigThread, self).__init__()
		self.urls = urls
	
	def run(self):
		print('Current %s is running...'% threading.current_thread().name)
		for url in self.urls:
			print('%s --->>>%s' %(threading.current_thread().name, url))
			time.sleep(random.random())
		print('%s ended.'% threading.current_thread().name)
    
if __name__ == '__main__':
	print('%s is running...'% threading.current_thread().name)
	t1 = BigThread( name='Thread_1',urls= (['url1','url2','url3'],))
	t2 = BigThread( name='Thread_2',urls=(['url4','url5','url6'],))
	# run()只是在主线程中调用了run函数，并没有开启新的线程，运行时间自然要长
	# t1.run()
	# t2.run()

	t1.start() #开启线程一
	t2.start() #开启线程二

	t1.join()
	t2.join()
	print('%s ended.'% threading.current_thread().name)
```

### 2.2线程同步
* 出现的问题：如果多个线程共同对某个数据修改，则可能出现不可预料的结果，为了保证数据的正确性，需要对多个线程进行同步。
* 解决方法：
使用Thread对象的Lock和RLock可以实现简单的线程同步，这二个对象都有
acquire方法和release方法，对于那些每次只允许一个线程操作的数据，可以
将其操作放到acquire和release方法之间。
  * Lock:如果一个线程连续二次进行acquire操作，如果第一次acquire之后没有release,第二次acquire将挂起线程，即锁死没有开锁。
  * RLock：RLock对象允许一个线程多次对其进行acquire操作，因为在其内部通过一个counter变量在维护着线程acquire的次数。而且每一次的acquire操作必须有一个release操作与之对应，在所有的release操作完成之后，别的线程才能申请该RLock对象。

```python
import threading

mylock = threading.RLock()
num = 0
class myThread(threading.Thread):
	"""docstring for myThread"""
	def __init__(self, name):
		super().__init__(name=name)

	def run(self):
		global num
		while True:
			mylock.acquire()
			print('%s locked,Number:%d' % (threading.current_thread().name,num))
			if num >= 4:
				mylock.release()
				print('%s released,Number:%d'%(threading.current_thread().name, num))
				break
			num += 1
			print('%s realased, Number:%d' % (threading.current_thread().name,num))
			mylock.release()

if __name__ == '__main__':
	thread_1 = myThread('Thread_1')
	thread_2 = myThread('Thread_2')

	thread_1.start()
	thread_2.start()
```
***
## 3、网络编程
### 3.1 Socket套接字
```markdown
   打开一个Socket需要知道目标计算机的IP地址和端口号，在指定协议即可。
Python提供了两个基本的Socket模块：
   * Socket，提供了标准的BSD Sockets API。
   * SocketServer，提供了服务器中心类，可以简化网络服务器的开发。
```
* Socket模块功能
1、Socket类型:
```markdown
套接字格式为:socket(family,type[,protocal]),使用给定的地址族、协议编号(默认为0)、套接字类型，来创建套接字，套接字类型如下：
```
Socket类型 |  描述 |
----------| ------
socket.AF_UNIX | 只能用于单一的Unix系统进程间的通信
socket.AF_INET | 服务器之间网络通信
socket.AF_INET6 | IPv6
socket.SOCK_STREAM |流式socket,用于TCP
socket.SOCK_DGRAM|数据报式socket用于UDP
socket.SOCK_RAW|原始套接字，普通的套接字无法处理ICMP、IGMP等网络报文，而     SOCK_RAW可以；其次，SOCK_RAW也可以处理特殊的IPv4报文。
socket.SOCK_SEQPACKET | 可靠的连续数据包服务
创建TCP Socket | s = socket.socket(socket.AF_INET,socket.SOCK_STREAM)
创建UDP Socket | s = socket.socket(socket.AF_INET,socket.SOCK_DGRAM)

2、Socket函数：
函数 | 描述
------|-----
服务端Socket函数：|
s.bind(address)|将套接字绑定到地址，在AF_INET下，以元组(('host',port))的形式表示地址
s.listen(backlog)| 开始监听TCP传入连接。backing指定在拒绝连接之前，操作系统可以挂起的最大连接数量。该值至少为1，大部分应用程序设为5就可以了
s.accept()|接受TCP连接并返回(conn,address),其中conn是新的套接字对象，可以用来接受和发送数据，address是连接客户端的地址。
客户端Socket函数：|
s.connect(address)|连接到address处的套接字。一般address的格式为元组(hostname,port),如果连接出错，返回socket.error错误
s.connect_ex(address)|功能与connect(address)相同，但是成功返回0，失败返回errno的值
共用Socket函数：|
s.recv(bufsize[,flag])|接受TCP套接字的数据。数据以字符串的形式返回，bufsize指定要接收的最大数据量。flag提供有关消息的其他信息，通常可以忽略
s.send(string[,flag])|发送TCP数据。将string中的数据发送到连接的套接字。返回值是要发送的字节数量，该数量可能小于string的字节大小
s.sendall(string[,flag])|完整发送TCP数据。将string中的数据发送到连接的套接字。但在返回之前会尝试发送所有的数据，成功返回None，失败抛出异常。
s.recvfrom(bufsize[,flag])|接受UDP套接字的数据.与recv()类似，但是返回值是(data.address)。其中data是包含接受数据的字符串,address是发送数据的套接字地址。
s.sendto(string[,flag],address)|发送UDP数据,将数据发送到套接字,address是形式为(ipaddr,port)的元组，指定远程地址。返回值是发送的字节数。
s.close()|关闭套接字
s.getpeername()|返回连接套接字的远程地址，返回值通常是元组(ipaddr，port)
s.getsockname()|返回套接字自己的地址,通常是一个元组(ipaddr,port)
s.setsockopt(level,optname,value)|设置给定套接字选项的值
s.getsockopt(level,optname[,buflen])|返回套接字选项的值
s.settimeout(timeout)|设置套接字操作的超时期，timeout是浮点数,单位是秒s,值为None表示没有超时期。
s.setblocking(flag)|如果flag为0，则将套接字设置为非阻塞模式,否则将套接字设置为阻塞模式(默认)非阻塞模式下如果调用recv()没有发现任何数据，或send()调用无法立即发送消息,将引起socket.error异常。

### 3.2 TCP编程
网络编程一般分为：服务端和客户端(主动发送的为客户端)
* 创建和运行TCP服务端：
```markdown
1、创建Socket,绑定Socket到本地IP和端口号
2、开始监听连接
3、进入循环，不断接受客户端的连接请求
4、接受传来的数据,并发送给对方数据
5、传输完毕后，关闭Socket。
```
```python
# 创建TCP服务端例子 ：
import socket, threading, time


def dealClient(sock, addr):
    # 第四步，接受传来的数据，并发送给对方数据
    print('Accept new connection from %s:%s...' % addr)
    sock.send('Hello , I am server!'.encode('utf-8'))
    while True:
        data = sock.recv(1024)
        time.sleep(1)
        if not data or data.decode('utf-8') == 'exit':
            break
        print('-->>>%s' % data.decode('utf-8'))
        sock.send(('Loop_Msg:%s' % data.decode('utf-8')).encode('utf-8'))
    # 第五步：关闭Socket
    sock.close()
    print('Connection from %s:%s closed.' % addr)


if __name__ == '__main__':
    # 第一步
    # Socket绑定的IP和端口号
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    s.bind(('169.254.124.183', 9595))  # IP地址和端口号（端口号可变）
    # 监听连接
    s.listen(5)
    print('Waiting for connection...')
    while True:
        # 第三步：接受一个新连接
        sock, addr = s.accept()
        # 创建线程
        t = threading.Thread(target=dealClient, args=(sock, addr))
        t.start()
```
* 创建和运行TCP客户端：
```markdown
1、创建Socket,连接远端地址
2、连接后发送数据和接受数据
3、传输完毕后，关闭Socket客户端
```
```python
# 创建TCP客户端的例子：
import socket

# 初始化Socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.connect(('169.254.124.183', 9595))  # IP地址和端口号（端口号服务端开启的端口号）

print('-->>'+s.recv(1024).decode('utf-8'))

s.send(b'Hello ,i am client!')
print('-->>'+s.recv(1024).decode('utf-8'))
s.send(b'exit')
s.close()
```


### 3.3 UDP编程
使用UDP协议,不需要建立连接,只需要知道对方的IP地址和端口号即可发送数据包,但是不用考虑是否会到达目的端。用UDP传输数据不可靠，但是它速度不TCP快。
* UDP服务端的创建和运行
```markdown
1、创建Socket,绑定指定的IP和端口号
2、直接发送数据和接受数据
3、关闭Socket
```
```python
# 创建UDP服务端的例子
import socket
# 1. 创建一个套接字   # SOCK_DGRAM(u传输协议的类型---UDP)
udp_ser=socket.socket(socket.AF_INET,socket.SOCK_DGRAM)

# 2.绑定自己的ip地址和端口号 (绑定门牌号)
udp_ser.bind(('',8000))

# 3.接收消息 是一个元祖包含接收到的消息和发送者的ip端口号
while True:
    data,addr=udp_ser.recvfrom(1024)
    print(data.decode('utf-8'))
    udp_ser.sendto('我不去,真不去,房间号地址告诉我'.encode('utf-8'),addr)

# 关闭套接字
udp_ser.close()
```
* UDP客户端的创建和运行
```markdown
创建Socket，直接可以与服务端进行数据交换
1、创建Socket套接字
2、给服务端发送数据
3、接受服务端发送过来的信息
```
```python
import socket

# 1. 创建一个套接字
udp_cl=socket.socket(socket.AF_INET,socket.SOCK_DGRAM)

# 2.发送
udp_cl.sendto('aaa'.encode('utf-8'),('169.254.206.44',8000))

# 2.接收
data,addr=udp_cl.recvfrom(1024)
print(data.decode('utf-8'))
# 关闭套接字
udp_cl.close()
```

### 3.4 HTTP协议
HTTP协议（HyperText Transfer Protocol，超文本传输协议）是用于从WWW服务器传输 超文本到本地浏览器的传送协议。
1、HTTP请求过程
```markdown
HTTP协议采取的是请求响应模型，HTTP协议永远都是客户端发起请求，服务器回送响应。
HTTP协议是一个无状态的协议，同一个客户端的这次请求和上次请求没有对应的关系。一次HTTP操作称为一个事务，其执行过程可分为四步：
* 1、首先客户端和服务端需要建立连接
* 2、建立连接后，客户端发送一个请求给服务器，请求方式的格式为：统一资源标识符（URL）、协议版本号，后边是MIME信息，包括请求修饰符、客户机信息和可能的内容。
* 3、服务端连到请求后，给予相应的响应信息，其格式为一个状态行，包括信息的协议版本号、一个成功或错误的代码，后边是MIME信息，包括服务器信息、实体信息和可能的内容。
* 4、客户端接受服务端所返回的信息，通过浏览器将信息显示在用户的显示屏上，然后客户端与服务端断开连接。
```
2、HTTP状态码含义
```markdown
* 200——请求成功
* 301——资源（网页等）被永久转入其他URL
* 404——请求的资源（网页等）不存在
* 500——内部服务器错误
```
分类|分类描述
---|---
1**|信息，服务器收到的请求，需要请求者继续执行操作
2**|成功，操作被成功接收并处理
3**|重定向，需要进一步的操作以完成请求
4**|客户端错误，请求包含语法错误或无法完成请求
5**|服务端错误，服务器在请求的过程中发生了错误

3、HTTP头部信息
get
post







































# Python第三阶段