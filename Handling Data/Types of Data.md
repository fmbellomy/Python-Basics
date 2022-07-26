# TYPES
There are many different types of data in programming, and most languages are very explicit about what type data is or has to be. Python is not, and it will do its best to keep you from having to worry about types. Unfortunately, it can't keep them away from you *all* the time, so you're going to have to at least be familiar with them.

## A list of all the data types you'll probably encounter.
### str (String)
A `string` is a sequence of `characters`. It can be of any length. Adding two strings together will concatenate them.
### int (Integer)
These are your *whole numbers*, like 1, 2, 3, and so on, as well as zero and negative numbers. They're what you probably want most of the time you're dealing with numbers in your code.
### float (Floating Point, or Decimal)
The `float` data type is the data type responsible for storing decimal values like **0.33**. It is imprecise, however, as you will notice from this code example.
```python
x = 0.1
y = 0.2
print(x + y)
# This will print `0.30000000000000004` to the console.
# It's *almost* 0.3, but off slightly.
```
Usually `float` imprecision is not a big deal, but it's worth knowing about in case it somehow does end up messing up your code down the line.
### bool (Boolean)
A `bool` can only be either True or False. Think of the expression `x == y`. This expression is either true or it isn't. To represent situations like that, where a function needs to return this "truthiness" of a result, you would use a `bool`.
Here is a code example using [[If This, Then That|if statements.]]
```python
test_variable = 7 > 6
# Here, test_variable gets assigned the value True

if(7 > 6):
	print("okay good math isn't broken")
if(7 < 6):
	print("how did this happen?")

if(test_variable):
	print("This should run because it's the same thing as saying `if(7 > 6)`")

if(True):
	print("This should also always run")

if(False):
	print("This will never run.")
```

## How to change data from one type to another.
This is a common problem. Lets say you're writing a program that needs to take a number from the user, and then add 20 to it. 
```python
x = input("enter a number:")
print(x + 20)
```
This program will not work as expected.
```bash
enter a number: 5

Traceback (most recent call last):
File "/home/username/script.py",
line 2, in <module>
	print(x + 20)
TypeError: can only concatenate str (not "int") to str
```
The `input()` function returns as `str`, no matter what. It's up to you to then *convert* that string into the data type you really want, which is an integer, or *int.*
Python provides functions that do this for you, and it's called ***Type Casting***
Here is the same code with Type Casting.
```python
x_as_string = input("enter a number:")
x = int(x_as_string)
print(x + 20)
```
Now we get the expected results, because we're adding two numbers together instead of adding a number on to the end of a string.
```bash
enter a number: 5
25
```

*[[Table of Contents|back to table of contents]]*