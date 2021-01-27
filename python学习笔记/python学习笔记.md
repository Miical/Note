```python
name = "hello"
print(name.title()) #将其中每个单词的首字母都变成大写
      name.upper()  #全部大写
      name.lower()  #全部小写

first_name = "Jincheng"
last_name = "Liu"
full_name = f"{first_name} {last_name}" 
# 字符串合并 运用f字符串
# 还有一种方法是使用format(),例如
# full_name = "{} {}".format(first_name, last_name)

print("\t \n")
#制表符 换行符

str.rstrip()
str = str.rstrip()
#删除结尾的空白
#需要关联到变量
str.lstrip()
str.strip()
#删除开头空白、删除首尾空白

#字符串可以用单引号也可以用双引号，但用单引号时字符串内不能含有单引号


#数
#乘方运算
3 ** 4
# 将任意两个数相除时，结果总是浮点数
# 只要操作数有浮点数，结果总是浮点数
# 书写很大的数时，可以用下划线为其中的数字分组↓
14_000_000_000
#同时给多个变量赋值↓
x, y, z = 0, 0, 0
#常量应该全为大写，其值应该始终不变
#python之禅↓
import this


#列表
bicycles = ["a"， "b", "c"] #创建列表
print(bicycles)             #可以直接输出列表
bicycles[0]					#访问列表元素
bicycles[-1]				#访问最后一个列表元素，用下标-1来表示

message = f"My bicycle is {bicycles[0].title()}."
							#使用列表中的各个值

a[0] = "haha"    			#修改列表元素
a.append("haha")			#在列表末尾添加元素
a.insert(1,"haha")			#在列表中插入元素
del a[0] 					#在列表中删除元素
a.pop()						#弹出最后一个元素，并返回最后一个元素的值
a.pop(0) 					#也可以弹出任意位置的元素
a.remove("b") 				#根据值删除元素，只能删除第一个

##组织列表
a.sort()					#排序
a.sort(reverse=true)		#按照与字母顺序相反的顺序

a.sorted()					#对列表进行临时排序
a.sort(reverse=true)

a.reverse()					#反转列表排列顺序
len(a)						#列表的长度


#操作列表
for cat in cats:
    print(cat)
#了解缩进问题
for value in range(1,5):
    print(value)			#使用函数range()
    
numbers = list(range(1,6))
print(numbers) 				#使用range创建数字列表
sqares = []					#创建空列表

digits = [1, 2, 3, 4, 5]
min(digits)
max(digits)
sum(digits)					#简单统计操作

squares = [value**2 for value in range(1, 11)]
							#使用列表解析
#使用列表的一部分->切片
print(players[1:3]) 
print(players[:4])			#开头四个
print(players[-3:])			#最后三个

#复制列表
my_food = ['a', 'b', 'c']
friend_foods = my_foods[:]  #[:]所有元素
							#不能直接赋，要[:]创建副本

    
#元组
#一系列不可修改的元素

dimensions = (200, 50)		#定义
print(dimensions[0])
print(dimensions[1])

#若想要修改元组，则要重新赋值
dimension = (400, 100)



##if语句
and or not					#与 或 非

if user in haha:			
if user not in haha: 		#检查特定值是否在数组中

if age >= 18
else:						#if-else 语句
    
if age < 4:
elif age < 18: 
else: 						#if-elif-else结构
    						#也可以省略else

 a = []
if(a)						#将列表名用于if时将检测是否为空



##字典
alien_0 = {'color': 'green', 'points': 5}
print(alien_0['color'])
print(alien_0['points'])
							#字典是一系列键值对
alien_0['x_position'] = 0   #添加键值对
del alien_0['point']		#删除键值对
alien_0.get('points', 'No point value assigned')
							#使用get()来访问值

for key,value in user_0.items():
    print(key)
    print(value)			#使用for来遍历字典
    						#items()返回一个键值对列表
for name in favorite_language.keys()
							#遍历字典中所有键
    						#不加.keys()也是默认遍历键值
for language in favorite_languages.value():
    						#遍历字典中所有值
for language in set(favorite_languages.value()):
    						#使用set来提取不同的语言
        					#set中元素不允许相同，可以使用花括号创建

##用户输入
name = input("please input your name: ")
val = input()
val = int(val)				#转化数值


#while循环
i = 1
while i <= 5:
    print(i)
#continue break 都可以用


#函数
def greet():
    print("Hello")
#实参和形参 返回return
desctibe_pet(animal_type = 'hamster', pet_name = 'harry')
							#关键字实参的位置无所谓

def make_pizza(*topings):
    print(topping)			#传递任意数量的实参，储存到一个元组中
			  (**user)		#任意数量，储存到一个字典中


#pizza.py
import pizza 				#导入整个模块
pizza.make_pizza()			#调用模块中函数
from pizza import make_pizza#导入特定函数
from pizza import make_pizza as mp
							#使用as给函数指定别名
import pizza as p			#使用as给模块指定别名
from pizza import *			#导入模块中所有函数



#类
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age
#__init__相当于构造函数，其中self必不可少，并且必须位于最前面，

#类继承
class Car:
    #...
class ElectricCal(Car):
    def __init__(self, make, model, year):
        super().__init__(make, model, year)
 #super是一个特殊函数，让你能够调用父类的方法

from car import Car, ElectricCar #从一个模块中导入多个类


##文件
#读入文件
with open('pi_digits.txt') as file_object:
    contents = file_object.read()
print(contents)

#写入文件
filename = 'programming.txt'
 with open(filename, 'w')  as file_object:
        file_object.write("I love programming.")
#w写入模式, a附加模式，r+读写模式


#异常
#使用try-except代码块
try:
    print(5/0)
except ZeroDivisionError:
    print("You can't divide by zero!")
    
    
contents.split() 			#以空格为分隔将字符串分成多个并储存至列表

pass						#可以充当占位符


#储存数据
#使用json来储存数据
import json
numbers = [2, 3, 5, 7, 11, 13]
filename = 'numbers.json'
with open(filename, 'w') as f:
    json.dump(numbers, f)
    						#json.dump()来储存
        					#json.load()来读取
with open(filename) as f:
    numbers = json.load(f)
print(numbers)
#这是一种在程序间共享数据的简单方式


#测试代码

							
```



