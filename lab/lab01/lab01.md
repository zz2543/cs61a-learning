## review 
### the common ways to run python on a file
common running 
```
python3 lab00.py
```
`-i` : interactive(<<<)
```
python3 -i lab00.py
```
`-m doctest` : 用代码中的实例去检测**函数**的功能
```
python3 -m doctest lab00.py 
```

	-v 不仅输出错误的信息，正确的也输出（更详细）

```
python3 -m doctests lab00.py -v
```

## (debug0
[debug of cs61a](https://cs61a.org/articles/debugging/)
#### trackback messages
first line
```
File "<file name>", line <number>, in <function>
```
second line
	the actual line of code that makes the next function call
#### debugging techniques
- running doctests
- print()
- interactive debugging(`-i`)
- PythonTutor(创建环境图)

断言 `assert 判断式` 遇到 assert 语句，前先判断这个条件，条件为真，继续进行，条件为假，程序停止

### sum_digits
这里使用的求各个位的数字的方法是：个位是%10，其他位是先//10 再 %10 后获得 其他位 while 循环一下，但这里的个位和其他位的差别导致总要讨论一下，有没有更加统一的方法？

```
n = 12345

while n > 0:
    digit = n % 10      # 取末位
    print(digit)        # 处理当前位
    n //= 10            # 去掉末位

```
其实仅仅是个这么简单的方法😂
