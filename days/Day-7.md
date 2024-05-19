# Learned
### Fundamentals of Python
   - Lists
   - Tuples
   - Looping
   - Advance Strings

# A Few Details
### Lists
```python
#Lists - Have brackets []
movies = ["When Harry Met Sally", "The Hangover", "The Perks of Being a Wallflower", "The Exorcist"]

print(movies[1])#returns the second item in the list - index / indices
print(movies[0])#returns the first item in the list
print(movies[1:3])#returns the first number given until right before last number given
print(movies[1:4])#returns all
print(movies[1:])#returns everything from number to end of list
print(movies[:1])#everything before 1
print(movies[:2])
print(movies[-1])#grabs last item

print(len(movies))#counts items in list
movies.append("JAWS")
print(movies)#appends to end of list

movies.insert(2, "Hustle")
print(movies)

movies.pop()#removes last item
print(movies)

movies.pop(0)#removes first item
print(movies)

amber_movies = ['Just Go With It', '50 First Dates']
our_favorite_movies = movies + amber_movies
print(our_favorite_movies)

grades = [["Bob", 82], ["Alice", 90], ["Jeff", 73]]
bobs_grade = grades[0][1]
print(bobs_grade)
grades[0][1] = 83
print(bobs_grade)
```
 
### Tuples
```python
fruits = ("apple", "banana", "orange")
fruits2 = ("grape", "kiwi")

combined = fruits + fruits2
print(combined)         # Output: ("apple", "banana", "orange", "grape", "kiwi")

print(len(fruits))      # Output: 3

subtuple = fruits[1:3]
print(subtuple)         # Output: ("banana", "orange")

```
```python
#Tuples - Do not change, ()
grades = ("a", "b", "c", "d", "f")

grades.pop, grades.append won't work - not mutable

print(grades[1])
```
### Looping
```python
#For loops - start to finish of an iterate
vegetables = ["cucumber", "spinach", "cabbage"]
for x in vegetables:
	print(x)

#While loops - execute as long as true
i = 1

while i < 10:
	print(i)
	i += 1
```

### Advanced Strings
```python
#ADVANCED STRINGS

my_name = "Heath"
print(my_name[0])#first letter
print(my_name[-1])#last letter

sentence = "This is a sentence."
print(sentence[:4])

print(sentence.split())#delimeter - default is a space

sentence_split = sentence.split()
sentence_join = ' '.join(sentence_split)
print(sentence_join)

quote = "He said, 'give me all your money'" - show example
quote = "He said, \"give me all your money\""
print(quote)

too_much_space = "                       hello          "
print(too_much_space.strip())

print("A" in "Apple")#returns true
print("a" in "Apple")#returns false - case sensitive

letter = "A"
word = "Apple"
print(letter.lower() in word.lower())#improved

movie = "The Hangover"
print("My favorite movie is {}.".format(movie))
print("My favorite movie is %s" % movie)
print(f"My favorite movie is {movie}")
```