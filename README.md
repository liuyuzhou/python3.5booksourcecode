# python3.5booksourcecode
python3.5 从零开始学各章节源码


下面为目前发现的错误勘误，以第一版为参照，后续版本已经有部分修正：

1、p12
图1-16中的 python 打错了，打成 pyhton 了， t和h 位置反了
需更正为 python


2、p25  倒数第三行：
这里使用的是整形
需更改为  这里使用的是整型


3、p37  表2-1 算术运算符中  
a/b输出结果为2 更改为 2.0
b%a 输出结果为0 更改为 a%b 输出结果为0


4、p55
从上往下的第二个代码块：
>>>number=[1,2,3,4,5,6,7,8,9,10]
>>>number[-3,-1]    此处错误。  应改为 number[-3:-1]
[8,9]


5、p61  第二段代码，第三行处漏了一行代码

[1,10,'hello',10,1]   这行代码下面需要添加一行代码，代码形式如下：

>>>type(a)


6、p68  
错误问题，描述错误：问题 

需将该页的 5.insert
insert()方法用于从列表中找出某个值第一个匹配项的索引位置。

更正为：insert()方法用于将对象插入列表。


7、p87
空白（“”）则表示在正数前加上空格。如下输入：
>>> print(('% 5d'%10)+'\n'+('% 5d'%-10))

这个输入需要更改为：
>>> print(('% 5d' % 10)+'\n'+('% 5d' % -10))


8、p88  4.3.2 join()方法对应的第一段代码：
>>> num=[1,2,3,4]
>>> mark.join(num)

这里漏了一句，完整的应该如下：
>>> num=[1,2,3,4]
>>> mark='+'
>>> mark.join(num)


9、
p92 第三行最后一句有错误
原句：指定第3个字符时
更改为：指定第3个参数时


10、p93问题 
intab='adfas'  更改为 intab='adefs'


11、P103   5.3.3 fromkeys()方法， 返回结果为字典，而非列表。 需要把列表二字更改为字典。


12、p135
需将第一段代码中的第六行  num -= -1 更改为num -= 1


13、P157    7.6.1 局部变量 代码块 def func() 中， 最后两行代码未缩进。
需更改为：
def func():
    x = 100
    print(x)


14、p162  示例代码中
justreturn函数的return语句丢失，应更改为如下：
def justreturn():
    print('justreturn函数只写return，不返回具体内容')
	return
	

print结果的语句中丢失了一句，
print('函数noreturn调用结果：',noreturn())
print('函数justreturn调用结果：',justreturn())
print('函数returnval调用结果：',returnval())

需要加上中间那句才能得到打印的结果。


15、书中168页的尾递归函数一般只能递归fact(997)，递归深度超过997后，应该会报如下错误：
RecursionError: maximum recursion depth exceeded in comparison

要能测试fact(1000)
需要加入如下设置：
import sys  
  
sys.setrecursionlimit(10000) #例如这里设置深度为一万  


16、p187 
完整代码块中的get_score 函数中存在代码缩进错误，原来代码如下：
    def get_score(self):
        return self.__score

    if 0<=score<=100:
            self.__score = score
        else:
            print('请输入0到100的数字。')
			
			
需要更正为（漏了一个set_score函数）			
	def get_score(self):
        return self.__score
		
	def set_score(self, score):
	    if 0<=score<=100:
                self.__score = score
            else:
                print('请输入0到100的数字。')
		

			
17、p197
stu = Student0('xiaomeng', 95)
这个语句后面漏了一句，不加上后面的执行结果打印不出来

需要修正为：
stu = Student0('xiaomeng', 95)
stu.info()

即加上   stu.info()  这个语句


18、
p207
因为这两者本来就有根本区别   修改为：因为这两者本来就没有根本区别


19、p216  
若把a=1/0注释掉或放到b=name下面
需要更改为
若把a=x/y注释掉或放到b=name下面
即把   a=1/0   更改为    a=x/y
		
			
20、p234
第4 和 5 点，需要修改
4. fromtimestamp(timestamp[, tz]) 下面的代码块：
import datetime

print('fromtimestamp is:', datetime.datetime.fromtimestamp(time.time()))

这里少了一条语句，需要更改为如下（还需要导入time）：
import datetime, time

print('fromtimestamp is:', datetime.datetime.fromtimestamp(time.time()))

5. utcfromtimestamp(timestamp)
import datetime

print('utcfromtimestamp is:', datetime.datetime.utcfromtimestamp(time.time()))

这里同样少了一条语句，需要更改为如下（还需要导入time）：
import datetime, time

print('utcfromtimestamp is:', datetime.datetime.utcfromtimestamp(time.time()))


21、p235
 7.strftime(format)下
 将格式字符串转换为datetime对象。  更正为：  将datetime对象转换为格式字符串。
 返回一个datetime对象。   更正为：   返回一个字符串对象。
 

22、
p238
缺少三个import语句，需添加如下：
import time
import datetime
import calendar


23、
p249
11.3节 示例代码 缺少import语句，需要添加如下：
import re


24、
p250
11.4节  示例代码 缺少import语句，需添加如下：
import re


25、p258
第二部分的代码片段有一个错误
f_name = open(path, 'w')
print('write length:', f_name.write('Hello world!'))
f_name = open(path,'r')
print('read result:', f_name.read())

f_name = open(path, 'a')
print(add length:', f_name.write('welcome!'))    ######该行需要修正为：print(add length:', f_name.write('\nwelcome!'))
f_name = open(path,'r')
print('read result:', f_name.read())


26、
p263
12.3.2 按行操作 一节下的代码，需更改如下：
if not c_str:   更改为：if not line:

			
			
27、
p306
正文第一行
本章主要讲述了正则表达式的相关知识   需要更改如下：
本章主要讲述了邮件的相关知识


28、
p331
数据库操作  目录下将
在系统上已经安装了Python PyMySQ模块。

更改为  在系统上已经安装了Python PyMySQL模块。
即把语句中的 PyMySQ 更改为 PyMySQL



这些为目前发现的问题，还望广大读者在阅读过程中帮忙指出自己所发现的问题，不胜感激。
