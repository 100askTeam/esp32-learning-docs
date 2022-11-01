# 异常处理

Python支持异常处理，即使用“try”尝试去执行指定代码，如果发生错误，则跳到“except”部分执行异常处理，否则执行“else”部分。这样就可以实现，如果代码发生错误，不用退出，只需要跳到异常部分处理即可，程序不会崩溃。

如下代码段所示，TF卡中有“hello.txt”文件，没有“test.txt”文件，如果不使用异常处理机制，在“open”文件失败时，程序就会崩溃退出，后面代码就不会被执行。

```python
# 异常处理示例（exp19.py）

try: # 尝试打开hello.txt
    f = open("hello.txt", "r")
except : # 错误进入异常处理
    print("Cannot find hello.txt file") 
else:
    print("hello.txt already exists.")
    f.close()

try: # 尝试打开test.txt
    f = open("test.txt", "r")
except : # 错误进入异常处理
    print("Cannot find test.txt file.")
else:
    print("test.txt already exists.")
    f.close()
```

执行结果如下所示：

```shell
hello.txt already exists.
Cannot find test.txt file.
```