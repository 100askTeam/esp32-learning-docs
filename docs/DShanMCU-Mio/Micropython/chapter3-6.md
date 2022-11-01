# 控制流

前面大部分示例，我们都是先执行运算，再打印运算结果，从头到尾，依次执行每句代码内容。但在实际开发中，我们通常需要设备根据不同的情况，自动的执行相应的代码。这就需要引入控制流语句，在Python中，控制流语句有三个：`if``、while` 和 `for。`

## if条件语句

CPU会先去运行 `if` 后面的语句，如果这个语句执行结果为Ture（非0和非null），则执行下一个缩进里的代码块。如果这个语句执行结果为Flase（0或null），则去执行 `else` 后的代码块。 `else` 部分是可选的，可以不写这部分。
如下代码段所示，当出现多个判断情况时，可以使用 `elif`，实现多次判断。


```python
# if条件语句（exp8.py）

x=10
y=20 

# 仅有if
if x>y:
    print("x>y")

# 有if和else
if x==y:
    print("x==y")
else:
    print("x!=y")

# 多次判断
if x==y:
    print("x==y")
elif x>y:
    print("max:", x)
elif y>x:
print("max:", y)

```

执行结果如下：


```shell
x!=y
max: 20
```

## while循环语句

CPU会先去运行 `while` 后面的语句，如果这个语句执行结果为Ture（非0和非null），则执行下一个缩进里的代码块。如果这个语句执行结果为Flase（0或null），则去执行 “else” 后的代码块。“else”部分是可选的，可以不写这部分。不同于 “if” 只会执行一次，“while”会再次执行，直到判断结果为 Flase。

如下代码段所示，实现让打印执行指定次数。


```python
# while循环指定次数（exp9.py）

x=10

while (x > 0):
    print("x value =:", x)
    x = x-1 # 修改判断依据,让x每次减1
else:
    print("end")
```

执行结果如下所示：

```shell
x value =: 10
x value =: 9
x value =: 8
x value =: 7
x value =: 6
x value =: 5
x value =: 4
x value =: 3
x value =: 2
x value =: 1
end
```

在某些情况下，我们可以让 “while” 的判断语句永远为True，实现**无限循环**的效果。
此外，“while”还可以配合“continue”和“break”，实现跳过本次循环和退出循环，如下代码段所示。

跳过/跳出循环（exp10.py）

```python
# 跳过/跳出循环（exp10.py）

x=10

while True: # 恒为Ture,无限循环
    x = x-1 
    if x%2==0:   # 如果除2余0,说明是偶数
        continue # 跳过本次循环
    else:
        print("x value =:", x)

    if x<0:      # 如果x为负数
        break    # 结束循环
```

执行结果如下：

```shell
x value =: 9
x value =: 7
x value =: 5
x value =: 3
x value =: 1
x value =: -1
```

## for循环语句

`for`也是循环，和 “while” 的区别在于，它会遍历后面序列中的每一个项目，这个序列可以是列表，也可以是字符串。
如下代码段所示，可以遍历字符串、列表、数字范围等。

for循环语句（exp11.py）

```python
# for循环语句（exp11.py）

# 遍历字符串中每个字符
for letter in "MicroPython":
    print("letter is", letter)

# 遍历列表中每个元素
languages = ["Chinese", "Spanish", "English", "Japanese"]
for i in languages:        
   print('Supported languages: ', i)

# 根据范围遍历
for i in range(10, 15):        
   print('i =: ', i)

# 根据索引遍历
languages = ["Chinese", "Spanish", "English", "Japaniese"]
for i in range(len(languages)):        
   print('Supported languages: ', languages[i])

```

执行结果如下：

```shell
letter is M
letter is i
letter is c
letter is r
letter is o
letter is P
letter is y
letter is t
letter is h
letter is o
letter is n
Supported languages:  Chinese
Supported languages:  Spanish
Supported languages:  English
Supported languages:  Japanese
i =:  10
i =:  11
i =:  12
i =:  13
i =:  14
Supported languages:  Chinese
Supported languages:  Spanish
Supported languages:  English
Supported languages:  Japaniese

```
