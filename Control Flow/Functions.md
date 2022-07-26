# Functions
A function is a piece of code that has been broken off into a chunk to be easily re-used.
For the simplest example of a function, here's a function that just prints 3 empty lines to the console.
```python
def print_three_blank_lines():
	print()
	print()
	print()


print("the program has started")
print_three_blank_lines()
print("there are three blank lines there now")
```

That's not a very useful function though, so maybe you want a function that *takes in* values, and *returns* a value as a result?
Maybe just a function that adds two numbers?

## Parameters and Return Values
(NOTE: To clarify, *parameters* and *arguments* refer to the same thing. They both mean "inputs to a function")

```python
def add(x, y):
	return x + y

print(add(9,10))
```
This also isn't a very useful function because it's not any easier than just writing `9+10` normally. A more useful function could be to maybe handle [[Read User Input from the Console|reading input from the user]], and then automatically [[Types of Data#How to change data from one type to another|converting]] it to an [[Types of Data#int Integer|integer]]?

```python
def read_integer(prompt):
	x = input(prompt)
	return int(x)

num = read_integer("enter a number")
print(num)
```

This is a slightly more useful function, but to really show you the benefit of a function, here's one that calculates the distance between two points using the distance formula. Don't worry about using some of the weird notation here, just pay attention to how much it would suck to write this code without having the `distance` function already written.

```python
def distance(point1, point2):
	return math.sqrt(math.pow(point1[0] - point2[0], 2) + math.pow(point1[1] - point2[1]), 2)

def read_float():
	return float(input("enter a number"))

p1 = (0.0, 0.0)
p2 = (10.0, 0.0)
p3 = (read_float(), read_float())

print(distance(p1,p2))
# should print 10.0
print(distance(p1,p3))
# no way of knowing what this will print, we don't know the values of p3
print(distance(p2,p3))
# same thing here.
```

Imagine having to write that entire distance function out over and over again... Agony. That's a big part of what makes functions appealing, they provide a way to avoid retyping the same code over and over again.

*[[Table of Contents|back to table of contents]]*