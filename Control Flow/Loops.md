# Loops
Loops are a way of repeatedly executing code a certain number of times.
Here's a simple loop that prints "HELLO" a hundred times.
```python
for i in range(100):
	print("HELLO")
```
You also can use that newly created `i` variable in the loop, however, if you want to know which iteration you're in.
```python
for i in range(100):
	my_function(i)
```
This way, you can repeatedly call the same code with a lot of different inputs, or as you may have seen in [[Lists]], you can use this to perform the same code on every element of a list.
```python
names = ["Todd", "Jeremy", "Christie", "Cameron"]
for i in names:
	print("heyo " + i)
```

If you want to learn more about `for` loops, consider checking out the [[Iterable]] page. If it goes over your head, don't worry about it and come back to it later.

*[[Table of Contents|back to table of contents]]*