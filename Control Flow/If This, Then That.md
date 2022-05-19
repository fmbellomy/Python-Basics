# If this, then that
If statements provide a way of executing code only if a certain *condition* is met.
```python
if(100 > 8):
	print("100 is greater than 8, that's good.")
```
This example is shallow because we already know that 100 > 8, but in the event that we *don't* know what data we're dealing with, it's quite useful.
```python
name = input("enter a new username")
if(len(name) > 32):
	"name exceeds length limit, please use a different name"
```

# Else, do this
If statements can be *extended* through the use of ***else*** statements, which will *only* execute if the previous if statement didn't run.

```python
if(100 > 8):
	print("okay math still works everything is fine")
else:
	print("WHAT HOW")
```

This is functionally equivalent to writing this code:
```python
if(100 > 8):
	print("okay math still works everything is fine")
if(100 <= 8):
	print("WHAT HOW")
```
The ***else*** statement provides a way to run code *only if* the previous ***if*** statement didn't run.

# Elif, and branch chaining.
This is something you will sometimes find yourself needing to do. Maybe there's more than just 2 branches of code you need? In that case, you can use the ***elif*** statement, which allows you to chain as many if statements in a row as you like.

```python
name = input("what's your name")

if(name is "todd"):
	print("get real, todd")
	
elif(name is "johnny"):
	print("man it's been a while, what's good john")
	
elif(name is "you"):
	print("you're not me! i'm me!")
	
else:
	print("yeah i don't know who you are, sorry.")
```
