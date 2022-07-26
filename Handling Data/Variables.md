# Variables 
Variables are simple and incredibly powerful tools.
The standard way to teach variables is to imagine them as a *box* that stores a piece of data.
```python
x = 7
print(x)
print(x + 3)
```
In this program, `x` could be changed to literally any number, and it would still print that number, followed by whatever that number plus 3 is.

The process of putting a value into a variable is called *assignment*, and there are also [[Compound Assignment|compound assignment]] operators that allow you to set a variable to a new value while taking it's current value into account.

Variables are most useful for whenever you're grabbing data from somewhere outside your program, like reading from a file or [[Read User Input from the Console|having the user type something in.]] 
```python
file = open("filename.txt")
print(file.read())
```
```python
user_input = input("enter some stuff idk")
print(user_input)
```
In these cases, you have absolutely no idea what you're going to be dealing with, and you may need to re-use that data later on, so it's best to store it in a variable to be re-used.

*[[Table of Contents|back to table of contents]]*