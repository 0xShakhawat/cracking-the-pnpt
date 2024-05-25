# Learned
### Fundamentals of Python
   - User Input
   - Reading and Writing Files
   - Classes and Objects

# A Few Details
### User Input
```python
#USER INPUT

x = float(input("Give me a number: "))
o = input("Give me an operator: ")
y = float(input("Give me yet another number: "))

if o == "+":
	print(x + y)
elif o == "-":
	print(x - y)
elif o == "/":
	print(x / y)
elif o == "*":
	print(x * y)
elif o == "**":
	print(x ** y)
else:
	print("Unknown operator.")
```

### Reading and Writing Files
Reading form a file
```python
# Open the file in read mode
file = open("example.txt", "r")


# Read the entire content
content = file.read()
print(content)


# Read a single line
line = file.readline()
print(line)


# Read all lines
lines = file.readlines()
print(lines)


# Close the file
file.close()
```
Writing to aFiles
```python
# Open the file in write mode
file = open("example.txt", "w")


# Write content to the file
file.write("Hello, World!\n")
file.write("This is a new line.")


# Close the file
file.close()
```
### Classes and Objects
```python
class Employees:

	def __init__(self, name, department, role, salary, years_employed):
		self.name = name
		self.department = department
		self.role = role
		self.salary = salary
		self.years_employed = years_employed

	def eligible_for_retirement(self):
		if self.years_employed >= 20:
			return True
		else:
			return False
```
```python
from Employees import Employees

e1 = Employees("Bob", "Sales", "Director of Sales", 100000, 20)
e2 = Employees("Linda", "Executive", "CIO", 150000, 10)

print(e1.name)
print(e2.role)
print(e1.eligible_for_retirement())
```