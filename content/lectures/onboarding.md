# Redmond Python Onboarding

## Overview

Welcome!

If you are reading this page, you have expressed an interest in attending the Redmond Python Meetup. The Redmond Python Meetup is for *everyone*--from new programmers to experienced developers.

Experienced programmers can probably go through this page without assistance, as a lot of the concepts will be familiar.

If you're brand new to Python or programming in general, we encourage you to come to a meetup for a guided onboarding session and complete these instructions with a teacher's assistant present to help with any obstacles you might encounter or answer any questions you might have.

### What's on this page?

Regardless of your skill level, this page will teach you the following:

- How to install Python on your computer
- How to use the Python Interpreter and input basic commands
- How to write and manipulate basic Python data types and applications

### About Python

Python is an easy-to-write, easy-to-read interpreted scripting language. "Hello world!" looks like this:

```py
>>> print("Hello world!")
Hello world!
```

Here's a more complex example application that sends an email which does the following:

1. Import some code in an external module (code we didn't write, but are nevertheless using).
2. Create an SMTP object to connect to a server.
3. Log in to the server.
4. Create our message.
5. Send the message.

```py
import smtplib
server = smtplib.SMTP('smtp.gmail.com', 587)
server.login("youremailusername", "password")
msg = "/nHello!"
server.sendmail("you@gmail.com", "yourFriend@hotmail.com", msg)
```
You don't need to understand this syntax at this time. The purpose of this example is simply to show you what you can accomplish in a few lines of Python code, which may take dozens of lines in other programming languages.

### Basic Python Features

Like any programming language, there's a lot to it. But the following principals are the main ones:

- **Python is open source**: Anyone can see all of the underlying code and can contribute to the code base.
- **Python is object-oriented**: Everything in Python is an object.
- **Python is platform-independent**: You can write an application on one operating system and run it on another.
- **Python has a minimalist design philosophy**: This emphasizes cleanliness and readability, with minimal semicolons and brackets.

### What can you do with Python?

The sky is the limit, but you can quickly:

  - Interact with files on your computer
  - Automate tasks as part of a workflow
  - Scrape data off a website
  - Build and deploy REST APIs
  - Build games
  - Interact with cloud services (AWS, Azure, Google, etc.)

# Setup

## Installing Python

Let's get Python installed on your computer.

First, there are two major versions of Python: Python2 and Python3. Python2 is retiring in 2020, and Python3 adds some improvements and new syntax, so we'll be using Python3.

You might already have one of these versions installed on your computer. Let's check:

1. Open a terminal or command prompt.
    - WIN: Start Menu > Command Prompt.
    - MAC/Linux: Application > Terminal.
2. Type `python` and hit **ENTER**. Do you see something like this? It means you have Python installed.
    ```bash
    Python 3.6.4 (default, Jan  3 2018, 12:27:09)
    [GCC 4.2.1 Compatible Apple LLVM 9.0.0 (clang-900.0.39.2)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>>
    ```
If you get an error, you probably need to install Python. See:

- [Windows](/setupwindows)
- [MacOS](/setupmac/)
- [Linux](/setuplinux/)

## Using the Python Interpreter

Now that we have Python installed, let's open the Python interpreter. The interpreter is where we'll be entering  Python code as we get started:

1. Open a terminal or command prompt like you did in the previous section.
2. Type `python` and hit **ENTER**.

Your prompt should look something like (if you don't, let a TA know):
```
Python 3.6.4 (default, Jan  3 2018, 12:27:09)
[GCC 4.2.1 Compatible Apple LLVM 9.0.0 (clang-900.0.39.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
You'll know you're in the interpreter when you see this prompt:
```
>>>
```
This means the Python interpreter is ready for your input. We can just type Python code directly into this prompt and it will run. Note that as you go through this tutorial, you'll see code samples like this:
```
>>> a = "Hello"
```

This means that you can type this line in at the `>>>` prompt. Simply enter the line of code, hit **Return** or **Enter** after every line you enter, and note the output (although sometimes there won't be any!).

>**Tip**: Don't copy and paste commands -- type them out. You'll learn far more if you take the time to type everything yourself.

To exit the interpreter:

1. Type `exit()` or hit `ctrl+d` to exit the Python interpreter and return to the computer's terminal.
2. Now, reopen the Python interpreter. A key point here is that everything that you entered in that previous Python interpreter session is **lost** between sessions. **The data does NOT persist**.

For now, we'll just be working with Python via the interpreter while we learn the basics. We'll show you later how to write lines of code in a file and run the script at the command line.

<!-- Commenting out for now, let's use this later

# Interactive Mode vs. Script Mode

There are two "modes" in which we can run Python. Open the interpreter again by running:
```
$ python
```
This is "Interactive Mode." This means we're feeding lines directly into the Python interpreter and it's interpreting the code live.

We'll run larger scripts later in "Script Mode." In that mode, you'll put your code in a file and pass it at the command line like this:
```
$ python myScript.py
```
For now, let's stick with Interactive Mode. -->

# Getting Started

## Basic Operations

Let's do some basic operations in Python to teach you how to interact with the Python interpreter.

1. Open the Python interpreter like we showed you in the previous section.
2. Type the following lines, noting the output:
  ```py
  >>> 2 + 4
  >>> 5 - 1
  >>> 3 * 4
  >>> 10 / 2
  ```
  This is how easy it is to interact with the interpreter. This also introduces you to some basic math operations available to you in Python like addition, subtraction, etc. We'll expand on this later.

  Now try these:
  ```py
  >>> 2+4
  >>> 5-1
  >>> 3*4
  >>> 10/2
  ```
  Same operations. Note that the whitespace between values, in this case, doesn't matter. `2+4` is the same as `2 + 4`.

## Variables

Let's introduce variables. Variables are used to store values--numbers, text, lists, etc., so that we can reference these variables later in our application.

Let's create a few variables that store some simple numbers. We'll use the `=` symbol as our assignment operator.
```py
>>> x = 4
>>> y = 2
>>> print(x + y)
```
Above, we assigned the number 4 to the variable "x" and the number 2 to "y". We then called the "print" function to print the sum. Note that we don't have to declare our variables as "integers." Python will assign the type automatically when we run our program ("at runtime").

Numbers are great, but try entering some strings of text, replacing your name below:
```py
>>> name = "Your Name"
>>> print(name)
>>> fav_food = 'Pasta'
>>> print(fav_food)
>>> long_multiline_string = """When in the Course of human events it becomes necessary for one people to dissolve the political bands which have connected them with another and to assume among the powers of the earth, the separate and equal station to which the Laws of Nature and of Nature's God entitle them, a decent respect to the opinions of mankind requires that they should declare the causes which impel them to the separation."""
>>> print(long_multiline_string)
```
Notice the use of quotes--single, double, or triple quotes are acceptable in Python. Just be consistent! To keep things simple, we'll use double quotes and all of our variables will start with a lowercase letter for now. We'll be expanding on variables and functions later.

>*Remember*: Once you close the interpreter, all of this data is lost.

## Numbers

There are two number data types in Python 3:

- **integers**: Whole numbers with no decimal point (e.g. 1, 2, -504803).
- **floats**: Written with a decimal point dividing the integer and fractional parts (e.g. .5, 842.32, .000238923).

### Math

Math in Python looks a lot like math with a calculator.

#### Addition

```py
>>> 2 + 2
>>> 1.65 + 2.15
>>> 2 + 1.65
```

#### Subtraction

```py
>>> 12 - 5
>>> 45.9 - 25.3
>>> 2 - -4
```

#### Multiplication

Multiplication uses the * (asterisk or star) symbol.
```py
>>> 6 * 7
>>> 5.6 * 4.3
>>> 6 * -5
```

#### Division

Division uses the / symbol.
```py
>>> 12/3
>>> 16/5
>>> 10/-5
```

> **Note**: If you’ve used Python 2, you’ll see that division works differently in Python 3. Python 2 uses floor division for integers, meaning it will return only the whole number part of the answer. Python 3 performs true division, returning the real or true value of the division.

To perform floor division in Python 3, use the following syntax:
```py
>>> 16//5
>>> 50//4
```

#### Modulus

Thinking back to long division that you may have learned in school, the modulus is the “remainder” after performing division. It uses the % symbol.
```py
>>> 16%5
>>> 50%4
```

#### Order of Operations

Order of operations works just like you learned in math class - Parentheses, Exponents, Multiplication, Division, Addition, Subtraction.
```py
>>> 5 + 4 * 3
>>> (5 + 4) * 3
```
> **PAUSE**: We've just covered a lot! Using the interpreter, variables, entering basic data types, doing some basic math....questions? Ask a TA!

## Booleans

So far, the code we've written has been *unconditional*: no choice is getting made--all of the code runs. Python has another data type called a **boolean** that is helpful for writing code that makes decisions. Booleans hold two values: `True` and `False`.

Re-open the Python interpreter and try typing these:
```py
>>> True
>>> type(True)
>>> False
>>> type(False)
>>> true
>>> false
```

You can test if Python objects are equal or unequal. The result is a boolean. Try typing these expressions in your Python console:

```py
>>> 0 == 0
>>> 1 == 0
>>> 54 = 42
```

Remember, use `==` to test for equality. Recall that `=` is used for assignment of a variable to a value. This is an important idea and can be a source of bugs until you get used to it: `=` is assignment, `==` is comparison.

Use `!=` to test for inequality:

```py
>>> "a" != "a"
>>> "a" != "A"
```
`<`, `<=`, `>`, and `>=` have the same meaning as in math class. The result of these tests is a boolean:

```py
>>> 1 > 0
>>> 2 >= 3
>>> -1 < 0
>>> .5 <= 1
```

You can check for containment with the `in` keyword, which also results in a boolean:
```py
>>> "H" in "Hello"
>>> "X" in "Hello"
```
Or check for a lack of containment with `not in`:
```py
>>> "a" not in "abcde"
>>> "Chicago" not in "Philadelphia Python Workshop"
```
## Operators

We just introduced some operators that let us further manipulate our data. We've outlined some (not all) of the Python operators in the following tables:

### Assignment Operators

|Operator|Description|Example|
|:----:|---|---|
|`=`|Assigns values from right side operands to left side operand|`c = a + b` assigns value of `a + b` into `c`|
|`+=` Add AND |Adds right operand to the left operand and assign the result to left operand|`c += a` is equivalent to `c = c + a`|
|`-=` Subtract AND|Subtracts right operand from the left operand and assign the result to left operand|`c -= a` is equivalent to `c = c - a`|
|`*=` Multiply AND|Multiplies right operand with the left operand and assign the result to left operand|`c *= a` is equivalent to `c = c * a`|
|`/=` Divide AND|Divides left operand with the right operand and assign the result to left operand|`c /= a`  is equivalent to `c = c / a`|
|`%=` Modulus AND|Calculates modulus using two operands and assign the result to left operand|`c %= a` is equivalent to `c = c % a`|
|`**=` Exponent AND|Performs exponential calculation on operators and assign value to the left operand|`c **= a` is equivalent to `c = c ** a`|
|`//=` Floor Division|Performs floor division on operators and assign value to the left operand |`c //= a` is equivalent to `c = c // a`|

Exercise:
```py
>>> a = 21
>>> b = 10
>>> c = 0
>>> c = a + b
>>> c
>>> c += a
>>> c
>>> c *= a
>>> c
>>> c /= a
>>> c
>>> c = 2
>>> c %= a
>>> c
>>> c **= a
>>> c
>>> c //= a
>>> c
```

### Comparison Operators

Assume `a = 5` and `b = 10`.

|Operator|Description|Example|
|:---:|---|---|
|`==`|If the values of two operands are equal, then the condition becomes true.|`a == b` evaluates to false.|
|`!=`|If values of two operands are not equal, then condition becomes true.|`a != b` is true.|
|`>`|If the value of left operand is greater than the value of right operand, then condition becomes true.|`a > b` is not true.|
|`<`|If the value of left operand is less than the value of right operand, then condition becomes true.|`a < b` is true.|
|`>=`|If the value of left operand is greater than or equal to the value of right operand, then condition becomes true.|`a >= b` is not true.|
|`<=`|If the value of left operand is less than or equal to the value of right operand, then condition becomes true.|`a <= b` is true.|

> **Key Point**: `=` assigns a value, and `==` tests for equality.

Exercise:
```py
>>> a = 5
>>> b = 10
>>> a == b
>>> a != b
>>> b = 5
>>> a == b
>>> a != b
```

### Logical Operators

|Operator|Description|Example|
|:---:|---|---|
|`and`|If both the operands are true then condition becomes true.|`x>4 and y<5`|
|`or`|If any of the two operands are non-zero then condition becomes true.|`x>4 or y<5`|
|`not`|Used to reverse the logical state of its operand.|`not(x and y)`|

### Identity Operators

|Operator|Description|Example|
|:---:|---|---|
|`is`|Evaluates to true if the variables on either side of the operator point to the same object.|See below.|
|`is not`|Evaluates to false if the variables on either side of the operator point to the same object.|See below.|

Exercise:
```py
>>> a = 1
>>> b = 1
>>> a is b
>>> b = 2
>>> a is b
```

> **PAUSE**: Booleans and operators, combined with everything we've learned thus far, make up a large portion of what you will be doing as you start out with Python. Questions? Ask a TA!

## Conditional Branching

Now that we know how to check if something is `True` or `False` using booleans and operators, we can use "conditional branching" to make Python execute commands on a conditional basis.

```py
if 6 > 5:
     print("Six is greater than five!")
```

This is the first piece of Python we've written that crosses multiple lines, and the way to enter it at a Python interpreter's prompt is a little different.

1. Open the interpreter.
2. Type `if 6 > 5:`, and hit `ENTER`. The next line will have `...` as a prompt, instead of the usual `>>>`. This is Python telling us that we are in the middle of a code block, and so long as we indent our code it should be a part of this code block.
3. Type 4 spaces, type `print("Six is greater than five!")`, and then hit `enter` to end the line.
4. Finally, hit `enter` again to tell Python you are done with this code block. All together, it will look like this:

```py
>>> if 6 > 5:
...      print("Six is greater than five!")
Six is greater than five!
```

So what's going on here? When Python encounters the `if` keyword, it evaluates the expression following the keyword and before the colon. If that expression is `True`, Python executes the code in the indented code block under the `if` line. If that expression is `False`, Python skips over the code block.

In this case, because 6 really is greater than 5, Python executes the code block under the if statement, and we see "Six is greater than five!" printed to the screen. Guess what will happen with these other expressions, then type them out and see if your guess was correct:

```py
>>> if 0 > 2:
...     print("Zero is greater than two!")
```
Another:
```py
>>> if "banana" in "bananarama":
...    print("I miss the 80s.")
```

**more choices: if and else**

You can use the `else` keyword to execute code only when the `if` expression isn't `True`:

```py
>>> sister_age = 15
>>> brother_age = 12
>>> if sister_age > brother_age:
...    print("sister is older")
...else:
...    print("brother is older")
```

Like with `if`, the code block under the `else` statement must be indented so Python knows that it is a part of the `else` block.

**compound conditionals: `and` and `or`**

We've been testing single conditions, but we can also test multiple conditions that result in execution of some code. You can check multiple expressions together using the `and` and `or` logical operators.

- If two expressions are joined by an `and`, they **both** have to be `True` for the overall expression to be `True`.
- If two expressions are joined by an `or`, as long as **at least one** is `True`, the overall expression is `True`.

Try typing these out and see what you get:

```py
>>> 1 > 0 and 1 < 2
>>> 1 < 2 and "x" in "abc"
>>> "a" in "hello" or "e" in "hello"
>>> 1 <= 0 or "a" not in "abc"

Guess what will happen when you enter these next two examples, and then type them out and see if you are correct. If you have trouble with the indenting, call over a staff member and practice together. It is important to be comfortable with indenting. Indenting is a crucial part of the syntax of Python.

```py
>>> temperature = 32
>>> if temperature > 60 and temperature < 75:
...    print("It's nice and cozy in here!")
... else:
....    print("Too extreme for me.")
```
One more:
```py
>>> hour = 11
>>> if hour < 7 or hour > 23:
...    print("Go away!")
...    print("I'm sleeping!")
... else:
...    print("Welcome to the cheese shop!")
...    print("Can I interest you in some choice gouda?")
```

You can have as many lines of code as you want in if-else block, just make sure to indent them so Python knows they are a part of the block.

**even more choices: elif and else**

If you have more than two cases, you can use the `elif` keyword to check more cases. Think of `elif` as Python-speak for else if. You can have as many `elif` cases as you want. Python will go down the code checking each `elif` until it finds a `True` condition or reaches the default `else` block.

```py
>>> sister_age = 15
>>> brother_age = 12
>>> if sister_age > brother_age:
...    print("sister is older")
... elif sister_age == brother_age:
...    print("sister and brother are the same age")
... else:
...    print("brother is older")
```

You don't have to have an `else` block if you don't need it. That just means there isn't default code to execute when none of the `if` or `elif`conditions are `True`:

```py
>>> color = "orange"
... if color == "green" or color == "red":
...    print("Christmas color!")
... elif color == "black" or color == "orange":
...    print("Halloween color!")
... elif color == "pink":
...    print("Valentine's Day color!")
```

If color had been "purple", that code wouldn't have printed anything. Remember that `=` is for assignment and `==` is for comparison.

## Functions

Functions are how we perform actions on our data. We've been using a function a lot so far: `print()`. Calling a function is as easy as calling the function name and putting a variable or value between round brackets like we've been doing.

Try the following:
```py
>>> a = "The number 3: "
>>> b = 3
>>> type(a)
>>> type(b)
>>> print(str, a)
```

We can pass multiple "arguments" to our functions as shown above. For now, remember that there are three kinds of functions:

- The built-in kind that come with Python (e.g.`print()`)
- The kind we write
- The kind that other people wrote that we can borrow (by importing their code modules and using them in our programs)

### Writing Our Own Function

```py
>>> def myFirstFunction():
...     print("Hello!")
```

We just wrote our first function. Now call it:
```py
>>> myFirstFunction()
```
Our function takes no arguments. Let's write one that passes an argument:

```py
>>> def mySecondFunction(name):
...     print("Hello", name)
```
Now let's run it:
```py
>>> mySecondFunction("Steven")
```

You just called a function and passed an argument.

### Utility Functions

We'll gradually expand your knowledge of functions, but for now we'll introduce a few cool functions that can help us with numerical types and strings.

#### For Numbers

We can convert between numerical types with ease:

Converts 5.0 to 5:
```py
>>> int(5.0)
```
Converts 4 to 4.0:
```py
>>> float(4)
```
As shown above, we can use the built-in `type()` function to determine the type of a given variable.

Convert from float to int:
```py
>>> x = 5.5
>>> x
>>> type(x)
>>> x = int(x)
>>> x
>>> type(x)
```
Convert from int to float:
```py
>>> y = 4
>>> y
>>> type(y)
>>> y = float(y)
>>> y
>>> type(y)
```
#### For Strings

`upper()` and `lower()` are handy:
```py
>>> str = "my string"
>>> str.upper()
>>> str2 = "MY STRING"
>>> str2.lower()
```

## Additional Concepts

### Tracebacks

When you make a mistake and try to run your program, Python will generate a traceback to tell you what went wrong. By now, you may have seen a few of these!

Open the interpreter and run:
```py
>>> a = "John"
>>> a + 2
```
We see the following error:
```py
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: must be str, not int
```
The above traceback tells us the following:

- The name of the file where the error occurred: "<stdin>" (means that the error occurred on input)
- The line number containing the error: 1
- The name of the module (if applicable, which it's not here)
- The error type: `TypeError`
- What we did wrong: We tried to perform an operation on one data type that Python wouldn't allow.

Tracebacks are invaluable when trying to diagnose why something won't run.

### Comments

Comments help us communicate with teammates about what our functions are doing. We'll use them more when we start running applications in Python files. For now, just know that when you see the following syntax, it's a comment.

Single line comment:
```py
# Here is a comment in python! It's great and is ignored when the program runs!
name = "Your Name"
print(name)
print("Your Name")
```
This is an in-line comment:
```py
name = "Your Name"
print(name) # Here is an in-line comment!
print("Your Name")
```
Here is a multiline comment that uses three apostrophes above and below the comment:
```py
'''
This is a multiline comment for longer comments that you want to put in your code. Commenting code is important when you're sharing code with multiple people. Because we're using the three apostrophes, we can make this comment as looooooooooong as we want!
'''
name = "Your Name"
print(name)
print("Your Name")
```
### TBD

# Additional Resources

- [Python Guide for Beginners - Non-Programmers](https://wiki.python.org/moin/BeginnersGuide/NonProgrammers)
- [Python Guide for Beginners - Programmers](https://wiki.python.org/moin/BeginnersGuide/Programmers)
- [Coding Bat](https://www.codingbat.com/python)
- [Hacker Rank](https://hackerrank.com)
- [Try Git](https://www.codeschool.com/courses/try-git)
