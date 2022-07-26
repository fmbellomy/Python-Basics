# Importing Modules

Python has a lot of functions available to the programmer, but not all of them are available all the time. Most programs don't need to use the `sqrt()` function, so including it by default is impractical.
In order to include functions from outside of the base features of the language, you have to `import` them at the top of the file.
```python
import math
for i in range(100):
	print(math.sqrt(i))
```
### Using pip
The example here, `math`, comes bundled with every installation of python, but sometimes you may want to include functions written by other people!

In this case, you'll most likely want to use the `pip` package manager to install libraries with the command line. That would look something like this:
```bash
pip install overwatch-stats
```
and then you can import `overwatch.stats` in your python code like this:
```python
import overwatch.stats
my_stats = overwatch.stats.query("BopVendor#3346")
```

### Your files are modules too
Once you get skilled enough at python, you may find yourself working on projects too large or complex to be put into a single file. In this case, you may have multiple files like this:
```
├── graphics/
│   ├── cube.py
│   ├── opengl.py
├── util/
│   ├── save.py
│   ├── spacecalc.py
│   ├── gravity.py
├── api/
│    ├── sauce.py
│    └── twitter.py
├── helper.py
└── main.py
```
In this project, there are lots of other files we will probably want to use in our `main.py` file. Doing this is easy, just `import` them!

```python
import helper
import graphics.opengl
import util.save
import api.twitter

def run():
	print("Starting...")
	# more code here blah blah blah

if(__name__ == "__main__"):
	run()
```
That `if(__name__ == "__main__"):` thing is just so that way the code in this file can be used as a library *or* as a program, depending on if it's imported by another file or actually executed. You *probably* don't need to worry about it yet.


*[[Table of Contents|back to table of contents]]*