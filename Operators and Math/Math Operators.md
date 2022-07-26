# Math Operators in Python
There's a lot of common math operations one needs to be able to perform in nearly every program.
Here is a list of the most common operations you'll need to perform, and usage examples.


## Addition
```python
num = 3 + 4;
# This is just standard addition.
# In this case, num == 7
```
## Subtraction
```python
num = 4 - 3; 
# Once again, this works exactly as you'd expect. Just basic subtraction.
# num == 1
```
## Multiplication
```python
num = 4*3
# This too works how you would expect. It multiplies the two numbers.
# num == 12
```

# ***Division***
There are two kinds of division in python, "integer division" and what you would normally think of when you think of division.

## "Normal" Division
```python
num = 4/3
# This is what you would expect from something like a calculator.
# num == 1.333333
```
## Integer Division
```python
num = 4//3
# Using two / operators tells python that you do *not* want a decimal number as your answer.
# In this case, python will round *DOWN* to the nearest whole number. 
# num == 1

# This is useful for knowing how many times you can fit X into Y, as being able to fit 0.44 people into a box isn't very useful information. Use this for if you only care about how many *full* things can fit into another.
```

## Exponentiation
```python
num = 2**3
# This is the equivalent of 2 to the 3rd power, or 2 cubed, or 2^3.
# You're probably familiar with this operation already.
# num == 8 (2*2*2)
```
## Modulus (remainder)
```python
# Sometimes you care about the *remainder* after division.
num = 7 % 5
# This will divide 7 by 5 and then spit out whatever's left.
# num == 2 

# Modulus is especially important for finding whether or not a number is a multiple of another number.
# Here is a program that checks if a user input is a multiple of 7.
x = int(input("enter a whole number."))

# Because any multiple of 7 would be cleanly divisble by 7, there would be no remainder.
if(x % 7 == 0):
	print("you entered a multiple of seven.")
else:
	print("you did not enter a multiple of seven.")
```


*[[Table of Contents|back to table of contents]]*