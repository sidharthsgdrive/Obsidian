Inheritance demonstration:
```Python
class Person(): # Superclass
	 def __init__(self, name, age):
		self.name = name
		self.age = age
	def display(self):
		print(self.name, self.age)
		
class Student(Person): #Subclass
	def __init__(self, name, age, marks):
		super().__init__(name, age) # execute superclass init method
		self.marks = marks
	def display(self):
		super().__display__() # execute superclass display method
		print(self.marks)

class Employee(Person): #Subclass
	def __init__(self, name, age, salary):
		super().__init__(name, age) # execute superclass init method
		self.salary = salary
	def display(self):
		super().__display__() # execute superclass display method
		print(self.salary)

s = Student('Rida', 20, 250)
s.display()
d = Employee('Harsh', 30, 50000)
d.display()
```

Private members for parent classes:
```Python
class Person():
	self.__age = age # Private member
```
