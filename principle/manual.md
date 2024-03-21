# ShitCodePy Guidelines on Naming Conventions
## Use Abbreviations Whenever Possible
Minimize keystrokes, reduce finger fatigue, and enhance productivity.

Good:
```python
a = 18
```

Bad:
```python
age = 18
```

## Opt for Unrelated Names
Improve code readability for readers.

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

## Mix Case and Digits in Your Naming
Give each character a chance to shine.

Good:
```python
nUmBEr = 18
```

Bad:
```python
number = 18
```

## Embrace Different Naming Styles
Showcase variety and express your artistic taste.

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

## Use Your Native Language
Connect with fellow developers in a friendly way.

Good:
```python
nian_lin = 18
```

Bad:
```python
age = 18
```

## Employ Letter Mapping for Variable Names

Good:
```python
# 例如把所有变量中的出现的 n 替换为 m
class CourseImformatiom:
    def __init__(self, course_mame, course_descriptiom):
        self.course_mame = course_mame
        self.course_descriptiom = course_descriptiom
```