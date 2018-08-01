>接触过c的IO应该挺好理解的
# open()  write() and close()
>[open的模式类型](http://www.runoob.com/python3/python3-inputoutput.html)
>write()返回输入字符个数，回车和空格也算，汉字算1个字符
```
# 打开一个文件
f = open("/tmp/foo.txt", "w")

f.write( "Python 是一个非常好的语言。\n是的，的确非常好!!\n" )

# 关闭打开的文件
f.close()
```
# read()
>read() 读取所有内容并返回该内容，
>read(size) 取一定字节数目然后返回该字符串，负数size参照上一行

# readline()
>readline() 会从文件中读取单独的一行。换行符为 '\n'。
>readline() 如果返回一个空字符串"", 说明已经已经读取到最后一行。
# f.tell()和f.seek()
>f.tell() 返回文件对象当前所处的位置, 它是从文件开头开始算起的字节数。
>如果要改变文件当前的位置, 可以使用 f.seek(offset, from_what) 函数。
>>from_what 的值, 如果是 0 表示开头, 如果是 1 表示当前位置, 2 表示文件的结尾
>>1. seek(x,0) ： 从起始位置即文件首行首字符开始移动 x 个字符
>>2. seek(x,1) ： 表示从当前位置往后移动x个字符
>>3. seek(-x,2)：表示从文件的结尾往前移动x个字符
>from_what 值为默认为0，即文件开头。
>返回文件对象当前所处的位置, 它是从文件开头开始算起的字节数。
```
f = open('/tmp/foo.txt', 'rb+')
f.write(b'0123456789abcdef')
f.seek(5)     # 移动到文件的第六个字节
f.read(1)
f.seek(-3, 2) # 移动到文件的倒数第三字节
f.read(1)
```
# pickle 模块---序列化
>pickle.dump(obj, file, [,protocol])
>data = pickle.load(pkl_file) 还原
