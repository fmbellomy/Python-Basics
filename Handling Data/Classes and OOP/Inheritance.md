# Inheritance
Sometimes, you want multiple classes to have *shared* behavior, but still be different in how they function.
Often, people will reach for Inheritance to solve this problem
Inheritance is a way of taking a class, and then making a new class that has new functions or data inside of it, as well as all the stuff from the old class.
Continuing our `Car` example from the previous example, let's write a `Vehicle` class.

```python
class Vehicle:
	# This is the code that gets run when you create a new Car object.
	# toyota = Car("Toyota", 12, 100)
	def __init__(self, name, tank_capacity, miles_per_gallon):
		self.name = name
		self.tank_capacity = tank_capacity,
		self.gas_in_tank = 0
		self.miles_per_gallon = miles_per_gallon

	def fillTank(self):
		self.gas_in_tank = tank_capacity

	def addGas(self, gasAmount):
		if(gasAmount < 0):
			print("you can't add negative gas dingus.")
			return

		self.gas_in_tank += gasAmount
		if(self.gas_in_tank > self.tank_capacity):
			print("oops, we overfilled the tank and some overflowed.")
			self.gas_in_tank = self.tank_capacity


	def canDrive(self, num_miles):
		return self.gas_in_tank * self.miles_per_gallon > num_miles

	def drive(self, num_miles):
		if(canDrive(num_miles)):
			self.gas_in_tank -= num_miles / self.gas_in_tank
			print("drove", num_miles, "miles!")
		else:
			print("not enough mileage to drive that far.")
```

This Vehicle could be a car, a truck, a motorcycle, or really anything with a gas tank and an engine.
Now we can write new classes like a Car class that add Car-specific code.

```python
class Car(Vehicle):
	# I cannot think of anything a Car can do that a truck can't, so I actually won't put any new code here.
	# Just imagine a situation where there are multiple objects that have some things in common, but not other things.
```
Now there's a Car class that *extends* Vehicle.
We can use it like this.
```python
nissan = Car("nissan", 12, 120)
```
This is identical to if we used `Vehicle("nissan", 12, 120)`, but later down the line we could add Car-specific code that a normal *Vehicle* may not be able to use.

You've seen this before, however. Every time you write `for x in list:`. The `list` is "inheriting" or "implementing" (its similar, dont worry about it yet) an interface called "iterable."
Things that are iterable must have two functions: ```__next__()``` and ```__iter__()```
From there, python can tell that the object must be iterable, and you're allowed to use it in a for-loop.

I'll stop explaining it myself here, and if you want to you can read up on it a bit more online.
```
```
```
```