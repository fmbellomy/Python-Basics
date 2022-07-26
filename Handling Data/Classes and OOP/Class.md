# Class
A Class is a *recipe* for a compound data type.
Say you want to represent a Car with one variable.
You *could* make a list that has all the things you might need, like so.
```python
# Manufacturer, Gas in Tank (gallons), current speed (miles per hour), number of seats
car_list = ["Toyota", 2.6, 88, 4]
```

This is of course, not really *convenient.*
Later down the line, you would have to remember that `car_list[0]` is the brand. That's kinda weird, right?

"A dictionary!" I hear you say.
While it's true that a dictionary would be a little better, it still has its problems.
```python
car_dict = {
			"brand": "Toyota",
			"gas_in_tank": 2.6,
			"speed": 88,
			"num_seats": 4
}
print(car_dict["brand"])
```

Okay, great, now the data is represented in a way that's a bit more human-readable. What if we actually want to *use* that data? Say we want to drive a certain number of miles?
Gas should be subtracted from the tank, obviously, so lets do that!

```python
def drive(car, num_miles):
	car["gas_in_tank"] -= num_miles / 100 # this car gets 100 miles per gallon, i've decided. 

drive(car, 9999999)
print(car["gas_in_tank"]) # -99997.39
# uh oh we have negative gas...
```
We have encountered an *implementation issue.* Because `car`'s attributes are accessible from anywhere at any time, and can be set to any data, there's very little guarantee that a piece of code won't change it to utter nonsense! 
It's annoying to write safeguards in every single function you write, so wouldn't it be better if we could write those safeguards only one time and have them apply universally?

# Actually writing a class.
```python
class Car:
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

This class takes care of all the annoying checks you have to do to make sure your *Car* variable never holds any nonsense values.
To use the car class, code would look like this.
```python
toyota = Car("Toyota, 12, 100")
toyota.fillTank()
toyota.drive(1000) # drove 1000 miles!
toyota.drive(1000) # not enough mileage to drive that far.
```

You use classes all the time already, they're everywhere in python. [[Lists]] are a class, [[Dictionaries]] are a class, and so on. Everything where you can type `thing.doSomething()` is a class.

*[[Table of Contents|back to table of contents]]*