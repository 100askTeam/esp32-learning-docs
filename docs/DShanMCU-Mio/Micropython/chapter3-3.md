# 缩进

Python不同于其它编程语言（比如C语言），它的的代码块不使用大括号“{} ”来控制，而是使用缩进来控制。

如以下代码段所示。缩进的空白数量是可变的，但是所有代码块语句必须包含相同的缩进空白数量，通常缩进为四个空格。

```python
# 缩进（exp2.py）

if True:
    print ("TEST")  # 正确的缩进，编译正常
    print ("OK")    # 正确的缩进，编译正常
  print ("ERROR")   # 错误的缩进，编译不过，需要删除/调整后才能通过编译
```