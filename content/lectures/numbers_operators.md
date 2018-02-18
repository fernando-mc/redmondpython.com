# Numbers and Operators

# Schedule

- Overview
- Basic Syntax & Rules
- Math
- Operators
- Utility Functions
- Examples
- Review
- Exercises
- Additional Resources

# Overview

Number data types store numeric values. They are immutable data types, means that changing the value of a number data type results in a new object.

# Basic Syntax & Rules

There are two numerical types that we will learn about:

- **integers**: Positive or negative whole numbers with no decimal point.
- **floats**: Written with a decimal point dividing the integer and fractional parts.

## Math

Math in Python looks a lot like math with a calculator.

### Addition

```
>>> 2 + 2
>>> 1.65 + 2.15
>>> 2 + 1.65
```

### Subtraction

```
>>> 12 - 5
>>> 45.9 - 25.3
>>> 2 - -4
```

### Multiplication

Multiplication uses the * (asterisk or star) symbol.
```
>>> 6 * 7
>>> 5.6 * 4.3
>>> 6 * -5
```

### Division

Division uses the / symbol.
```
>>> 12/3
>>> 16/5
>>> 10/-5
```

> **Note**: If you’ve used Python 2, you’ll see that division works differently in Python 3. Python 2 uses floor division for integers, meaning it will return only the whole number part of the answer. Python 3 performs true division, returning the real or true value of the division.

To perform floor division in Python 3, use the following syntax:
```
>>> 16//5
>>> 50//4
```

### Modulus

Thinking back to long division that you may have learned in school, the modulus is the “remainder” after perfoming division. It uses the % symbol.
```
>>> 16%5
>>> 50%4
```

### Order of Operations

Order of operations works just like you learned in math class - Parentheses, Exponents, Multiplication, Division, Addition, Subtraction.
```
>>> 5 + 4 * 3
>>> (5 + 4) * 3
```
### Storing Numbers in Variables

A lot of work gets done in Python using variables. A variable consists of an identifier (the variable’s name) and a value stored in the variable – any kind of value, not just a number. We'll talk more about valuables later, but this is how numbers are stored in variables:
```
>>> x = 1
>>> x
>>> y = 2.5
>>> y
```
Note the `=` sign. This leads us to an important topic.

# Operators

## Assignment

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

### Assignment Operator Exercise

Enter the following in the interpreter:
```
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

## Comparison

Assume `a = 5` and `b = 10`.

|Operator|Description|Example|
|:---:|---|---|
|`==`|If the values of two operands are equal, then the condition becomes true.| `a == b` evaluates to false.|
|`!=`|If values of two operands are not equal, then condition becomes true.|`a != b` is true.|
|`>`|If the value of left operand is greater than the value of right operand, then condition becomes true.|`a > b` is not true.|
|`<`|If the value of left operand is less than the value of right operand, then condition becomes true.|`a < b` is true.|
|`>=`|If the value of left operand is greater than or equal to the value of right operand, then condition becomes true.|`a >= b` is not true.|
|`<=`|If the value of left operand is less than or equal to the value of right operand, then condition becomes true.|`a <= b` is true.|

> **Key Point**: `=` assigns a value, and `==` tests for equality.

Exercise:
```
>>> a = 5
>>> b = 10
>>> a == b
>>> a != b
>>> b = 5
>>> a == b
>>> a != b
```

## Logical

|Operator|Description|Example|
|:---:|---|---|
|`and`|If both the operands are true then condition becomes true.|`x>4 and y<5`|
|`or`|If any of the two operands are non-zero then condition becomes true.|`x>4 or y<5`|
|`not`|Used to reverse the logical state of its operand.|`not(x and y)`|

## Identity

|Operator|Description|Example|
|:---:|---|---|
|`is`|Evaluates to true if the variables on either side of the operator point to the same object.|See below.|
|`is not`|Evaluates to false if the variables on either side of the operator point to the same object.|See below.|

Exercise:
```
>>> a = 1
>>> b = 1
>>> a is b
>>> b = 2
>>> a is b
```

## Membership

|Operator|Description|Example|
|:---:|---|---|
|`in`|Evaluates to true if it finds a variable in the specified sequence and false otherwise.|x in y is true if x is found in sequence y|
|`not in`|Evaluates to true if it does not finds a variable in the specified sequence and false otherwise.|x not in y evaluates to true if x is not in sequence y|

You don't need to understand lists or the loop structure here--this is just to demonstrate how `in` and `not in` can be used:

```py
a = 5
b = 10
list = [1, 2, 3, 4, 5 ];

if ( a in list ):
   print("a is in your list!")
else:
   print("a is not in your list!")

if ( b not in list ):
   print("b is not in your list!")
else:
   print("b is in your list!")
```

# Utility Functions

We'll talk more about functions in a different lecture, but for now we'll introduce a few small functions that can help us with numerical types. We can convert between numerical types with ease:

Converts 5.0 to 5:
```
>>> int(5.0)
```
Converts 4 to 4.0:
```
>>> float(4)
```
We can also use the handy built-in `type()` function to determine the type of a given variable.

Convert from float to int:
```
>>> x = 5.5
>>> x
>>> type(x)
>>> x = int(x)
>>> x
>>> type(x)
```
Convert from int to float:
```
>>> y = 4
>>> y
>>> type(y)
>>> y = float(y)
>>> y
>>> type(y)
```

# Example 1

TBD

# Example 2

TBD

# Example 3

TBD

# Review of Key Points

- You can use the Python interpreter to do basic math.
- There are many different operators available to you.
- Important: `=` assigns a value, and `==` tests for equality.
- We can convert between integers and floats using `int()` and `float()`
- We can check the type of any value or variable by using `type()`

# Exercises

TBD

# Additional Resources

TBD
