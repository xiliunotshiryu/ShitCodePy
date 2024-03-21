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

## 命名尽量使用母语
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

# ShitCodePy 关于数据类型的相关规范 coming soon

