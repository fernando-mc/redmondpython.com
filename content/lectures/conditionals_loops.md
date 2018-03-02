# Title

# Schedule

# Overview

# Basic Syntax & Rules

## Conditional Branching

## For Loops

## While Loops

# Utility Functions

# Example 1

```py
# Craps Roller
# Demonstrates random number generation

import random

# generate random numbers 1 - 6

count = 0
numcount=0
targ = 4

while count < 100:
    die1 = random.randint(1, 6)
    die2 = random.randrange(6) + 1
    if die1 == targ or die2 == targ:
        numcount+=1
    total = die1 + die2
    print("You rolled a", die1, "and a", die2, "for a total of", total)
    count+=1

print("You rolled a", die1, "and a", die2, "for a total of", total)
print(targ)
input("\n\nPress the enter key to exit.")
```

# Example 2

```py
# Password
# Demonstrates the if statement

print("Welcome to System Security Inc.")
print("-- where security is our middle name\n")

name = input("Enter your name: ")
password = input("Enter your password: ")

if password == name:
    print("You really shouldn't use your name as your password.")

if password == "secret":
    print("Access Granted")

input("\n\nPress the enter key to exit.")

```

# Example 3

```py
# Counter
# Demonstrates the range() function

print("Counting:")
for i in range(10):
    print(i, end=" ")

print("\n\nCounting by fives:")
for i in range(0, 50, 5):
    print(i, end=" ")

print("\n\nCounting backwards:")
for i in range(10, 0, -1):
    print(i, end=" ")

input("\n\nPress the enter key to exit.\n")
```

# Example 4

```py
# Finicky Counter
# Demonstrates the break and continue statements

count = 0
while True:
    count += 2
    if count > 100:
       break
    if count == 94 or count==96 or count == 98:
        continue
    print(count)

input("\n\nPress the enter key to exit.")
```

# Review of Key Points

# Exercises
