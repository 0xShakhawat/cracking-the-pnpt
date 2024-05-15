# Learned
### Fundamentals of Python
    - Strings  
    - Math  
    - Variables and Methods  
    - Functions  
    - Boolean Expressions and Relational Operators  
    - Conditional Statements

# A Few Details

### Strings
```python
#Print string
print("Hello, world!")
print('Hello, world!')
print("""This string runs
multiple lines!""")
print("This string is "+"awesome!")#we can also concatenate
print('\n')#new line
print('Test that new line out.')

```  


```python
name = 'Alice'
age = 30
print("My name is %s and I'm %d years old." % (name, age))
# Output: My name is Alice and I'm 30 years old.

```   
 

### Math 
```python
#Math
print(50 + 50)#add
print(50 - 50)#subtract
print(50 * 50)#multiply
print(50 / 50)#divide
print(50 + 50 - 50 * 50 / 50)#PEMDAS
print(50 ** 2)#exponents
print(50 % 6)#modulo - takes what is left over
print(50 / 6)#division with decimals
print(50 // 6)#no remainder
```  

```python
import math
# Using math functions
print(math.sqrt(25)) # Output: 5.0
print(math.pow(2, 3)) # Output: 8.0
print(math.sin(math.pi/2)) # Output: 1.0

# Using math operators
x = 10 y = 3 print(x + y) # Output: 13
print(x / y) # Output: 3.3333333333333335
print(x // y) # Output: 3
print(x % y) # Output: 1
print(x ** y) # Output: 1000

```
 

### Variables and Methods
```python
#Variables and Methods
quote = "All is fair in love and war."
print(quote)

print(quote.upper())#uppercase
print(quote.lower())#lowercase
print(quote.title())#title case
print(len(quote))#counts characters


name = "Shakhawat"#string
age = 20#int
gpa = 5.0#float - has a decimal

print(int(age))
print(int(30.1))
print(int(30.9)) - Will it round? No!

print("My name is " + name + " and I am " + str(age) + " years old.")


age +=1
print(age)

birthday = 1
age += birthday
print(age)
```  

```python
# Variable assignment
x = 10
name = "John"
is_true = True


# Variable usage
y = x + 5
print("Hello, " + name)
if is_true:
    print("The condition is true")
```  

```python
# Built-in method example
numbers = [1, 2, 3, 4, 5]
length = len(numbers)
print("Length:", length)


# User-defined method example
def greet(name):
    print("Hello, " + name)


greet("Alice")
```

### Functions

```python
#Functions
print("Here is an example function:")

def who_am_i():#this is a function without parameters
	name = "Shakhawat"
	age = 20#local variable
	print("My name is " + name + " and I am " + str(age) + " years old.")

who_am_i()

#adding parametersdef add_one_hundred(num):
	print(num + 100)

add_one_hundred(100)

#multiple parametersdef add(x,y):
	print(x + y)

add(7,7)

def multiply(x,y):
	return x * y

multiply(7,7)
print(multiply(7,7))

def square_root(x):
	print(x ** .5)

square_root(64)


def nl():
	print('\n')

nl()
```  
```python
def greet(name):
    print("Hello, " + name + "!")


greet("Alice")

``` 

### Boolean Expressions and Relational Operators

```python
#Boolean expressions (True or False)
print("Boolean expressions:")

bool1 = True
bool2 = 3*3 == 9
bool3 = False
bool4 = 3*3 != 9

print(bool1,bool2,bool3,bool4)
print(type(bool1))

bool5 = "True"
print(type(bool5))

nl()

#Relational and Boolean operators
greater_than = 7 > 5
less_than = 5 < 7
greater_than_equal_to = 7 >=7
less_than_equal_to = 7 <= 7

test_and = True and True#True
test_and2 = True and False#False
test_or = True or True#True
test_or2 = True or False#True

test_not = not True#False
```
```python
x = 5
y = 10


# Relational operators
print(x == y)   # Output: False
print(x < y)    # Output: True


# Boolean expressions
print(x < y and y > 0)    # Output: True
print(x < y or y < 0)     # Output: True
print(not (x == y))       # Output: True
```
### Conditional Statements
```python
#Conditional Statementsdef drink(money):
	if money >= 2:
		return "You've got yourself a drink!"
	else:
		return "No drink for you!"

print(drink(3))
print(drink(1))


def alcohol(age,money):
	if(age >= 21) and (money >= 5):
		return "We're getting a drink!"
	elif (age >= 21) and (money < 5):
		return "Come back with more money."
	elif (age < 21) and (money >= 5):
		return "Nice try, kid!"
	else:
		return "You're too poor and too young!"

print(alcohol(21,5))
print(alcohol(21,4))
print(alcohol(20,5))
print(alcohol(20,4))
```
```python
if condition1:
    # code to be executed if condition1 is true
elif condition2:
    # code to be executed if condition1 is false and condition2 is true
else:
    # code to be executed if all conditions are false
```
example:
```python
x = 5
if x > 0:
    print("x is positive")
elif x < 0:
    print("x is negative")
else:
    print("x is zero")
```  


