# Learned
### Fundamentals of Python
- [Building A Shoe Budget Tool](#building-a-shoe-budget-tool)

# A Few Details
### Building A Shoe Budget Tool
```python
class Shoes:
        def __init__(self, name, price):
                self.name = name
                self.price = float(price)

        def budget_check(self, budget):
                if not isinstance(budget, (int, float)):
                        print('Invalid entry. Please enter a number.')
                        exit()

        def change(self, budget):
                return (budget - self.price)

        def buy(self, budget):
                self.budget_check(budget)

                if budget >= self.price:
                        print(f'You can cop some {self.name}')

                        if budget == self.price:
                                print('You have exactly enough money for these shoes.')
                        else:
                                print(f'You can buy these shoes and have ${self.change(budget)} left over')

                        exit('Thanks for using our shoe budget app!')
```

```python
#!/bin/python3from Shoes import Shoes

low = Shoes('And 1s', 30)
medium = Shoes('Air Force 1s', 120)
high = Shoes('Off Whites', 400)

try:
   shoe_budget = float(input('What is your shoe budget? '))
except ValueError:
   exit('Please enter a number')

for shoes in [high, medium, low]:
   shoes.buy(shoe_budget)
```

```python
months = open('months.txt')

print(months)
print(months.mode)
print(months.readable())

months.close()


print(months.read())
print(months.readline())#reads one line
print(months.readline())#reads next line
print(months.readlines())#prints an array
print(months.readlines())#prints an empty array because we already read it
months.seek(0)
print(months.readlines()) - prints an array again

months.seek(0)
for month in months:
	print(month)

months.seek(0)
for month in months:
	print(month.strip())

days = open("days.txt", "w")
days.write("Monday")
days.close()

days = open("days.txt", "w")
days.write("\nTuesday") - overwrites
days.close()

days = open("days.txt", "a")
days.write("\nWednesday") - appends
days.close()
```