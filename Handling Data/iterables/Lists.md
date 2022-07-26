# Lists.
A list is technically a [[Types of Data|data type]], but for now it's easier to think of it as just what the name makes it sound like: a list of values.
Here's an example of a list.
```python
x = [1,1,2,3,5,8,13,21,34]
```
Here, `x` stores *all* of those values. In order to get a specific value, you have to grab the element out using its *index.*
```python
x = [10,20,30,40]
#    0, 1, 2, 3
third_element = x[2]
```
Take note of this! Lists start counting at `0`.  The first element of a list will *always* be its 0th element.

To [[Loops|loop]] over the contents of a list, you can use this notation.

```python
numlist = [4,2,4,1,-4,0,1]
for i in numlist:
	if( i < 2 ):
		print(i)
# will print 1,-4, 0, and 1 
```

*[[Table of Contents|back to table of contents]]*