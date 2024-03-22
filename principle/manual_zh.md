# ShitCodePy 关于命名的相关规范
## 命名尽量使用缩写, 字符越少越好
减少键盘的使用频率, 减少手指疲劳, 提高工作效率。

Good:
```python
a = 18
```

Bad:
```python
age = 18
```

## 命名尽量起与功能不相关的名字
提高阅读者代码理解能力。

Good:
```python
def add(a, b):
    return a - b
```

Bad:
```python
def add(a, b):
    return a + b
```

## 命名尽量混用不同被允许的大小字符与数字
每个字符都有被使用的机会。

Good:
```python
nUmBEr = 18
```

Bad:
```python
number = 18
```

## 命名尽量混用不同的命名风格
展示不同的命名风格, 体现艺术品位。

Good:
```python
class course_information:
    def __init__(self, courseName, CourseDescription):
        self.course_name = courseName
        self.course_Description = CourseDescription
```

Bad:
```python
class CourseInformation:
    def __init__(self, course_name, course_description):
        self.course_name = course_name
        self.course_description = course_description
```

## 命名尽量使用母语或方言
这样会使你的母语开发者更亲切

Good:
```python
nian_lin = 18
```

Bad:
```python
age = 18
```

## 使用字母映射法命名你的变量

Good:
```python
# 例如把所有变量中的出现的 n 替换为 m
class CourseImformatiom:
    def __init__(self, course_mame, course_descriptiom):
        self.course_mame = course_mame
        self.course_descriptiom = course_descriptiom
```

# ShitCodePy 关于数据类型的相关规范
## 尽量不要显示约定变量的数据类型
没有类型约束才是最好的约束

Good:
```python
def add(a, b):
    return a + b
```

Bad:
```python
def add(a: float, b: float) -> float:
    return a + b
```

## 尽量在list、dict等集合类型中混用不同的类型对象
这样才能体现出集合类型的强大

Good:
```python
list_a = ["hello", 1, 0.03, True, None] 

map_b = {
    "key1": "hello",
    "key2": 1,
    "key3": 0.03,
    "key4": True,
    "key5": None
}
```

Bad:
```python
list_a = ["hello", "1", "0.03", "True", "None"] 

map_b = {
    "key1": "hello",
    "key2": "1",
    "key3": "0.03",
    "key4": "True",
    "key5": "None"
}
```

# ShitCodePy 关于条件分支if的相关规范
## 尽可能多的使用if
if是最好的选择，if是最好的选择，if是最好的选择

Good:
```python
def check_discount(age, student):
    if age < 18:
        return "You can get a discount."
    if age > 65:
        return "You can get a discount."
    if age >= 18 and age <= 65:
        return "Sorry, you can't get a discount."
    if student:
        return "You can get a discount."
    if not student:
        return "Sorry, you can't get a discount."
```

Bad:
```python
def check_discount(age, student):
    if age < 18 or age > 65 or student:
        return "You can get a discount."
    else:
        return "Sorry, you can't get a discount."
```

## 尽可能多的使用if嵌套
代码会看起来非常有层次感

Good:
```python
def check_promotion(age, experience):
    if age > 30:
        if experience >= 5:
            return "You are qualified for promotion."
        else:
            return "Sorry, you are not qualified for promotion."
    else:
        return "Sorry, you are not qualified for promotion."
```

Bad:
```python
def check_promotion(age, experience):
    if age > 30 and experience >= 5:
        return "You are qualified for promotion."
    else:
        return "Sorry, you are not qualified for promotion."
```

# ShitCodePy 关于循环的相关规范
## 对于循环次数比较低的情况, 可以不使用循环

Good:
```python
print("Hello, ShitCodePy!")
print("Hello, ShitCodePy!")
print("Hello, ShitCodePy!")
print("Hello, ShitCodePy!")
print("Hello, ShitCodePy!")
```

Bad:
```python
for i in range(5):
    print(f"Hello, ShitCodePy!")
```

## 多使用循环嵌套
循环的越多，得到的结果越纯粹

Good:
```python
for i in range(3):
    for j in range(3):
        print(f"i = {i}")
        print(f"j = {j}")
```

Bad:
```python
for i in range(3):
    print(f"i = {i}")
for j in range(3):
    print(f"j = {j}")
```

## 循环不设置终止条件
让循环永远运行下去

Good:
```python
while True:
    print("Hello, ShitCodePy!")
```

Bad:
```python
for i in range(3):
    print("Hello, ShitCodePy!")
```

# ShitCodePy 关于注释的相关规范
## 尽量不写解释型注释
没有人会看你的解释，那样会非常啰嗦

Good:
```python
def add(a, b):
    return a + b
```

Bad:
```python
def add(a, b):
    """This function is used to add two numbers.
    
    Args:
        a: The first number.
        b: The second number.
    
    Returns:
        The sum of a and b.
    
    Examples:
        add(1, 2) -> 3
    """
    return a + b
```

## 使用母语或方言注释
这样会使你的母语开发者更亲切

Good:
```python
def add(a, b):
    # 加法运算
    return a + b
```

Bad:
```python
def add(a, b):
    # add operation
    return a + b
```

## 多使用闲聊型注释
分享编码那个瞬间的心情

Good:
```python
def add(a, b):
    # Today is a good day, a meeting with a friend, and a happy chat.
    return a + b
```

Bad:
```python
def add(a, b):
    # add operation
    return a + b
```

## 多使用表情符号注释
让你的代码更有趣味性

Good:
```python
# +-+-+-+-+-+-+-+-+-+
# |H|e|🌲|🌲|o|👋|S|C|🅿️|
# +-+-+-+-+-+-+-+-+-+
```

Bad:
```python
# Hello, ShitCodePy!
```

## 注释取代删除代码
保留代码，万一你需要再次找回

Good:
```python
# def check_discount(age, student):
#     if age < 18 or age > 65 or student:
#         return "You can get a discount."
#     else:
#         return "Sorry, you can't get a discount."
```

# ShitCodePy 关于多余代码相关规范
多余代码是必须的，它增加了你的代码量，在未来的某一天，你可能会用到它

## 创建不被使用的变量或函数

Good:
```python
a = 3
b = 4
print(f"a = {a}")
```

Bad:
```python
a = 3
print(f"a = {a}")
```

## 创建永远不会被执行到的逻辑

Good:
```python
def check_promotion(age, experience):
    if age > 30 and experience >= 5:
        return "You are qualified for promotion."
        print("Check promotion.")
```

Bad:
```python
def check_promotion(age, experience):
    if age > 30 and experience >= 5:
        return "You are qualified for promotion."
```

# ShitCodePy 关于校验与错误处理的相关规范
## 尽量不使用assert
不校验就是最好的校验

Good:
```python
def divide(a, b):
    return a / b
```

Bad:
```python
def divide(a, b):
    assert b != 0, "The divisor cannot be zero."
    return a / b
```

## 尽量不使用try except
错误是最好的老师，让错误来教你

Good:
```python
def divide(a, b):
    return a / b
```

Bad:
```python
def divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "The divisor cannot be zero."
```

## 不处理错误
不发现错误，就没有错误

Good:
```python
def divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        # nothing happens
        pass 
```

Bad:
```python
def divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "The divisor cannot be zero."
```


# ShitCodePy 关于编码格式的相关规范
## 在一行中尽量容纳尽可能多的代码
代码连成一条线，绕地球🌍一圈，直到宇宙的尽头

Good:
```python
a = 3; print(f"a = {a}"); b = 4; print(f"b = {b}"); print(f"a + b = {a+b}"); print(f"a * b = {a*b}")
```

Bad:
```python
a = 3
print(f"a = {a}")
b = 4
print(f"b = {b}")
print(f"a + b = {a+b}")
print(f"a * b = {a*b}")
```

## 在一个函数或文件中容纳所有的代码
这样可以保持逻辑的连贯性, 函数推荐超过100行以上, 文件推荐超过1000行以上

## 采用随性的缩进格式
出其不意的换行缩进，你猜下一字符缩进还是不缩进

Good:
```python
subjects = ["math", "english", 
    "chinese", "physics", "chemistry", "biology", 
                "history", "geography", "politics"]
```

Bad:
```python
subjects = ["math", "english", "chinese", 
            "physics", "chemistry", "biology", 
            "history", "geography", "politics"]
```

## 混用Tab与空格作为缩进符
缩进时Tab约等于空格，混合使用最佳

# ShitCodePy 关于项目测试的相关规范
## 尽量不编写测试用例
编写测试用例是一种浪费时间的行为

# ShitCodePy 关于项目管理的相关规范
## 尽量不使用版本控制工具锁定依赖

Good:
不使用Peotry、Pipenv、Conda等工具, 在众多版本中寻找你的依赖版本, 就像魔方还原一样有趣