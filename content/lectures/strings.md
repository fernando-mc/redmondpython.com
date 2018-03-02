# Title

# Schedule

# Overview

# Basic Syntax & Rules

## quotes

# Utility Functions

# Example 1

Some basic operations:

```py
# Quotation Manipulation
# Demonstrates string methods
# quote from IBM Chairman, Thomas Watson, in 1943

quote = "I think there is a world market for maybe five computers."
name = "Enter your name here"

print("Original quote:")
print(quote)
print(name.upper())
print(name.lower())
print(name.title())
print(name.replace("EnterYourLastNameHere","EnterTheFirstLetterOfYourLastNameHere"))
print("In uppercase:")
print(quote.upper())
print("In lowercase:")
print(quote.lower())
print("As a title:")
print(quote.title())
print("With a minor replacement:")
print(quote.replace("five", "millions of"))
print("Original quote is still:")
print(quote)
input("Press the enter key to exit.")
```

# Example 2

```py
# Silly Strings
# Demonstrates string concatenation and repetition

print("You can concatenate two " + "strings with the '+' operator.")

print("\nThis string " + "may not " + "seem terr" + "ibly impressive. " \
      + "But what " + "you don't know" + " is that\n" + "it's one real" \
      + "l" + "y" + " long string, created from the concatenation " \
      + "of " + "twenty-two\n" + "different strings, broken across " \
      + "six lines." + " Now are you" + " impressed? " + "Okay,\n" \
      + "this " + "one " + "long" + " string is now over!")

print("\nIf you really like a string, you can repeat it.  For example,")
print("who doesn't like pie?  That's right, nobody.  But if you really")
print("like it, you should say it like you mean it:")
print("Pie" * 10)

input("\n\nPress the enter key to exit.")
```

# Example 3

```py
# Trust Fund Buddy - Bad
# Demonstrates a logical error

print(
"""
            Trust Fund Buddy

Totals your monthly spending so that your trust fund doesn't run out
(and you're forced to get a real job).

Please enter the requested, monthly costs.  Since you're rich, ignore pennies
and use only dollar amounts.

"""
)

car =  input("Lamborghini Tune-Ups: ")
rent = input("Manhattan Apartment: ")
jet = input("Private Jet Rental: ")
gifts = input("Gifts: ")
food = input("Dining Out: ")
staff = input("Staff (butlers, chef, driver, assistant): ")
guru = input("Personal Guru and Coach: ")
games = input("Computer Games: ")

total = car + rent + jet + gifts + food + staff + guru + games

print("\nGrand Total:", total)

input("\n\nPress the enter key to exit.")
```

# Example 4

```py
# Word Problems
# Demonstrates numbers and math

print("If a 2000 pound pregnant hippo gives birth to a 100 pound calf,")
print("but then eats 50 pounds of food, how much does she weigh?")
input("Press the enter key to find out.")
print("2000 - 100 + 50 =", 2000 - 100 + 50)

print("\nIf an adventurer returns from a successful quest and buys each of")
print("6 companions 3 bottles of ale, how many bottles are purchased?")
input("Press the enter key to find out.")
print("6 * 3 =", 6 * 3)

print("\nIf a restaurant check comes to 19 dollars with tip, and you and")
print("your friends split it evenly 4 ways, how much do you each throw in?")
input("Press the enter key to find out.")
print("19 / 4 =", 19 / 4)

print("\nIf a group of 4 pirates finds a chest full of 107 gold coins, and")
print("they divide the booty evenly, how many whole coins does each get?")
input("Press the enter key to find out.")
print("10 // 3 =", 10 // 3)

print("\nIf that same group of 4 pirates evenly divides the chest full")
print("of 107 gold coins, how many coins are left over?")
input("Press the enter key to find out.")
print("10 % 3 =", 10 % 3)

input("\n\nPress the enter key to exit.")
```

# Review of Key Points

# Exercises
