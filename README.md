<h1 align="center">Python Notes</h1>

### Printing, Commenting, Debugging, String Manipulation & Variables

- Printing
- Inputting
- Commenting
- Debugging
- Name Errors
- Syntax Errors
- String Manipulation
- Variables
- Concatenation
- Indentation

**Note:** Shortcut to run program in Pycharm in windows is **Shift + F10**

In Python, the print() function is used to display output to the console.

✅ Basic Usage

`print("Hello, world!")`
Output:
Hello, world!

🧵 Printing Variables

`name = "Nagendra"`
`print("Hello,", name)`
Output:
Hello, Nagendra

🧩 Using f-strings (Python 3.6+ — Recommended)

`name = "Nagendra"`
`age = 30`
`print(f"My name is {name} and I am {age} years old.")`
Output:
My name is Nagendra and I am 30 years old.

📚 Other Formatting Options
format() method:
`print("My name is {} and I am {} years old.".format(name, age))`
% operator:
`print("My name is %s and I am %d years old." % (name, age))`

🔄 Printing Multiple Values

`print("Name:", name, "Age:", age)`

🛠️ Print with Separator or End Options

`print("A", "B", "C", sep="-")` # Output: A-B-C
`print("Line 1", end=" | ")` # Output: Line 1 | (no newline)

### Can I use both single quotes and double quotes in Python's print() function?

Yes, in Python’s print() function, you can use both single quotes ' and double quotes " to define strings — they are functionally the same.

✅ Examples:

`print("Hello, world!")`
`print('Hello, world!')`
Both print:
Hello, world!

💡 When to choose ' or ":
Use the one that makes your code more readable, especially if your string contains quotes.

Example 1: String contains single quote → use double quotes
`print("It's a sunny day.")`

Example 2: String contains double quote → use single quotes
`print('He said, "Hello!"')`

Example 3: Use escape characters if needed
`print('It\'s a sunny day.')`
`print("He said, \"Hello!\"")`

**When I run a Python program in an IDE or terminal, I see several lines in the output. What do they mean?**
When you run a Python program in an IDE or terminal, you may see several lines in the output. Let's break down each part:

🧾 Example Output:
/Users/nagendra/my_script.py
Hello, world!
Process finished with exit code 0

🔍 Explanation:
✅ 1. /Users/nagendra/my_script.py
This is the path to your Python file.

Some IDEs (like PyCharm) or editors (like VS Code) show the full path of the script you're running.

✅ 2. Hello, world!
This is your program's actual output, printed by the print() function in your script.

✅ 3. Process finished with exit code 0
This is a message from the IDE or terminal indicating that the program ran successfully.

exit code 0 means no errors occurred during execution.

Exit Code Meaning
0 Success
1+ Error occurred (non-zero value)

**Commenting**
Commenting in Python is a way to explain your code, make it more readable, and help other developers (or your future self) understand what your code is doing.

Here’s a quick guide to Python commenting:

1. Single-line comments
   Use the # symbol.

# This is a single-line comment

x = 5 # This is an inline comment

2. Multi-line comments
   Python doesn’t have a native multi-line comment syntax, but you can use multiple # symbols:

# This is a multi-line comment

# that spans more than one line

# to explain the code below

x = x + 1
Alternatively, triple-quoted strings (''' or """) are sometimes used as block comments, but they’re technically string literals and not true comments:

"""
This is a block comment.
It's not ignored by the interpreter if it's not assigned.
Use only when necessary.
""" 3. Docstrings (Documentation Strings)
Used to describe modules, functions, classes, or methods.

def add(a, b):
"""Return the sum of a and b."""
return a + b
You can access docstrings using:

help(add)
print(add.**doc**)
Best Practices:
Keep comments concise and relevant.

Don’t state the obvious. For example, avoid this:

x = 5 # Set x to 5
Use docstrings for all public functions and classes.

Update comments when code changes.

**Concatenation?**

- Concatenation means joining two or more strings (text) together.
- The String Concatenation is simply taking those separate strings of characters and merging them into one.

**🧱 Indentation in Python**
Indentation in Python refers to the spaces or tabs at the beginning of a line. It’s not optional — it defines the structure and flow of your code (like blocks in loops, functions, if-statements, etc.).

✅ Basic Rule
Use consistent indentation (usually 4 spaces per level).

Do not mix tabs and spaces.

🔍 Example 1: If Statement

```x = 10
       if x > 5:
       print("x is greater than 5")  # This line is indented
```

🔍 Example 2: Function

```def greet(name):
       print("Hello,", name)
       print("Welcome!")
```

❌ Incorrect Indentation (will cause an error)

```if x > 5:
       print("x is greater than 5") # ❌ No indentation — causes IndentationError
```

📌 Common Indentation Errors
IndentationError: expected an indented block – You forgot to indent after if, for, def, etc.

IndentationError: unexpected indent – You added unnecessary spaces where Python didn’t expect them.

Mixing tabs and spaces – Use one or the other, not both.

**input() in Python — Getting User Input**
The input() function lets you take input from the user via the keyboard. It always returns the input as a string.

✅ Basic Syntax

`name = input("Enter your name: ")`
`print("Hello,", name)`
Output example:
Enter your name: Nagendra
Hello, Nagendra

🔁 Converting Input to Other Types
Since input() returns a string, you may need to convert it if you expect a number.
🔸 Integer Input:
`age = int(input("Enter your age: "))`
`print(f"You will be {age + 1} next year.")`

🔸 Float Input:
`price = float(input("Enter the price: "))`
`print(f"Total with tax: {price * 1.18}")`

🧪 Validating Input (Optional Best Practice)
To avoid errors, you can check input before converting:

```user_input = input("Enter a number: ")
if user_input.isdigit():
    number = int(user_input)
    print("You entered:", number)
else:
    print("That's not a valid number.")
```

<h2 align="center">Variables</h2>

**What is a Variable in Python?**
A variable is a named storage that holds data. You can use it to store, modify, and access values in your program.

📌 Think of a variable as a label for a value.

🔸 Example:
`name = "Nagendra"`

`age = 30`

`is_admin = True`

name holds a string

age holds an integer

is_admin holds a boolean

🧪 How Python Handles Variables
You don't need to declare a variable's type.

Python infers the type when you assign a value.
`x = 10` # Integer
`x = "hello"` # Now it's a string
✅ This is called dynamic typing.

🏷️ Variable Naming Rules (Syntax Rules)
Python has strict rules and conventions for naming variables.

✅ Valid Variable Names
`name = "Alice"`
`_name = "Bob"`
`name2 = "Charlie"`

❌ Invalid Variable Names
`2name = "X"` # ❌ Starts with a number
`first-name = "Y"` # ❌ Hyphen is not allowed
`class = "Z"` # ❌ Reserved keyword

📚 Rules for Naming Variables in Python
Rule Description
✅ Must start with a letter (A–Z or a–z) or an underscore \_
✅ Can contain letters, digits (0–9), and underscores
❌ Cannot start with a digit
❌ Cannot use special characters like @, #, -, .
❌ Cannot be a Python keyword (like class, for, if, etc.)
🔠 Python is case-sensitive: Name, name, and NAME are different variables

💡 Naming Conventions (PEP 8 Style Guide)
PEP 8 is Python’s official style guide.

Convention Example Used For

- lowercase_with_underscores user_name, total_price ✅ Regular variables and functions
- CamelCase UserProfile, LoginManager ✅ Class names
- \_single_leading_underscore \_temp, \_hidden 🔒 Internal use (private variables)
- **double_leading_underscore **init\_\_ 🚀 Special methods (magic methods)
- ALL_CAPS MAX_VALUE, PI Constants

🔐 Python Reserved Keywords (Cannot be Used as Variable Names)
Here are a few examples:

False, class, finally, is, return
None, continue, for, lambda, try
True, def, from, nonlocal, while
and, del, global, not, with
as, elif, if, or, yield
assert, else, import, pass
break, except, in, raise
Full list: Run help("keywords") in a Python shell.

**🧠 Summary**

- Variables store data.

- Python uses dynamic typing (no need to declare type).

- Naming must follow syntax rules.

- Use PEP 8 conventions for readability and professionalism.

## Data Types, Numbers, Operations, Type Conversion, f-Strings

**What is Subscripting in Python?**
Subscripting is the act of accessing elements inside a collection (like a string, list, tuple, dictionary, etc.) using square brackets [].

🧪 Examples of Subscripting
✅ 1. String Subscripting
`text = "Hello"`
`print(text[0])` # Output: H
`print(text[-1])` # Output: o (last character)
Strings are sequences. You can use indexes to get individual characters.

✅ 2. List Subscripting
`fruits = ["apple", "banana", "cherry"]`
`print(fruits[1])` # Output: banana
Lists are ordered, so you can access elements by their position (starting from 0).

✅ 3. Dictionary Subscripting
`person = {"name": "Nagendra", "age": 30}`
`print(person["name"])` # Output: Nagendra
In dictionaries, subscripting uses keys instead of numeric indexes.

📌 General Syntax:
`collection[index_or_key]`
For lists, tuples, strings → use index (like 0, -1, etc.)

For dictionaries → use key (like "name" or "age")

⚠️ Subscripting Errors
Error Type Example Reason
IndexError `my_list[10]` Index is out of range
KeyError `my_dict["wrong_key"]` Key doesn't exist in dictionary
TypeError `5[0]` or `None['x']` Type doesn't support subscripting

🔧 Behind the Scenes
Subscripting uses the `__getitem__()` method in Python. So when you write:

`x[0]`
It’s actually doing:
`x.__getitem__(0)`

🧠 Summary

- Subscripting = accessing elements using [ ]

- Works on strings, lists, tuples, dictionaries, etc.

- Supports positive and negative indexes

- Raises errors if used incorrectly

- Let me know if you want examples of nested subscripting or how to safely handle missing keys/indexes!

### 🧱 Python Primitive Data Types

Primitive data types are the basic building blocks of data in Python. They store simple values and are immutable (cannot be changed after creation).

🧮 1. Integer (int)
Represents whole numbers (positive, negative, or zero)

No decimal point

✅ Examples:
a = 10
b = -25
c = 0
🔍 Usage:
Counting, indexing, looping

Used in math operations: +, -, \*, //, %

🧮 2. Floating Point (float)
Represents decimal numbers

Can be written with or without a decimal point

✅ Examples:
pi = 3.14
temperature = -12.5
value = 10.0
🔍 Usage:
Precise values, measurements, percentages, etc.

Supports math operations: +, \*, /, etc.

🧾 3. String (str)
Represents textual data

Enclosed in \*\*single ' ' or double " " quotes

✅ Examples:
name = "Nagendra"
msg = 'Hello, World!'
🔍 Usage:
Display messages, user input, file names

Can be indexed, sliced, and concatenated

print(name[0]) # N
print(name + " Rao") # Nagendra Rao

✅ 4. Boolean (bool)
Represents True or False

Used in logic and conditions

✅ Examples:
is_active = True
has_permission = False
🔍 Usage:
if is_active:
print("User is active")
Behind the scenes: True is treated as 1, False as 0

🕳️ 5. NoneType (None)
Represents the absence of a value

Often used to initialize a variable that doesn't have a value yet

✅ Examples:
result = None
if result is None:
print("No result yet")

🧠 Summary Table

- Data Type Keyword Example Description
- Integer int x = 10 Whole numbers
- Float float pi = 3.14 Decimal numbers
- String str name = "Alice" Textual data
- Boolean bool flag = True Logic values True or False
- NoneType None value = None Represents absence of a value

🔍 How to Check Data Type?
Use type() function:
x = 10
print(type(x)) # <class 'int'>

### 📦 Non-Primitive Data Types in Python

These include:

List

Tuple

Set

Dictionary

1. 🧾 List (list)
   A list is an ordered, mutable (changeable) collection that allows duplicate elements.

✅ Example:
fruits = ["apple", "banana", "cherry"]
print(fruits[1]) # banana
fruits[1] = "orange" # Change banana to orange

🔍 Features:

- Maintains order

- Allows duplicates

- Can contain different data types

- Elements are accessed using indexes

✅ Common Operations:
fruits.append("grape") # Add to end
fruits.remove("apple") # Remove value
len(fruits) # Count of items

2. 📦 Tuple (tuple)
   A tuple is like a list but immutable (cannot be changed after creation).

✅ Example:
colors = ("red", "green", "blue")
print(colors[0]) # red

🔍 Features:

- Ordered

- Immutable (read-only)

- Faster than lists

- Useful for fixed collections

⚠️ Tuples cannot be modified:
colors[1] = "yellow" # ❌ Error

3. 🎯 Set (set)
   A set is an unordered, mutable collection of unique elements.

✅ Example:
unique_numbers = {1, 2, 3, 3, 2}
print(unique_numbers) # {1, 2, 3}

🔍 Features:

- No duplicates

- No order (so no indexing)

- Useful for set operations (union, intersection, etc.)

✅ Common Operations:
unique_numbers.add(4)
unique_numbers.remove(2)

4. 📚 Dictionary (dict)
   A dictionary stores data as key-value pairs.

✅ Example:
person = {"name": "Nagendra", "age": 30}
print(person["name"]) # Nagendra

🔍 Features:

- Unordered (in older versions of Python)

- Keys are unique

- Values can be any type

✅ Common Operations:
person["location"] = "India" # Add a key-value pair
del person["age"] # Remove a key

🧠 Summary Table
Type Ordered Mutable Duplicate Items Syntax Example
List ✅ ✅ ✅ ["a", "b", "c"]
Tuple ✅ ❌ ✅ ("a", "b", "c")
Set ❌ ✅ ❌ {1, 2, 3}
Dictionary ❌\* ✅ ❌ (keys only) {"key": "value"}

\*Dictionaries preserve order from Python 3.7+

1️⃣ TYPE ERROR
🔴 What is a TypeError?
A TypeError occurs when you try to perform an operation on a value of the wrong data type.

🚫 Example:
x = "5"
y = 2
print(x + y) # ❌ TypeError: can only concatenate str (not "int") to str
✅ Fix:
print(int(x) + y) # ✅ Converts string "5" to int

2️⃣ TYPE CHECKING
🧪 What is Type Checking?
Type checking is the process of verifying the data type of a variable before using it in operations.

✅ Using type():
name = "Nagendra"
print(type(name)) # <class 'str'>
✅ Using isinstance():
age = 30
print(isinstance(age, int)) # True
print(isinstance(age, str)) # False
isinstance() is safer for checking inheritance in object-oriented code too.

3️⃣ TYPE CONVERSION (TYPE CASTING)
🔄 What is Type Conversion?
Type conversion means converting a variable from one data type to another using built-in functions.

🔧 Common Conversion Functions:

- Function Converts To Example
- int(x) Integer int("10") → 10
- float(x) Float float("3.14") → 3.14
- str(x) String str(100) → "100"
- bool(x) Boolean bool(0) → False
- list(x) List list("abc") → ['a','b','c']
- stuple(x) Tuple tuple([1, 2]) → (1, 2)

🧪 Example: Type Conversion in Action
a = "25"
b = 5
result = int(a) + b
print(result) # Output: 30
⚠️ Notes:
Not all conversions are possible. For example, int("hello") will raise a ValueError.

Always validate or check types before conversion when handling user input.

🧠 Summary

- Topic Meaning Tool / Method
- Type Error Wrong operation between incompatible types Automatically raised
- Type Checking Checking data type before using type(), isinstance()
- Type Conversion Changing value from one type to another int(), float(), etc.

**🧠 What is Python Implicit Type Conversion?**
Implicit type conversion, also known as type coercion, happens automatically in Python when it converts one data type to another during an operation without requiring explicit instructions from the programmer.

✅ Key Points:
Done automatically by Python.

Happens when different data types are used in an expression.

Converts to the higher precision type to avoid data loss (e.g., int → float).

🔄 Example:
`num_int = 5` # int
`num_float = 2.5` # float

`result = num_int + num_float`

print(result) # 7.5
print(type(result)) # <class 'float'>

✅ What happened here?
Python saw int + float

It automatically converted the int (5) to a float (5.0)

Then performed the addition: 5.0 + 2.5 = 7.5

🛠 More Examples:
a = True # bool → int → 1
b = 10
print(a + b) # Output: 11

x = 10
y = 3.0
z = x / y # x is converted to float automatically
print(z) # Output: 3.333...
⚠️ Notes:
Implicit conversion avoids data loss or errors during operations.

Python always tries to promote to the most general type in expressions (e.g., int → float → complex).

❌ What Python won’t do implicitly:
Some conversions must be explicit to avoid ambiguity:

print("5" + 2) # ❌ TypeError: can only concatenate str (not "int") to str

✅ Use explicit conversion:
print(int("5") + 2) # 7

🔚 Summary:
Term Meaning
Implicit Conversion Python automatically changes data types
Goal Prevent errors and promote safe calculations
Trigger Mixed-type expressions (e.g., int + float)

**🧮 What is Flooring a Number in Python?**
Flooring a number means rounding it down to the nearest integer that is less than or equal to the number.

✅ Example:
import math

`print(math.floor(3.9))`# Output: 3
`print(math.floor(-3.9))` # Output: -4
3.9 becomes 3

-3.9 becomes -4 (it goes downward, not toward zero)

🔧 Syntax:
import math
math.floor(number)
You must import the math module to use math.floor()

📌 Difference between floor() and int():
Function Behavior
math.floor() Always rounds downward
int() Removes decimal part (rounds towards 0)

✅ Example:
import math

print(math.floor(-3.7)) # -4
print(int(-3.7)) # -3

💡 Bonus: Floor Division Operator (//)
Python also supports floor division using //, which returns the floored result of a division:
print(7 // 2) # 3
print(-7 // 2) # -4

📚 Summary:

- Flooring means rounding down to the nearest whole number.

- Use math.floor(x) to floor a number.

- Use // to do floor division.

- int(x) and math.floor(x) may give different results for negative numbers.

**🔁 round() Function in Python**
The round() function is used to round a number to the nearest integer or to a specified number of decimal places.

✅ Basic Syntax:
round(number, ndigits)
number: The floating-point number you want to round.

ndigits (optional): The number of decimal places to round to.

If not provided, it rounds to the nearest integer.

🔍 Examples:

1. Rounding to Nearest Integer:
   print(round(4.6)) # 5
   print(round(4.3)) # 4

2. Rounding to Specific Decimal Places:
   print(round(3.14159, 2)) # 3.14
   print(round(3.14159, 3)) # 3.142

3. Rounding Negative Numbers:
   print(round(-2.3)) # -2
   print(round(-2.7)) # -3

⚠️ Tie-breaking Rule (Banker's Rounding)
Python uses round-half-to-even strategy (also called Banker’s rounding). That means:

print(round(2.5)) # 2 (nearest even)
print(round(3.5)) # 4 (nearest even)
This avoids rounding bias in large datasets.

💡 Note:
round() returns an int if ndigits is not specified.

Returns a float if you round to decimal places.

🧠 Summary:

- Use Case Code Example Result
- Round to nearest integer round(2.7) 3
- Round to 2 decimal places round(2.71828, 2) 2.72
- Round 2.5 round(2.5) 2
- Round 3.5 round(3.5) 4

**🔤 What is an f-string in Python?**
f-strings (formatted string literals) are a concise and readable way to embed expressions, variables, or function calls directly inside strings using {}.

Introduced in Python 3.6, they start with the letter f or F before the string.

✅ Basic Syntax:
name = "Nagendra"
print(f"Hello, {name}!") # Hello, Nagendra!
💡 Why Use f-strings?
Cleaner and more readable

Faster than format() or concatenation

Supports expressions inside {}

🔍 Examples:

1. Inserting Variables:
   age = 25
   print(f"I am {age} years old.") # I am 25 years old.

2. Expressions Inside f-strings:
   x = 5
   y = 10
   print(f"Sum: {x + y}") # Sum: 15

3. Calling Functions:
   def greet(name):
   return f"Hi, {name}!"

print(f"{greet('Nagendra')} Welcome!") # Hi, Nagendra! Welcome!

4. Formatting Numbers:
   pi = 3.14159
   print(f"Value of pi: {pi:.2f}") # Value of pi: 3.14
   :.2f → format float to 2 decimal places

5. Using Dictionaries or Lists:
   person = {"name": "Ram", "age": 30}
   print(f"{person['name']} is {person['age']} years old.") # Ram is 30 years old.

⚠️ Rules:

- f-strings only work in Python 3.6+

- Expressions must be valid Python code

- You can’t use backslashes (\) inside expressions

🧠 Summary

- Feature Example Output
  -p Variable Insert f"Name: {name}" Name: Nagendra
- Expression f"{a + b}" Sum result
- Decimal Format f"{pi:.2f}" 3.14
- Function Call f"{greet('Ram')}" Hi, Ram!

### Conditional Statements, Logical Operators, Code Blocks and Scope

🔀 Python Conditional Statements – All Rules & Details
Conditional statements allow you to make decisions in your code based on conditions. These are core to control flow in Python.

🧱 1. The if Statement
Executes a block of code only if a condition is True.

x = 10

if x > 5:
print("x is greater than 5")

🧱 2. The else Statement
Provides an alternative block if the if condition is False.

x = 2

if x > 5:
print("x is greater than 5")
else:
print("x is 5 or less")

🧱 3. The elif (Else If) Statement
Checks multiple conditions in sequence.

x = 5

if x > 10:
print("x > 10")
elif x == 5:
print("x is exactly 5")
else:
print("x is less than 10 and not 5")
✅ Only one block will execute — the first condition that is true.

✅ 4. Indentation Matters
Python uses indentation to define blocks.

if True:
print("This is inside the if")
print("This is outside the if")

🔗 5. Comparison Operators
Operator Meaning Example
== Equal to x == y
!= Not equal to x != y

>     Greater than	x > y
>
> < Less than x < y
> = Greater than or equal x >= y
> <= Less than or equal x <= y

🔀 6. Logical Operators
Used to combine multiple conditions.

Operator Description Example
and Both conditions must be True x > 3 and x < 10
or At least one condition is True x < 3 or x > 8
not Inverts a condition not(x > 5) is True if x <= 5

🧠 7. Nested Conditions
You can write if statements inside another if.

x = 15
if x > 10:
if x < 20:
print("x is between 10 and 20")

🧪 8. Ternary / One-line if
Short-hand for if-else.

x = 10
result = "Even" if x % 2 == 0 else "Odd"
print(result) # Even

🚫 9. Falsy and Truthy Values
In conditions, Python treats the following as False:

0, 0.0

None

False

Empty structures: '', [], {}, ()

Everything else is considered True.

if []:
print("Won't print")
else:
print("This will print")

📌 Summary Flow:

if condition1: # block A
elif condition2: # block B
else: # block C
