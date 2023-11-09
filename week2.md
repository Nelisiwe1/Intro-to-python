# Control flow
Control flow statements in Python are used to alter the normal flow of program execution. Here are some of the key control flow statements in Python:

1. **if statements:**
   ```python
   if condition:
       # code to execute if condition is True
   elif another_condition:
       # code to execute if another_condition is True
   else:
       # code to execute if none of the above conditions are True
   ```

2. **for loop:**
   ```python
   for item in iterable:
       # code to execute for each item in the iterable
   ```

3. **while loop:**
   ```python
   while condition:
       # code to execute as long as the condition is True
   ```

4. **break statement:**
   ```python
   while condition:
       # code
       if some_condition:
           break  # exit the loop prematurely
   ```

5. **continue statement:**
   ```python
   for item in iterable:
       if some_condition:
           continue  
   ```

6. **pass statement:**
   It is used as a placeholder where syntactically some code is required, but you don't want to execute any code.

   ```python
   if some_condition:
       pass  
   else:
       
   ```

  # Function in python 

```python
def function_name(parameters):
    # code to be executed
    return result  # optional
```

- **def:** Keyword used to define a function.
- **function_name:** Name of the function, following the same rules as variable names.
- **parameters:** Input values that the function accepts (optional).
- **code to be executed:** The block of code that the function will run when called.
- **return:** Keyword used to return a value from the function (optional).

Here's an example:

```python
def greet(name):
    """This function greets the person passed in as a parameter."""
    return f"Hello, {name}!"

# Call the function
result = greet("Alice")
print(result)
```

In this example:
- `greet` is the function name.
- `(name)` is the parameter the function takes.
- The code inside the function is a simple string formatting.
- The function returns a greeting.

You can call the function with different values for `name` to get different greetings.

Functions are a fundamental part of Python programming, allowing you to organize and reuse code effectively. They can also take default values for parameters, accept variable numbers of arguments, and more, making them versatile and powerful.

# Modules



### Mechanism of Python Modules:

- **Definition:** A module is a file containing Python definitions and statements. It allows you to organize code logically.
  
- **Mechanism:**
  - Modules are imported using the `import` keyword.
  - The Python interpreter searches for the module in its standard path.

### Listing of Modules:

- **Listing:**
  - You can list all the modules available in your Python environment using the `help()` function or by exploring the `sys.modules` dictionary.

  ```python
  import sys

  print(sys.modules.keys())
  ```

### Importing Modules from Python Standard Path:

- **Standard Path:**
  - Python has a standard path where it looks for modules. This includes the Python standard library and other directories.
  - You can import modules using the `import` statement.

  ```python
  import math
  ```

### Importing Modules from Other Sources:

- **Custom Modules:**
  - You can import modules from other sources by providing the path.
  
  ```python
  # Assuming mymodule.py is in the same directory
  import mymodule
  ```

### Variable in a Module:

- **Variables in Module:**
  - Variables defined in a module can be accessed using the module's namespace.
  
  ```python
  # module.py
  my_variable = 42

  # script.py
  import module

  print(module.my_variable)
  ```

### Difference between a Module and a Package in Python:

- **Module:**
  - A single file containing Python definitions and statements.
  - It serves as a way to organize code.

- **Package:**
  - A collection of modules grouped together in a directory.
  - It includes a special `__init__.py` file to indicate that the directory should be treated as a package.

```plaintext
my_package/
|-- __init__.py
|-- module1.py
|-- module2.py
```

- **Usage:**
  - Modules are used for smaller-scale organizational purposes.
  - Packages are used for larger-scale projects, providing a hierarchical structure.

# Regular Expression
### Manipulating Strings to a Certain Format:

Manipulating strings in Python can be achieved using various methods. Two common techniques are grouping and capturing, as well as using assertions and flags.

#### Grouping and Capturing:

- **Grouping:**
  - Use parentheses `()` to group parts of a regular expression.

  ```python
  import re

  pattern = re.compile(r"(\d+)-(\d+)-(\d+)")
  match = pattern.match("2023-11-09")

  if match:
      print(match.groups())
  ```

- **Capturing:**
  - `groups()` method of the match object retrieves the captured groups.

#### Assertions and Flags:

- **Assertions:**
  - Use assertions like `(?=...)` for positive lookahead and `(?!...)` for negative lookahead.

  ```python
  import re

  pattern = re.compile(r"\bword\b(?=\s)")
  match = pattern.search("This word is followed by a space.")

  if match:
      print("Word is followed by a space.")
  ```

- **Flags:**
  - Flags modify the behavior of the regular expression. Common flags include `re.IGNORECASE` for case-insensitive matching.

  ```python
  import re

  pattern = re.compile(r"python", re.IGNORECASE)
  match = pattern.search("Python is awesome.")

  if match:
      print("Found Python (case-insensitive).")
  ```

These techniques are useful when working with regular expressions to manipulate strings. Grouping and capturing help extract specific parts of a string, while assertions and flags provide more flexibility and control over the matching process. Regular expressions can be powerful tools for string manipulation, but they require a good understanding of the syntax and patterns.