# Printing to the Console
## You can print text to the console using Python's `print()` [[Functions|function]].
```python
print("Like this, you see?");
```
## Using multiple arguments
```python
print("This", "is", "multiple", "words.")
print("This is also multiple words.")
```
This seems like a not particularly useful feature, but comes in handy if you're printing the value of a [[Variables|variable.]]

```python
name = "Smelvin"
print("Hey", name, "what's good?")
```
### But the spaces are annoying, what if I don't want them?
Python also has support for "named arguments" to a function, and `print()` has a named argument called `delimiter` that determines what to put in between each element, which you can set like this:
```python
list = [1,2,3,2,1]
print("Numbers:")
print(list[0], list[1], list[2], list[3], list[4], delimiter=",")
# This will print `1,2,3,2,1`
```

## Using String Concatenation
The same effect can be achieved by using the `+` operator to add or *concatenate* the values together.
```python
print("This " + "is " + "also " + "a way " + "to do this.")
```
Unlike passing every string as an individual argument, string concatenation does *not* automatically put spaces in between your strings, so you have to add them yourself.