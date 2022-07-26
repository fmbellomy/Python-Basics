# Dictionaries
Dictionaries are *kind of*  like [[Lists]] in that they contain more than one piece of data, but different in that you do not access a dictionary item by its position.
Dictionaries contain *key/value pairs.*  Or, in other words, they contain pairs of data, where one piece is used to access the other piece.
This concept is a little hard to explain in English, so I'll just show you a small example of a dictionary in use.

```python
# The things before the colon are the KEYS
# The things after the colon are the VALUES
dictionary_example = {
	"john": "guardian",
	"egbert": "creeper",
	"jack": "enderman",
	"paul": "raid"
}

# This will print "enderman"
print(dictionary_example["jack"])

# This will cause an error, because "creeper" is a VALUE, and not a KEY
print(dictionary_example["creeper"])
```
Dictionaries are incredibly useful for *associating* data with other data. They're so useful they pop up nearly everywhere in real-world code, so becoming familiar with their usage is incredibly important.

### A few more ways to interact with Dictionaries
When you have a dictionary, you may not always know what is actually inside of it. Perhaps you want to access "paul", but you're not sure if "paul" even exists?
In that case, python provides this syntax for optionally performing code depending on if an element exists.
```python
if("paul" in dictionary_example):
	print(dictionary_example["paul"], "exists!")
else:
	print("paul did not exist :(")
```
Other than that, sometimes just *creating* a dictionary with values isn't enough. Maybe you want to add new data later?
To do that, python provides *this* syntax.
```python
dictionary_example["karl"] = "shulker"

print(dictionary_example["karl"], has been added to the dict!)
```
## A note on the efficiency of dictioaries
Dictionaries are fast. Like, really fast.
You may think you could achieve the same thing a dictionary does by making two parallel lists like this:
```python
list_keys["paul", "jack", "karl"]
list_values["enderman", "creeper", "shulker"]

for index, item in enumerate(list_keys):
	if(item == "paul"):
		print(list_values[index])
```
Other than the syntax being a little cluttered for this kind of behavior, its also ***significantly*** slower than a dictionary.
Behind the scenes, dictionaries rely on a data structure called a HashMap, or HashTable. These use something called a Hash Function to create unique and long numbers for every input. This long number can be manipulated to be smaller, and then used as the *index* for an internal list. 
From that point, Python has a way of getting something's position in a list in only about 2 steps, no matter what the input is and no matter how many things are in that list.
A dictionary could have 3 million items in it, and it would still be able to grab an item nearly instantly.
*[[Table of Contents|back to table of contents]]*