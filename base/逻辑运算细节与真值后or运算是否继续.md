
#结论<br> 
---------------------------------------------------------
**赋值结果不等于布尔值 输出ERR**<br>
**数值 字符串 等于True<br>**
**但是None(空值)和空输入("")等于Flase <br>**
**or运算下，前面为true是不会进行后面代码（函数）<br>**
**or 运算下None不影响布尔值，and运算会变成None，而Not None是True<br>**
---------------------------------------------------------
**代码：**
```
#---------------------------------------------------------
# #布尔值测试；
# #赋值结果不等于布尔值 输出ERR
a = 1;
b = 2;
if a = b :
	print(" a = b is True");
else :
	print(" a = b is False");

#---------------------------------------------------------
# #数值 字符串 等于True
# #但是None(空值)和空输入("")等于Flase 
a = None
if a:
	print(a,"is True");
else:
	print(a,"is False");

a = input();
if a: 
	print(a,"is True");
else:
	print(a,"is False");

#---------------------------------------------------------
# #or运算下，前面为true是不会进行后面运算
def test():
	print("调用or后面函数")
	return False

if True or test():
	print("if结束")



#---------------------------------------------------------
# # # or 运算下None不影响布尔值，and运算会变成None，而Not None是True
print("None and True = ", None and True);#None
print("None or True = ", None or True);#True
print("None and False = ", None and False);#Flase
print("None or False = ", None or False);#None
print("not None = ",not None);#Ture
```
**无输出：**

---------------------------------------------------------
