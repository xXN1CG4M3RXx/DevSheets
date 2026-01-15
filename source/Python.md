---
Author: xXN1CG4M3RXx
Description: Comprehensive python Cheat-Sheet
---

# Python Cheat-Sheet
Welcome to the Python Cheat-Sheet!
Here you can find everything you need to know about Python, doesn't matter matter if your are still learning or if you're already a pro.

**Happy Coding!**

---

## Table of Contents
- [Python Cheat-Sheet](#python-cheat-sheet)
  - [Table of Contents](#table-of-contents)
  - [Variables](#variables)
    - [Types of Variables](#types-of-variables)
    - [Strings](#strings)
    - [Integers](#integers)
    - [Floats](#floats)
    - [Booleans](#booleans)
  - [Data Types](#data-types)
    - [Lists](#lists)
    - [Dictionaries](#dictionaries)
    - [Tuples](#tuples)
    - [Sets](#sets)
  - [Operators](#operators)
    - [Arithmetic Operators](#arithmetic-operators)
    - [Comparison Operators](#comparison-operators)
    - [Logical Operators](#logical-operators)
    - [Assignment Operators](#assignment-operators)
  - [Conditional statements](#conditional-statements)
    - [If statements](#if-statements)
    - [Else statements](#else-statements)
    - [Elif statements](#elif-statements)
  - [Match](#match)
  - [Loops](#loops)
    - [For loop](#for-loop)
    - [While loop](#while-loop)
  - [Functions](#functions)
    - [Defining functions](#defining-functions)
    - [Calling functions](#calling-functions)
    - [Returning values](#returning-values)
  - [Try - Except](#try---except)
  - [Classes](#classes)

---

## Variables

### Types of Variables
Type | Use | Example
--- | --- | ---
`string` | Storing text or single characters | `"Hello, World"`, `"a"`
`int` | Storing full numbers | `12`, `-5`
`float` | Storing decimal numbers | `3.14`, `-2.5`
`bool` | Storing true or false values | `True`, `False`

### Strings

Strings are used to store **text**. They can be any length or single characters. They are enclosed in either single or double quotes.

```python
# You can store a string in a variable like this:
# <name_of_string> = "<string>"

name = "John Doe" # String enclosed in double quotes
message = 'Hello, World' # String enclosed in single quotes
```

There are a lot of useful things you can do with strings.

```python
# Adding two strings together
message_part_1 = "Hello"
message_part_2 = "World"
message = message_part_1 ", "+ message_part_2 # Output: "Hello, World"

# Making a string all capitals...
message = "Hello, World"
message_upper = message.upper() # Output: "HELLO, WORLD"

# ...or all lowercase
message_lower = message.lower() # Output: "hello, world"

# Removing unnecessary whitespace
message = "   Hello, World   "
message_stripped = message.strip() # Output: "Hello, World"
```

### Integers

Integers are used to store **whole numbers**. They can be positive or negative

```python
# You can store an integer in a variable like this:
# <name_of_integer> = <integer>
number = 12

# Negative numbers also work
negative_number = -12
```

You are also able to do math with integers by using the following operators:

- Addition: `+` -> Adds two numbers together
- Subtraction: `-` -> Subtracts one number from another
- Multiplication: `*` -> Multiplies two numbers together
- Exponentiation: `**` -> Raises a number to a power
- Division: `/` -> Divides one number by another
- Floored Division: `//` -> Divides one number by another and rounds down to the nearest integer
- Modulus: `%` -> Returns the remainder of a division operation

```python
# Some examples of math with integers
x = 10
y = 3

# Addition
z = x + y # Output: 13

# Subtraction
z = x - y # Output: 7

# Multiplication
z = x * y # Output: 30

# Exponentiation
z = x ** y # Output: 1000

# Division
z = x / y # Output: 3.333...

# Floored Division
z = x // y # Output: 3

# Modulus
z = x % y # Output: 1
```

### Floats

Floats are used to store **decimal numbers**. They are very similar to integers and can be positive or negative.

```python
# Floats are stored similarly to integers, but with a decimal point.
# You can store a float in a variable like this:
# <name_of_float> = <float>
number = 3.14

# Negative numbers also work
negative_number = -3.14
```

Just like integers, you are also able to do math with floats by using the following operators:

- Addition: `+` -> Adds two numbers together
- Subtraction: `-` -> Subtracts one number from another
- Multiplication: `*` -> Multiplies two numbers together
- Exponentiation: `**` -> Raises a number to a power
- Division: `/` -> Divides one number by another
- Floored Division: `//` -> Divides one number by another and rounds down to the nearest integer
- Modulus: `%` -> Returns the remainder of a division operation

```python
# Some examples of math with floats
x = 5
y = 2.5

# Addition
z = x + y # Output: 7.5

# Subtraction
z = x - y # Output: 2.5

# Multiplication
z = x * y # Output: 12.5

# Exponentiation
z = x ** y # Output: 32.5

# Division
z = x / y # Output: 2.0

# Floored Division
z = x // y # Output: 2

# Modulus
z = x % y # Output: 1.0
```

Note that floats **always** have a decimal point, event if they don't have any digits after the decimal point.

### Booleans

Booleans are used to store one of two possible states, `True` or `False`. They are very useful for [conditional statements](#conditional-statements). To use them in conditional statements you don't **have** to store them in a variable.

```python
# You can store a boolean in a variable like this:
# <name_of_boolean> = <boolean>
is_true = True
is_false = False
```

Booleans are often used in conditional statements to check if a condition is true or false. They are also used in [loops](#loops).

```python
# Some examples for the use of booleans in conditional statements
# You can ignore the logic behind this code as we'll cover it in the conditional statements section

x = 3

if x < 5:
  is_less_than_five = True
else:
  is_less_than_five = False

if is_less_than_five:
  print("x is less than 5")

# The output of this program would be: "x is less than 5"
```

---

## Data Types

### Lists

Lists are used to store **multiple pieces of data**. You can e.g. store names in a list.

```python
# Lists are always indicated by the square brackets.
# You can store a list in a variable like this:
# <name_of_list> = [<item_1>, <item_2>, <item_3>, ...]
names = ["John", "Nic", "Mia"]
```

With lists you are able to do a lot of things. You can access **each individual item** of a list by using its **index**. The index of a list always starts at 0. You can also access a **range** of items by using a **colon**. A use that is very important is to **loop through a list** using a [for loop](#for-loop).

```python
# Accessing specific items in a list
names = ["John", "Nic", "Mia"]

print(names[0]) # Output: "John"
print(names[1]) # Output: "Nic"
print(names[2]) # Output: "Mia"

# You can also access items in reverse order by using negative indices
print(names[-1]) # Output: "Mia"
print(names[-2]) # Output: "Nic"
print(names[-3]) # Output: "John"

# Accessing a range of items in a list
print(names[0:2]) # Output: ["John", "Nic"]

# Looping through a list
for name in names:
  print(name)

# The output of this program would be:
# "John"
# "Nic"
# "Mia"
```

### Dictionaries

Dictionaries are very similar to lists. They are also used to store multiple pieces of data but with a different syntax. Dictionaries use something called a `key-value pair` to store data.

```python
# Dictionaries are always indicated by the curly brackets.
# You can store a dictionary in a variable like this:
# <name_of_dictionary> = {<key_1>: <value_1>, <key_2>: <value_2>, <key_3>: <value_3>, ...}
person_1 = {
  "name": "Nic"
  "age": 16
  "is_student": True
}

# Note that you typically write one `key-value pair` per line for better readability.
```

Just like with lists, you can access each individual item of a dictionary by using its **key**. You can also loop through a dictionary using a [for loop](#for-loop).

```python
# Accessing specific items in a dictionary
person_1 = {
  "name": "Nic"
  "age": 16
  "is_student": True
}

print(person_1["name"]) # Output: "Nic"
print(person_1["age"]) # Output: 16
print(person_1["is_student"]) # Output: True

# Looping through a dictionary
for key, value in person_1.items():
  print(key, value)

# The output of this program would be:
# "name Nic"
# "age 16"
# "is_student True"
```

### Tuples

Tuples are a little different from lists and dictionaries. They also store different pieces of data just like lists, but they are **immutable**. This means that you can't change the data in a tuple after it has been created.

```python
# Tuples are always indicated by the round brackets.
# You can store a tuple in a variable like this:
# <name_of_tuple> = (<item_1>, <item_2>, <item_3>, ...)
names = ("John", "Nic", "Mia")

# You can also mix different types of variables in a tuple
random_things = ("Banana", 16, 2.5, True)
```

Just like with lists and dictionaries, you can access each individual item of a tuple by using its **index**. You can also loop through a tuple using a [for loop](#for-loop).

```python
# Accessing specific items in a tuple
random_things = ("Banana", 16, 2.5, True)

print(random_things[0]) # Output: "Banana"
print(random_things[1]) # Output: 16

# Just like with lists you can access items in reverse order by using negative indices
print(random_things[-1]) # Output: True
print(random_things[-2]) # Output: 2.5

# Looping through a tuple
for thing in random_things:
  print(thing)

# The output of this program would be:
# "Banana"
# 16
# 2.5
# True
```

### Sets

Sets are just like a list with the only difference being that they are **unordered** and **can't be indexed**. Sets also **can't contain duplicate values**. Like tuples, items in a set are **immutable** meaning they can't be changed after creating the set, however new items **can** be added to a set and old items **can** be removed.

```python
# You can create a set like this:
# <name_of_set> = {<item_1>, <item_2>, <item_3>, ...}
names = {"John", "Nic", "Mia"}

# You can also mix different types of variables in a set
random_things = {"Banana", 16, 2.5, True}

# Adding items to a set
random_things.add("Apple") # Output: {"Banana", 16, 2.5, True, "Apple"}

# Removing items from a set
random_things.remove("Banana") # Output: {16, 2.5, True, "Apple"}

# Looping through a set
for thing in random_things:
  print(thing)

# The output of this program would be:
# 16
# 2.5
# True
# "Apple"

# Note that if you were to print a set the items in it would be in a completely random order each time you print it.
print(random_things) # This line would give you the set in this form but the items are shuffled: {<item_1>, <item_2>, <item_3>, ...}
```

---

## Operators

### Arithmetic Operators

### Comparison Operators

### Logical Operators

### Assignment Operators

---

## Conditional statements

### If statements

### Else statements

### Elif statements

---

## Match

---

## Loops

### For loop

### While loop

---

## Functions

### Defining functions

### Calling functions

### Returning values

---

## Try - Except

---

## Classes

---