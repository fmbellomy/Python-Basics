# Compound Assignment
Assignment is the process of putting a value into a variable, like so.
```python
x = 10
name = "yeah"
```
Sometimes, however, you want to perform an action on a variable that uses the variables current value.
In that case, the normal way to write it would be as so.
```python
x = 10
x = x + 3
# Now x is 13, because we just assigned x to the value `10 + 3`
```
This works, but it's not very fun to write or particularly easy to understand.
If it looks confusing, that's fine. People don't usually write code that way, because we have ***compound assignment operators.***

## An example of compound assignment.
Here is the same code example written out using compound assignment.
```python
x = 10
x += 3
# Now this code seems more obvious. Think of "x += 3" to mean "add 3 to x"
```
### other compound assignment operators, because of course they exist
See [[Math Operators]] if you don't know some of these.
```python
# Here's all the other compound assignment operators in action.
# division
x = 11
x /= 2
# X == 5.5

# integer division
x = 4
x //= 3
# X == 1

# multiplication
x = 10
x *= 3
# X == 30

# exponentiation
x = 10
x **= 3
# X == 1000

# modulus
x = 10
x %= 7
# X ==  3

# addition
x = 10
x += 5
# X == 15

# subtraction
x = 10
x -= 5
# X == 5

```

*[[Table of Contents|back to table of contents]]*