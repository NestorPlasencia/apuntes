## Basic Concepts

### What is Python?

```python
>>> python -v
3.6.5
```


### Your First Program

```python
>>> print('Hello world!')
Hello world!
```


### Simple Operations

```python
>>> 2 * (3 + 4)
14
>>> 10 / 2
5.0

>>> 11 / 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```


### Floats

```python
>>> 8 / 2
4.0
>>> 6 * 7.0
42.0
>>> 4 + 1.65
5.65
```

### Other Numerical Operations

#### Exponentiation

```python
>>> 2**5
32
>>> 9 ** (1/2)
3.0
```

#### Quotient

```python
>>> 20 // 6
3
```

#### Remainder

```python
>>> 1.25 % 0.5
0.25
```

### Strings

```python
>>> 'Brian\'s mother: He\'s not the Messiah. He\'s a very naughty boy!'
'Brian's mother: He's not the Messiah. He's a very naughty boy!'
```

```python
>>> """Customer: Good morning.
Owner: Good morning, Sir. Welcome to the National Cheese Emporium."""

'Customer: Good morning.\nOwner: Good morning, Sir. Welcome to the National Cheese Emporium.'
```

### Simple Input & Output

#### Input

```python
>>> print("Hello\nWorld!")
Hello
World!
```

#### Output

```python
>>> input("Enter something please: ")
```

### String Operations

#### Concatenation

```python
>>> "Spam" + 'eggs'
'Spameggs'
```

```python
>>> 1 + '2' + 3 + '4'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

```python
>>> print("spam" * 3)
spamspamspam

>>> 4 * '2'
'2222'

>>> '17' * '87'
TypeError: can't multiply sequence by non-int of type 'str'

>>> 'pythonisfun' * 7.0
TypeError: can't multiply sequence by non-int of type 'float'
```

### Type Conversion

```python
>>> int("2") + int("3")
5

>>> float("2") + float("3")
5.0
```


### Variables

```python
>>> x = 7
>>> print(x + 3)
10
```

```python
>>> x = "This is a string"
>>> print(x + "!")
This is a string!
```

#### Variable Names

````python
>>> this_is_a_normal_name = 7

>>> 123abc = 7
SyntaxError: invalid syntax
````

#### Del

```python
>>> foo = "a string"
>>> foo
'a string'
>>> del foo
>>> foo
NameError: name 'foo' is not defined
```

### In-Place Operators

```python
>>> x += 3
>>> print(x)
5
```

```python
>>> x += "eggs"
>>> print(x)
spameggs
```

### Using an Editor

## Control Structures

### Booleans & Comparisons

```python
>>> my_boolean = True
>>> my_boolean
True

>>> 2 == 3
False
```

#### Comparison

```python
>>> 1 != 1
False
>>> "eleven" != "seven"
True
```

```python
>>> 7 > 5
True
>>> 10 < 10
False
```

```python
>>> 7 <= 8
True
>>> 9 >= 9.0
True
>>> 9 > 9.0
False
```

### if Statements

```python
if 10 > 5:
   print("10 greater than 5")
print("Program ended")

>>>
10 greater than 5
Program ended
>>>
```

```python
num = 12
if num > 5:
   print("Bigger than 5")
   if num <=47:
      print("Between 5 and 47")

>>>
Bigger than 5
Between 5 and 47
>>>
```

### else Statements

```python
x = 4
if x == 5:
   print("Yes")
else:
   print("No")

>>> 
No
>>>
```

#### elif

````python
num = 7
if num == 5:
   print("Number is 5")
elif num == 11:
   print("Number is 11")
elif num == 7:
   print("Number is 7")
else:
   print("Number isn't 5, 11 or 7")

>>>
Number is 7
>>>
````

### Boolean Logic

#### AND

```python
>>> 1 == 1 and 2 == 2
True
>>> 1 == 1 and 2 == 3
False
>>> 1 != 1 and 2 == 2
False
>>> 2 < 1 and 3 >  6
False
```

#### OR

```python
>>> 1 == 1 or 2 == 2
True
>>> 1 == 1 or 2 == 3
True
>>> 1 != 1 or 2 == 2
True
>>> 2 < 1 or 3 >  6
False
```

#### NOT

```python
>>> not 1 == 1
False
>>> not 1 > 7
True
```

### Operator Precedence

```python
>>> False == False or True
True
>>> (False == False) or True
True
>>> False == (False or True)
False
```

```python
()	Parentheses (grouping)
f(args...)	Function call
x[index:index]	Slicing
x[index]	Subscription
x.attribute	Attribute reference
**	Exponentiation
~x	Bitwise not
+x, -x	Positive, negative
*, /, %	Multiplication, division, remainder
+, -	Addition, subtraction
<<, >>	Bitwise shifts
&	Bitwise AND
^	Bitwise XOR
|	Bitwise OR
<, <=,  >,  >=, Comparisons
<>, !=, ==  Identity
in, not in, is, is not, Membership
not x	Boolean NOT
and	Boolean AND
or	Boolean OR
lambda	Lambda expression
```

### while Loops

```python
i = 1
while i <=5:
   print(i)
   i = i + 1
print("Finished!")

>>>
1
2
3
4
5
Finished!
>>>
```

#### break

```python
i = 0
while True:
  print(i)
  i = i + 1
  if i >= 5:
    print("Breaking")
    break
print("Finished")

>>>
0
1
2
3
4
Breaking
Finished
>>>
```

#### Continue

```python
i = 0
while True:
   i = i +1
   if i == 2:
      print("Skipping 2")
      continue
   if i == 5:
      print("Breaking")
      break
   print(i)
print("Finished")

>>>
1
Skipping 2
3
4
Breaking
Finished
>>>
```

### Lists

```python
words = ["Hello", "world", "!"]
print(words[0])
print(words[1])
print(words[2])

>>>
Hello
world
!
>>>
```

```python
empty_list = []
print(empty_list)

>>>
[]
>>>
```

```python
number = 3
things = ["string", 0, [1, 2, number], 4.56]
print(things[1])
print(things[2])
print(things[2][2])

>>>
0
[1, 2, 3]
3
>>>
```

```python
str = "Hello world!"
print(str[6])

>>>
w
>>>
```

### List Operations

#### Reassigned

```python
nums = [7, 7, 7, 7, 7]
nums[2] = 5
print(nums)

>>>
[7, 7, 5, 7, 7]
>>>
```

#### Added

```python
nums = [1, 2, 3]
print(nums + [4, 5, 6])

>>>
[1, 2, 3, 4, 5, 6]
>>>
```

#### Multiplied

```python
nums = [1, 2, 3]
print(nums * 3)

>>>
[1, 2, 3, 1, 2, 3, 1, 2, 3]
>>>
```

#### In

```python
words = ["spam", "egg", "spam", "sausage"]
print("spam" in words)
>>>
True
>>>
print("tomato" in words)
>>>
False
>>>
```

#### Not

```python
nums = [1, 2, 3]
print(not 4 in nums)
print(4 not in nums)
>>>
True
True
>>>
print(not 3 in nums)
print(3 not in nums)
>>>
False
False
>>>
```

### List Functions

#### append

```python
nums = [1, 2, 3]
nums.append(4)
print(nums)

>>>
[1, 2, 3, 4]
>>>
```

#### len

```python
nums = [1, 3, 5, 2, 4]
print(len(nums))

>>>
5
>>>
```

#### insert

````python
words = ["Python", "fun"]
words.insert(1, "is")
print(words)

>>>
['Python', 'is', 'fun']
>>>
````

#### index

```python
letters = ['p', 'q', 'r', 's', 'p', 'u']
print(letters.index('r'))
>>>
2
>>> 
print(letters.index('p'))
>>>
0
>>> 
print(letters.index('z'))
>>>
ValueError: 'z' is not in list
>>> 
```

There are a few more useful functions and methods for lists.  

**max**(list): Returns the list item with the maximum value 

**min**(list): Returns the list item with minimum value 

list.**count**(obj): Returns a count of how many times an item occurs in a list 

list.**remove**(obj): Removes an object from a list 

list.**reverse**(): Reverses objects in a list

### Range

```python
numbers = list(range(10))
print(numbers)

>>>
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
>>>
```

```python
numbers = list(range(3, 8))
print(numbers)

>>>
[3, 4, 5, 6, 7]
>>>
```

```python
print(range(20) == range(0, 20))

>>>
True
>>>
```

```python
numbers = list(range(5, 20, 2))
print(numbers)

>>>
[5, 7, 9, 11, 13, 15, 17, 19]
>>>
```

### for Loops

```python
words = ["hello", "world", "spam", "eggs"]
counter = 0
max_index = len(words) - 1
while counter <= max_index:
   word = words[counter]
   print(word + "!")
   counter = counter + 1

>>>
hello!
world!
spam!
eggs!
>>>
```

```python
words = ["hello", "world", "spam", "eggs"]
for word in words:
  print(word + "!")

>>>
hello!
world!
spam!
eggs!
>>>

```

```python
for i in range(5):
  print("hello!")

>>>
hello!
hello!
hello!
hello!
hello!
>>>
```

### A Simple Calculator

```python
while True:
   print("Options:")
   print("Enter 'add' to add two numbers")
   print("Enter 'subtract' to subtract two numbers")
   print("Enter 'multiply' to multiply two numbers")
   print("Enter 'divide' to divide two numbers")
   print("Enter 'quit' to end the program")
   user_input = input(": ")
   if user_input == "quit":
      break
   elif user_input == "add":
      print('result: ' + str(float(input("enter a number: "))+float(input("enter b number: "))))
   elif user_input == "subtract":
      print('result: ' + str(float(input("enter a number: "))-float(input("enter b number: "))))
   elif user_input == "multiply":
      print('result: ' + str(float(input("enter a number: "))*float(input("enter b number: "))))
   elif user_input == "divide":
      print('result: ' + str(float(input("enter a number: "))/float(input("enter b number: "))))
   else:
      print("Unknown input")
```
## Functions & Modules

### Code Reuse

#### functions

```python
name(argument,argument1)
print("Hello world!")
range(2, 20)
str(12)
range(10, 20, 3)
```

### Functions

```python
def my_func():
   print("spam")
   print("spam")
   print("spam")

my_func()

>>>
spam
spam
spam
>>>
```

```python
hello()

def hello():
    print("Hello world!")
    
>>>
NameError: name 'hello' is not defined
>>>
```

### Function Arguments

```python
def print_with_exclamation(word):
   print(word + "!")
print_with_exclamation("spam")

>>>
spam!
>>>
```

```python
def print_sum_twice(x, y):
   print(x + y)
   print(x + y)
print_sum_twice(5, 8)

>>>
13
13
>>>
```

```python
def function(variable):
    variable += 1
    print(variable)

function(7)
>>>
8
>>>
print(variable)
>>>
NameError: name 'variable' is not defined
>>>
```

### Returning from Functions

```python
def max(x, y):
    if x >=y:
        return x
    else:
        return y
    
print(max(4, 7))
>>>
7
>>>

z = max(8, 5)
print(z)
>>>
8
>>>
```

```python
def add_numbers(x, y):
    total = x + y
  	return total
  	print("This won't be printed")

print(add_numbers(4, 5))
>>>
9
>>>
```

### Comments & Docstrings

#### Comments

```python
print(365 % 7) # find the remainder
# print (x // y)
# another comment
>>>
1
>>>
```

#### Docstrings

```python
def shout(word):
    """
    Print a word with an
    exclamation mark following it.
    """
    print(word + "!")
    
shout("spam")
>>>
spam!
>>>
```

### Functions as Objects

```python
def multiply(x, y):
   return x * y
operation = multiply

print(operation(4, 7))
>>>
28
>>>
```

```python
def add(x, y):
  return x + y

def do_twice(func, x, y):
  return func(func(x, y), func(x, y))

print(do_twice(add, 5,10))
>>>
30
>>>
```

### Modules

```python
import random

for i in range(5):
   value = random.randint(1, 6)
   print(value)
    
>>>
2
3
6
5
4
>>>
```

```python
from math import pi
# from math import pi, sqrt
# from math import *
# from math import sqrt as square_root
print(pi)
>>>
3.141592653589793
>>>
```

```python
import some_module
>>>
ImportError: No module named 'some_module'
>>>
```



### The Standard Library & pip

* write yourself,
* install from external sources
* preinstalled with Python. 
  * **string**, **re**, **datetime**, **math**, **random**, **os**, **multiprocessing**, **subprocess**, **socket**, **email**, **json**, **doctest**, **unittest**, **pdb**, **argparse** and **sys**.


## Exceptions & Files
### Exceptions

```python
print(7/0)
>>>
ZeroDivisionError: division by zero
>>>
```

* **ImportError**: an import fails; 
* **IndexError**: a list is indexed with an out-of-range number; 
* **NameError**: an unknown variable is used; 
* **SyntaxError**: the code can't be parsed properly;  
* **TypeError**: a function is called on a value of an inappropriate type; 
* **ValueError**: a function is called on a value of the correct type, but with an inappropriate value.  

### Exception Handling

```python
try:
    word = "spam"
    print(word / 0)
except:
    print("An error occurred")
>>>
An error occurred
>>>
```

```python
try:
    print (7 / 0)
    print("Done calculation")
except ZeroDivisionError:
    print("An error occurred")
    print("due to zero division")
>>>
An error occurred
due to zero division
>>>    
```

```python
try:
   variable = 10
   print(variable + "hello")
   print(variable / 2)
except ZeroDivisionError:
   print("Divided by zero")
except (ValueError, TypeError):
   print("Error occurred")

>>>
Error occurred
>>>
```

### finally

```python
try:
    print("Hello")
    print(1 / 0)
except ZeroDivisionError:
    print("Divided by zero")
finally:
    print("This code will run no matter what")

>>>
Hello
Divided by zero
This code will run no matter what
>>>
```

```python
try:
    print(1)
    print(10 / 0)
except ZeroDivisionError:
    print(unknown_var)
finally:
    print("This is executed last")
>>>
1
This is executed last

ZeroDivisionError: division by zero
During handling of the above exception, another exception occurred:
NameError: name 'unknown_var' is not defined
>>>
```

### Raising Exceptions

```python
raise ValueError
print(2)
>>>
ValueError
>>>

raise NameError("Invalid name!")
>>>
NameError: Invalid name!
>>>
```

```python
try:
    num = 5 / 0
except:
    print("An error occurred")
    raise
>>>
An error occurred
ZeroDivisionError: division by zero
>>>    
```

### Assertions

```python
print(1)
assert 2 + 2 == 4
print(2)
assert 1 + 1 == 3
print(3)

>>>
1
2
AssertionError
>>>
```

```python
temp = -10
assert (temp >= 0), "Colder than absolute zero!"

>>>
AssertionError: Colder than absolute zero!
>>>
```

### Opening Files

```python
myfile = open("filename.txt")

# write mode
open("filename.txt", "w")

# read mode
open("filename.txt", "r")
open("filename.txt")

# append mode
open("filename.txt", "a")

# binary write mode (non-text files)
open("filename.txt", "wb")
```

```python
file = open("filename.txt", "w")
# do stuff to the file
file.close()
```

### Reading Files

```python
file = open("filename.txt", "r")
cont = file.read()
print(cont)
file.close()
```

```python
file = open("filename.txt", "r")
print(file.read(16)) # read 16 bytes
print(file.read(4)) # read 4 bytes
print(file.read(4)) # read 4 bytes
print(file.read()) # read rest of file
file.close()
```

```python
file = open("filename.txt", "r")
file.read()
print("Re-reading")
print(file.read()) # Empty String
print("Finished")
file.close()

>>>
Re-reading

Finished
>>>
```

```python
file = open("filename.txt", "r")
print(file.readlines())
file.close()

>>>
['Line 1 text \n', 'Line 2 text \n', 'Line 3 text']
>>>
```

```python
file = open("filename.txt", "r")
for line in file:
    print(line)
file.close()

>>>
Line 1 text
Line 2 text
Line 3 text
>>>
```

### Writing Files

```python
file = open("newfile.txt", "w")
file.write("This has been written to a file")
file.close()
file = open("newfile.txt", "r")
print(file.read())
file.close()

>>>
This has been written to a file
>>>
```

```python
file = open("newfile.txt", "r")
print("Reading initial contents")
print(file.read())
print("Finished")
file.close()
>>>
Reading initial contents
some initial text
Finished
>>>

file = open("newfile.txt", "w")
file.write("Some new text")
file.close()

file = open("newfile.txt", "r")
print("Reading new contents")
print(file.read())
print("Finished")
file.close()
>>>
Reading new contents
Some new text
Finished
>>>
```

```python
msg = "Hello world!"
file = open("newfile.txt", "w")
amount_written = file.write(msg)
print(amount_written)
file.close()

>>>
12
>>>
```

### Working with Files

```python
try:
    f = open("filename.txt")
    print(f.read())
finally:
    f.close()
```
```python
with open("filename.txt") as f:
    print(f.read())
```

## More Types

### None

```python
>>> None == None
True
>>> None
>>> print(None)
None
>>>
```

```python
def some_func():
    print("Hi!")
var = some_func()
print(var)
>>>
Hi!
None
>>>
```

### Dictionaries

```python
ages = {"Dave": 24, "Mary": 42, "John": 58}
print(ages["Dave"])
print(ages["Mary"])
>>>
24
42
>>>
```

```python
primary = {
  "red": [255, 0, 0], 
  "green": [0, 255, 0], 
  "blue": [0, 0, 255], 
}
print(primary["red"])
print(primary["yellow"])
>>>
[255, 0, 0]
KeyError: 'yellow'
>>>
```

```python
bad_dict = {
  [1, 2, 3]: "one two three", 
}
>>>
TypeError: unhashable type: 'list'
>>>
```

### Dictionary Functions

```python

```

### Tuples

```python

```

### List Slices

```python

```

### List Comprehensions

```python

```

### String Formatting

```python

```

### Useful Functions

```python

```

### Text Analyzer

```python

```
## Functional Programming
## Object-Oriented Programming
## Regular Expressions
## Pythonicness & Packaging

