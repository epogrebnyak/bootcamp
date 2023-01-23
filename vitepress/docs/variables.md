# Variables

## What is a variable?

> A variable is a name that is bound to a value.

A variable is an identifier that is used to refer to a specific value stored in the memory of a computer.
The variable serves as a kind of a "nickname" or an "alias" for the value.

The value can be of various types, such as a number, a string, or some other object, 
and it can be passed to various parts of the program, modified or reassigned 
during the execution of the program.

### Questions and excercises

1. Does the variable name always remain the same throughout the program?
1. Does the variable value always remain the same throughout the program?

## Variable assignment

> `x=1` is a perfect variable assignment.

A variable get assigned a value with `=` operator.
The expression to the right of the = operator is evaluated first, and the result is then assigned to the variable name on the left.

```python
r = 2.5
area = 3.1415 * r ** r
print(area)
```

**Math vs programming**. Concept of variables in programming and mathematics slightly differ.
In mathematics, a variable is often used to represent an unknown value that needs to be derived by solving an equation.
In programming the variable value is known after assignment and can be used in further computations.

```python
x = 1        # assignment of value of 1 to variable x
x = x + 1    # new assignment to variable x, not an equation
print(x)
```

To highlight the difference, some other programming languages use 
`:=` (Pascal) or `<-` (R) as an assignment operator.

```pascal
x := 1   // assignment of value 1 to variable x in Pascal 
```

```R
x <- 1   # assignment of value 1 to variable x in R
```

## Changing variables

> In Python all variables are mutable.

After initially assigning a value to a variable in Python you can reassign
a new value to it.

```python 
favourite_food = "My favourite food is mushroom soup."
print(favourite_food)

# later in the same program

favourite_food = "Now my favourite food is apple pie."
print(favourite_food)
```
A typical situation where a variable changes is some sort of a counter.

```python
string = ("Now my favourite food is apple pie, " +
          "but I liked mushroom soup before.")
letter = "e"
counter = 0
for s in string:
   if s == letter: 
      counter = counter + 1
print("We searched for letter:", letter)
print("In the following string:", string)
print("The letter was found", counter, "times")
```

### Questions and excercises

1. In code example above screw the counter to wrong starting value.
1. Think of different and better variable names instead of `string`, `s`, `letter` and `counter` in code above.
1. Count number of spaces in `string` and print the result.
1. What other variable does seem to change other than `counter`?
1. Try removing `if` from code. How did the meaning of code change? What else needs to be changed in this code without `if`?
1. Can we adapt this code to search for letter combinations? (*)

## Constants and immutability

> Variables with UPPERCASE names are assumed to be constant.

**Constants.** Python does not have a concept of constants like other languages.
To indicate a constant the variable name is written with uppercase letters, but this is a
matter of convention, not a syntax rule. Python does not have a built-in mechanism 
for enforcing this convention at interpreter level.

The uppercase convention aims to improve readability of the code 
and indicates the intent of the programmer to keep the variable value unchanged. 
However, you can reassign a value to a variable even if the variable name is written 
in uppercase letters. 

```python
KM_PER_MILE = 1.6
print("One kilometer is about",  round(1/KM_PER_MILE, 2), "miles")

# ... but I want more precision!
KM_PER_MILE = 1.60934
print("One kilometer is about",  round(1/KM_PER_MILE, 2), "miles")
```

**Immutability.** In some other programming languages, variables are immutable by default, 
which means that once a value is assigned to a variable, it cannot be changed. 
To store computation results either new variables are created or a variable has to 
declared as mutable when first introduced. 

Mutable variables are flexible and perhaps simplier to write code with. 
Immutable variables also have benefits, for example they cannot be changed accidentally 
and the program behavior is more predictable.

## Variable naming in Python

> Language conventions and common sense guide variable naming.

Variable naming is not as easy at it may first sound.
While there are just a few formal syntax limitations on variable names,
picking the right name that strikes a balance between brevity
and being well-understood by people who read your code is rather difficult.
Programmers may not agree what makes a good variable name, except for trivial 
cases like `x` and `y` for coordinates on a two-dimensional plaine.

Variable naming ideas by you.com:

> 1. Choosing good variable names is an important part of writing code that is easy to read and understand.

> 2. The name of the variable should be descriptive and accurately describe what the variable holds or what it is used for.

> 3. It should be concise and include only the necessary words to clearly describe the variable. 

> 4. Additionally, it should avoid the use of acronyms and abbreviations that may be confusing or ambiguous. 

> 5. It is also important to avoid using generic terms like "data" or "value" as variable names. 

> 6. Finally, it is important to be consistent with variable naming conventions across the codebase.

## More suggestions

> What ChatGPT thought to add to this section.

If the lesson is intended for beginner programmers, it's probably best to keep the topic list simple and not go into more advanced topics like scope, debugging and best practices.

However, here are some additional topics that might be useful to include in a lesson on variables:

- The different data types that can be stored in a variable.
- Variables as function parameters.
- The scope of a variable (i.e. where in the code it can be accessed).
- How to debug variable-related errors in a program. Is `print()` ok for this?
- Best practices for using variables, such as initializing variables before use, avoiding using the same variable name for different purposes, and avoiding using hard-coded values in a program.
