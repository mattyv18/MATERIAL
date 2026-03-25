---
marp: true
title: Introduction to Python
author: Matthew Venzie
description: UCSAS 2026
theme: uncover
# class: [blue]
---


# Introduction to Python

## CSAS 2026

### Matthew Venzie

---

# About Me

<img src="IMG_7757.jpeg" alt="My Image" width="300">

- 3rd Year Applied Mathematics and Statistics Student at UConn
- Unergraduate Time Series Researcher

## Interests

- Modeling Time Series Data with a Neural Network Architecture(Mamba)
- Modeling with Biological Data(Biostatistics)
- Cooking

## Aspirations:

Statistics PhD!

---

# Why Python?
- Python is a readable object oriented language making it easier to understand to those who have never delt with programming

- It has many applications in fields such as software development, data engineering, statistics and mathematics

- There is a vast amount of libraries and tools that allow you to use whichever packages may fit your needs

- It is primarily used in new and hot fields such as Data Science, AI and Machine Learning

---

<table>
  <tr>
    <td><img src="nhl.png"></td>
    <td><img src="forecast_vs_actual2.png"></td>
  </tr>
</table>

---

# Prerequisites:

A laptop with access to internet.


---

# What we will be covering!
 basic syntax, data types, functions, loops, conditionals and classes, then combining this knowledge to build a simple algorithm.
- Basic Syntax (Variables, Indentation, Comments, Print Statements)
- Data Types
  - Strings (`str`)
  - Numerical types (`int`, `float`, `complex`)
  - Mapping (`dict`)
- Conditions, Loops, Functions, and Classes
- Python Packages and Algorithms

---

# Syntax
- We make comments to help document how our code works, so that when we come back to it we can easily remind ourselves what the code does
- To make a comment, just prefix whatever you typed with a `#`
- In Python, a newline indicates a start of a new command

```python
# Print Hello, CSAS 2026
print("Hello, CSAS 2026!")

print("Are you bored?")
```

---

## Numerical and Boolean Data Types

- Integer (`int`)
- Float (`float`)
- complex (`complex`)
  - Ex. `1 + 5j` where 5j is the complex component
- Boolean (`bool`)
  - Boolean represents two values wither 'True' or 'False'

---



# Data Types (continued)

## Strings ('str')

- String is basically a sequence of characters that can be accessed or iterated through 
- Multiline strings need three quotes and keep line breaks intact when printed.
- Operators like + concatenates(combines) strings
- When searching for membership commonly used methods are:
  - `replace("a", "b")`: replaces a with b in string
  - `split()`: splits a string based on a given separator in () that can be found in the string
  - `upper()` converts letters to uppercase, `lower()` converts letters to lower case, `strip()` removes leading and trailing whitespace, `capitalize()` capitalizes first letter and makes rest lower case
  - `count('a')` counts how many times 'a' appears in string, `endswith('a')` checks if string ends with specified substring 'a' and returns boolean, `startswith('a')` checks if a string starts with specified substring 'a' and returns boolean, `find('a')` returns the index of first occurence of specified substring 'a' and returns -1 if not found, `index('a')` same as find but raises error

---

## Note: types of strings

#### F-strings:

```python
>>> f"{5+2} is 7"

"7 is 7"

>>> x = 7
>>> f"{x} is 7"

"7 is 7"
```

- Makes it very easy to insert values, expressions and variables into a string.
- Very useful when printing multiple strings that include a changing variable

#### R-strings

```python
r"./practice.txt"
```

- Ensures that the contents of the strings is treated as-is (no escape characters for example)
- Especially useful when you are working with files

---

# Practice time!

## Q1, Q2: Manipulating Strings, 5 minutes

### Try not to look things up

### https://colab.research.google.com/drive/1t_x1m4N0gopUKamo-9Aju3qZUeKLh1sg?usp=sharing
---

# Data Types (continued)

## Lists

```python
["a", 1, True]
```

- Can contain any type of elements even functions
- Created using `[]`
- Indexed and Ordered as a sequence
- Index starts at 0
- Elements can be accessed like so:
  - First element: `x[0]`
  - Last Element: `x[-1]`
  - Slice of elements 0-2 does not include 3: `x[0:3]`
  - Slice of elements 0-1: `x[:2]`
  - Slice of elements 2-(n-1), with element n being the last element of the list: `x[2:]`
  - Copy of entire list: `x[:]`
- Elements can be modified using `x[1:4] = ["UCSAS", [1,2,3]]`
  - Thie would replace how ever many elemnts are indicated in teh slice with the elements provided, so elements 1,2,3 are replaced with `"UCSAS", [1,2,3]`
- Methods:
  - `len(x)`: returns length of list x
  - `x.insert(2, "Python")`: Insterts "Python" at index 2 of list x
  - `x.append("Python")`: Adds "Python" as new element at end of list x
  - `x.remove(2)`: Removes first occerence of element 2 from list x
  - `x.pop(1)`: Removes and returns element at index 1
  - `x.sort()`: Sorts elements of list in order i.e. numerical if elements are integers and floats and alphabetical if strings
  - `y = x.copy()`: Creates copy of list x
  - `x.extend(y)`: Appends elements of list y to the end of list x

---

# Data Types (continued)

## Tuples

```python
(1, 2, [1, 2], 1, "abc")
```

- Created using `()`
- Very similar to a list, but elements inside cannot be changed or be added (immutability)
  - This means that for any change made to the tuple, a new tuple will be created
- Accessing items is similar to a list.
- Methods: `len(x)`, `x.count("a")`, `x.index()`
  - Cannot use most methods of list on Tuple

---

# Data Types (Continued)

## Dictionary

- A `dict` is a mapped data type
  - This means it consists of a key-value pair, where a key is used to access a value i.e. the key maps to the value.
- The keys of a dictionary are immutable & duplicate keys will replace the original value, but the values themselves are mutable

```python
>>> ucsas = {"workshop": "Introduction To Python", "year": 2026} # creatng the dictionary
>>> ucsas["workshop"] # Accessing Values of "workshop" key
"Introduction To Python"
>>> ucsas["year"]
2027
>>> ucsas.keys() # returns keys
["workshop", "year"]
>>> ucsas["workshop"][0:12]
"Introduction"
>>> ucsas = {"workshop": "Introduction To Python", "year": [2025, 2026]}
>>> ucsas["year"].append(2027) # "year" now has value [2025, 2026, 2027]
>>> uscas
{'workshop': 'Introduction To Python', 'year': [2025, 2026, 2027]}
```

---

# Data Types (Continued)

## Duck Typing & type enforcement

- Python does not do data type checking.
- It behaves on the principle: "If it walks like a duck and quacks like a duck, then it must be a duck"

---

# Data Types

- Obviously this is not an exhaustive list
- So if you ever need to inspect the type of something, there is a nice built-in `type(x)` that returns the type of x.

---

# Variable Assignment

- Is as simple as writing the name of the variable `=` to some value.
- There is no need to define the type of the variable in Python, as it is determined on its own.

```python
# Integer Assignment
>>> x = 2
# String
>>> z = "UCSAS"
# Boolean
>>> w = True
# Dictionary
>>> y = {"sports": "Hockey", "Baseball", Basketball, "year": [2025, 2026]}
# printing variables
>>> print(x)
2
>>> print(z)
UCSAS
>>> print(w)
True
>>> print(y)
{"sports": "Hockey", "Baseball", Basketball, "year": [2025, 2026]}
```

---

# Practice time!

## Q3: Manipulating lists

### 5 min

---

# Operators

Arithmetic Operators:

- add: `+`, subtract: `-`, multiply: `*`, division: `/`, modulus: `%`(returns a remainder), exponentiation: `**`, floor division: `//` (rounds down to nearest integer after dividing)

Assignment Operators:

- equals: `=`, add and equal: `+=`, subtract and equal: `-=`, multiply and equal: `*=`, divide and equal: `/=`

Comparison Operators:

- value equality: `==`, value not equal: `!=`, value greater than: `>`, value less than: `<`, value greater than equal: `>=`, value less than equal: `<=`

Logical Operators:

- `and`, `or`, `not`, `in`

---

# Conditionals (If, elif, else)

- The conditionals should be based on a logical input such as ==, >=, >, <, <=, is, is not, in, not in.
- They can be written in one line if the statement has only one statement.
- An if statement cannot be empty. If it has to be, use `pass`
- If condition are to result in more than two cases, use elif
  and or can be used for the conditional.

---

# Conditionals (continued)

```python
## which player scored the most points this season and using `and` and `or`.
i, j, k = 95, 103, 70

if  i > j and i > k:
    print(f'{i} scored the most')
elif j > i and j > k:
    print(f'{j} scored the most')
elif i == j and j == k:
    print('They scored the same amount of points') 
else:
    print(f'{k} scored the most')


## checking between two players in one line
i, j = 109, 115

print('i scored more') if i > j else print('j scored more')

```

---

# Loops

## While loop

- It runs as long as a condition is true. Careful as it can run into an infinte loop if condition never gets satisfied.
- `break` and `continue` allows to either break or continue based on a condition within the loop.

```python
## First player to 5 matches won, wins game
a_score = 0
b_score = 0

A = 15
B = 21
while a_score != 5 and b_score != 5:
     if A > B:
        a_score += 1
        continue
     else:
        b_score += 1
        continue
print('Player A wins') if a_score > b_score else print('Player B wins')



```

---

# Loops (Continued)

## For loop

- Used to iterate over a sequence.
- `range(y, x)` function is useful as it gives a list of integers from y to x to iterate over excluding x
  -By default range(x) will start at 0 and stop at x

```python
## How many balls did the pitcher throw

pitch_count = ["ball", "ball", "strike", "ball", "strike", "strike", "strike", "ball", "ball"]

ball_count = 0
for i in range(len(pitch_count)):    #iterate using range()
    if pitch_count[i] == "ball":
       ball_count += 1
    else:
       continue


for pitch in pitch_count:      #iterate directly through list
    if pitch == "ball":
       ball_count += 1
    else:
       continue

print(f'The pitcher threw {ball_count} balls')
```

---

# Functions

- A function is defined using keywords `def` followed by the function name and arguments within parenthesis.
- A function should either print or return some value. Else pass should be used to avoid error.
- Often when we use functions to obtain values and store them in another variable, we need a return statement.
- Type hints are used for readability in functions to tell the reader what type of argument the function takes
  - Just place a semi-colon after the argument and indicate which type
  - This wont have any affect on the function it can still take other types it just tells you what type it should be taking 
- A lambda is a small anonymous function which returns the result in the same line (a useful property).

```python

def ball_count(pitch_count: list)  # ball count function takes list
    ball_count = 0
    for pitch in pitch_count:    
        if pitch == "ball":
           ball_count += 1
        else:
           continue
    return print(f'The pitcher threw {ball_count} balls')

def fib(n):    #returns n-th fibonacci number
    if (n==1 or n==2) return 1
    else return fib(n - 1) + fib(n - 2)
```

---

# Scope

- Scope: There are 4 scopes when it comes to accessing variables
  - Local: variables defined inside a function
  - Enclosing: Variables defined within nested functions, that is, it is defined outside the inner function and inside the outer function
  - Global: variables defined outside all functions
  - Built-in: built in pre-defined python names and functions
- A variable defined inside a function cannot be accessed outside the function
- A variable defined outside of a function can be accessed from within a function
- Try not to define functions or variables that are already pre-defined by python(built-in)

---

# Practice Q4

## Basketball Preformance Score

## 6 minutes

---

# Classes

- A class is a blueprint for objects
- It defines ways to initiate an object of the made up class, functions for various properties, methods, etc.
- **init**(self, parameters) is a function that exists for all classes - to initiate values to the class.
- Methods are defined for the object class using functions with parameter self and more within the class.

---

```python
class SoccerPlayer:
    def __init__(self, name, goals, assists, matches_played):
        self.name = name
        self.goals = goals
        self.assists = assists
        self.matches_played = matches_played

    def goals_per_match(self):
        if self.matches_played == 0:
            return 0
        return self.goals / self.matches_played

    def total_contribution(self):
        return self.goals + self.assists

    def add_match(self, assists_scored  goals_scored):
        self.goals += goals_scored
        self.assists += assists_scored
        self.matches_played += 1
        


print('Soccer Player Stats')

x = SoccerPlayer(Matt, 6, 3, 2)   
print(f'Goals per match:{x.goals_per_match()}')
print(f"Total Points Contributed:{x.total_contribution()}")
x.add_match(3,2)    # add new match
print(type(x))

```

---

# Sidenote: Getting help in Python

For any object, you can call the `dir()` function to see all the methods that it support

```python
>>> dir(list)
['__add__', '__class__', '__class_getitem__', ...]
```

For any function, you can call the `help()` function to read more about what the function does and what its arguments represent

```python
>>> help(sorted)
sorted(iterable, /, *, key=None, reverse=False)
    Return a new list containing all items from the iterable in ascending order.

    A custom key function can be supplied to customize the sort order, and the
    reverse flag can be set to request the result in descending order.
```

---

# Practice Q5

## Hockey Statistics


---

# Python Packaging and Virtual Environments

---

## Packaging and Package Managers

### Packages

In Python, a package is a collection of modules grouped together to organize and structure code. It allows for better code management, reuse, and distribution.

### Package Manager

- A package manager is a tool that automates the process of installing, upgrading, configuring, and removing software packages. In Python, popular package managers include pip and conda (Anaconda).
- They streamline the installation and management of Python libraries and dependencies.
- Pip generally comes with a standard Python installation, while conda is its own python distribution and needs to be installed separately

---

## Example: Installing Pandas

### Pip

```sh
pip install pandas
```

### Conda

```sh
conda install pandas
```

---

## Python Virtual Environments 

- Self-contained directory that encapsulates a Python interpreter along with its associated libraries and scripts.
- It enables developers to create isolated environments for different projects, each with its own dependencies and versions of Python packages.
- This isolation prevents conflicts between packages and ensures project is reproducible across different environments.
- A common way of creating a virtual environments is conda
- To use conda first install either Anaconda or Miniconda see https://www.anaconda.com/docs/getting-started/miniconda/main


---

## Creating Virtual Environment

### Conda

```sh
conda create -n env_name
conda activate -n env_name
```



---

# Core libraries for Sports Analytics

## NumPy, Pandas, and Matplotib

---

# NumPy

- A library for working with arrays/vectors.
- Efficiently stores and manipulates numerical data.
- Boasts fast matrix operations on entire arrays

---
## NumPy Example
```py
import numpy as np
# Create a 2D NumPy array representing hockey player statistics
player_stats = np.array([
    [40, 39, 30, 1.8, 80],  # Player 1: Total Goals, Total Assists, Total penalties minutes, Height(m), Games Played
    [20, 50, 20, 1.70, 79],  # Player 2
    [30, 40, 16, 1.65, 68],  # Player 3
    [60, 20, 34, 1.95, 72]   # Player 4
])
# Accessing elements
print(f"\nPoints scored by Player 2: {player_stats[1, 0] + player_stats[1, 1]}")# add goals and assists, row 1 column 0 and row 1 column 1
# Calculating the average goals scored
average_goals = np.mean(player_stats[:, 0])  # All rows, column 0
print("\nAverage Goals Scored Among players:", average_goals)
# Calculating the average height
average_height = np.mean(player_stats[:, 3])
print("Average Height:", average_height)
# Finding the maximum penalty minutes
max_pen = np.max(player_stats[:, 2])
print("Maximum Penalty Minutes:", max_pen)
# Finding the minimum assists
min_assists = np.min(player_stats[:, 1])
print("Minimum Assists:", min_assists)
# Calculating the total games played for all players
total_games= np.sum(player_stats[:, 4])
print("Total Games Played By Players:", total_games)
```
---
## Pandas
- Library for working with tables of data (not at scale!)
- Organize, clean, analyze data easily
- Can read files
---
## Pandas Example
```py
import pandas as pd
# Create a DataFrame
data = {
    'Date': ['2025-02-15', '2025-02-16', '2025-02-19', '2025-02-23', '2025-02-25'],
    'Team': ['Steelers', 'Eagles', 'Jets', 'Eagles', 'Steelers'],
    'Opponent': ['Ravens', 'Cowboys', 'Ravens', 'Giants', 'Dolphins'],
    'Points Scored': [30, 28, 54, 21, 28],
    'Points Allowed': [14, 16, 35, 6, 40]
}
df = pd.DataFrame(data)
# Calculate a new column: Point Differential
df['Point Differential'] = df['Points Scored'] - df['Points Allowed']
print("\nDataFrame with Point Differential:\n", df)
# Filter the DataFrame to show only Eagles games
eagles_games = df[df['Team'] == 'Eagles']
print("\nEagles Games:\n", eagles_games)
# Filter for games where the point differential is greater than 14
high_scoring_games = df[df['Point Differential'] > 14]
print("\nHigh Scoring Games (Point Differential > 14):\n", high_scoring_games)
# Calculate the average points scored by the Eagles
average_eagles_points = df[df['Team'] == 'Eagles']['Points Scored'].mean()
print("\nAverage Points Scored by the Eagles:", average_eagles_points)
# Group by team and calculate the average points scored
average_points_by_team = df.groupby('Team')['Points Scored'].mean()
print("\nAverage Points Scored by Team:\n", average_points_by_team)
```
---
## Matplotib and Seaborn
---
## Maplotlib and Seaborn Example
```py
# Using the data from above
# Create a bar chart using Matplotlib
import matplotlib.pyplot as plt
import seaborn as sns
plt.figure(figsize=(8, 6))  # Adjust figure size
plt.bar(average_points_by_team.index, average_points_by_team.values)
plt.xlabel("Team")
plt.ylabel("Average Points Scored")
plt.title("Average Points Scored by Team")
plt.savefig("my_plot1.png")
plt.show()

# Create a scatter plot
plt.figure(figsize=(8, 6))
plt.scatter(df['Points Scored'], df['Points Allowed'])
plt.xlabel("Points Scored")
plt.ylabel("Points Allowed")
plt.title("Points Scored vs. Points Allowed")
plt.savefig("my_plot2.png")
plt.show()
```
---
<table>
  <tr>
    <td><img src="my_plot1 (1).png"></td>
    <td><img src="my_plot2.png"></td>
  </tr>
</table>

---
# Thank you for having me!

# Acknowledgements

- Thank you to Dr. Yan for the wonderful opportunity to teach you all

---

# 

# Email me at matthew.venzie@uconn.edu if you have any questions!
