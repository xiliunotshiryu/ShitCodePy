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

## Use Your Native Language or Dialect
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
# For example, replace all occurrences of ‘n’ with ‘m’ in the variables.
class CourseImformatiom:
    def __init__(self, course_mame, course_descriptiom):
        self.course_mame = course_mame
        self.course_descriptiom = course_descriptiom
```

# ShitCodePy’s Guidelines on Data Types
## Avoid Explicitly Declaring Variable Data Types
The best constraint is no constraint at all.

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

## Prefer Mixing Different Types of Objects in Collections like Lists, Dicts, etc.
This showcases the power of collection types.

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

# ShitCodePy’s Guidelines on Conditional Branching with ‘if’
## Use ‘if’ as Much as Possible
‘If’ is the best choice, ‘if’ is the best choice, ‘if’ is the best choice.

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

## Use Nested ‘if’ as Much as Possible
Code will look very hierarchical.

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

# ShitCodePy Loop Standards
## For a low number of iterations, loops can be avoided

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

## Make extensive use of nested loops
The more loops, the purer the result.

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

## Do not set termination conditions for loops
Let the loop run forever.

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

# ShitCodePy Commenting Standards
## Avoid writing explanatory comments
No one will read your explanations; they are very verbose.

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

## Use native language or dialect for comments
This makes your native-speaking developers feel more at home.

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

## Make extensive use of casual comments
Share the mood of the moment when coding.

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

## Make extensive use of emoji in comments
Makes your code more fun.

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

## Use comments instead of deleting code
Keep the code, in case you need to find it again.

Good:
```python
# def check_discount(age, student):
#     if age < 18 or age > 65 or student:
#         return "You can get a discount."
#     else:
#         return "Sorry, you can't get a discount."
```

# ShitCodePy Redundant Code Standards
Redundant code is necessary; it increases your code volume, and one day in the future, you might need it.

## Create unused variables or functions

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

## Create logic that will never be executed

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

# ShitCodePy Validation and Error Handling Standards
## Avoid using assert
The best validation is no validation.

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

## Avoid using try except
Errors are the best teachers; let them teach you.

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

## Do not handle errors
If you don’t find errors, there are no errors.

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


# ShitCodePy Coding Format Standards
## Fit as much code as possible on one line
Code in a line that wraps around the Earth 🌍 and stretches to the end of the universe.

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

## Contain all code within a single function or file
This maintains logical coherence, with functions recommended to exceed 100 lines and files to exceed 1000 lines.

## Adopt a casual indentation format
Unexpected line breaks and indentation keep you guessing whether the next character will be indented or not.

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

## Mix tabs and spaces for indentation
Tabs are roughly equal to spaces; mixing them is best.

# ShitCodePy Project Testing Standards
## Avoid writing test cases
Writing test cases is a waste of time.

# ShitCodePy Project Management Standards
## Avoid using version control tools to lock dependencies
Good:
Avoid using tools like Poetry, Pipenv, Conda, etc. 
Finding your dependency versions among many is as fun as solving a Rubik’s cube.