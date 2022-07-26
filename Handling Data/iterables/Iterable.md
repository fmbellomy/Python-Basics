# What is an iterable?
The `for x in ` syntax actually applies to anything *iterable*, which means it works on [[Dictionaries]], [[Lists]] and any other data type that holds multiple pieces of data.

This is also why we use `range(10)` instead of just `for x in 10`
The function `range(10)` returns an *iterator* from 0 to 9, which acts the same as looping over a list of the numbers 0 to 9.
Iterators don't have to be lists though, as it would be very impractical to create a list from 0 to 1000 if you wanted to make a loop that runs 1000 times.

*Iterators can actually do anything they want internally, but they're expected to cover every element in a "list" type structure.*

If you have a custom data structure like a Tree, you could write multiple different iterators for it.

```
# Example of a tree numbered by BFS

[3]   [4]   [5]   [6]
 |     |     |    |
 --[1]--     --[2]-
    |          |
	----[0]----
```
This tree is ordered according to "Breadth First Search."
Iterating through it would go lengthwise across all the possible options, and then down another level through all the options in that level.

Another Tree iterator would look like this!

```
# Example of a tree numbered by DFS

[2]   [3]   [5]   [6]
 |     |     |    |
 --[1]--     --[4]-
    |          |
	----[0]----
```
This tree is ordered according to "Depth First Search"
Iterating through it would go down as far as possible, and when it hits a dead-end, only go back far enough until it has new options to go back down. This continues until it has exhausted every element in the tree.

Both ways of iterating over the tree are valid, but they don't act exactly the same way. As such, keep in mind that iterators may not always work the way you expect them to *under the hood,* but that they will always more or less fulfill the same purpose.

*[[Table of Contents|back to table of contents]]*