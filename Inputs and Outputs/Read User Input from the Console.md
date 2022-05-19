# How to get user input from the console.
Use the `input()` function, and assign it to a variable like this:

```python
f_name = input("What is your first name?")
print("Your first name is: " + name)
```
You may notice that input() is capable of taking in a string as an argument, to act as the "*prompt*" for the user to type something. 
This isn't actually necessary, and can be completely ignored if you wish.
```python
x = input()
y = input()
z = input()
```

### A problem you will probably encounter.
If you run into issues with data obtained from `input()` it probably means that your data is of the wrong [[Types of Data|type.]] See [[Types of Data#How to change data from one type to another|How to change data from one type to another]].