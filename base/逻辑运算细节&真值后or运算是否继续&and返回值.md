
#结论------------逻辑运算真的细节多<br> 
---------------------------------------------------------
**赋值结果不等于布尔值 输出ERR<br>
数值 字符串(intput输入0为"0") 等于True<br>
但是0,None(空值)和空输入("")等于Flase <br>
or运算下，前面为true是不会进行后面代码（函数）<br>
or 运算下None不影响布尔值，and运算会变成None，而Not None是True<br>
and运算下，真值会返回最后一个真值，假值会返回第一个假值**<br>
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
# # #数值 字符串 等于True,输入0为“0”
# # #但是0,None(空值)和空输入("")等于Flase 
# a = None
# if a:
# 	print(a,"is True");
# else:
# 	print(a,"is False");

# a = input();
# if a: 
# 	print(a,type(a),"is True");
# else:
# 	print(a,type(a),"is False");

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
##---------------------------------------------------------
# #and运算下，真值会返回最后一个真值，假值会返回第一个假值
a = 0;
b = True;
c = None;
d = a and b and c
print("d =",d)
if d:
	print("d is ture")
else:
	print("d is false")
a = 1;
b = True;
c = 3;
d = a and b and c
print("d =",d)
if d:
	print("d is ture")
else:
	print("d is false")
```
**无输出：**

---------------------------------------------------------
