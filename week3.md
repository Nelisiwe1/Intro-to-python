# Data Structure

Python offers several built-in data structures that help you organize and manipulate data efficiently. Here are some key data structures in Python:

### 1. Lists:

- **Definition:**
  - An ordered collection that can contain elements of different data types.

- **Example:**
  ```python
  my_list = [1, 2, 3, 'hello', True]
  ```

- **Operations:**
  - Indexing, slicing, appending, extending, etc.

### 2. Tuples:

- **Definition:**
  - Similar to lists but immutable (cannot be changed once created).

- **Example:**
  ```python
  my_tuple = (1, 2, 'world')
  ```

- **Operations:**
  - Similar to lists, but no item assignment or deletion.

### 3. Sets:

- **Definition:**
  - An unordered collection of unique elements.

- **Example:**
  ```python
  my_set = {1, 2, 3, 3, 4}
  ```

- **Operations:**
  - Set operations like union, intersection, difference, etc.

### 4. Dictionaries:

- **Definition:**
  - A collection of key-value pairs.

- **Example:**
  ```python
  my_dict = {'name': 'John', 'age': 25, 'city': 'New York'}
  ```

- **Operations:**
  - Accessing, updating, and deleting items by key.

### 5. Strings:

- **Definition:**
  - Immutable sequences of characters.

- **Example:**
  ```python
  my_string = "Hello, World!"
  ```

- **Operations:**
  - String manipulation, slicing, concatenation, etc.

### 6. Queues (Queue module):

- **Definition:**
  - Implemented using the `queue` module for First-In-First-Out (FIFO) order.

- **Example:**
  ```python
  from queue import Queue

  my_queue = Queue()
  my_queue.put(1)
  ```

### 7. Stacks (LifoQueue module):

- **Definition:**
  - Implemented using the `queue` module for Last-In-First-Out (LIFO) order.

- **Example:**
  ```python
  from queue import LifoQueue

  my_stack = LifoQueue()
  my_stack.put(1)
  ```

  # Python List

Lists in Python are versatile and commonly used data structures. They are ordered, mutable (can be changed), and can contain elements of different data types. Here's an overview of Python lists:

### Creating a List:

You can create a list by placing elements inside square brackets `[]`:

```python
my_list = [1, 2, 3, 'hello', True]
```

### Accessing Elements:

Elements in a list can be accessed using indexing. Python uses 0-based indexing:

```python
first_element = my_list[0]  # Access the first element
second_element = my_list[1]  # Access the second element
```

### Slicing:

You can extract a portion of the list using slicing:

```python
subset = my_list[1:4]  # Get elements from index 1 to 3
```

### Modifying Elements:

Lists are mutable, so you can change their elements:

```python
my_list[0] = 100  # Change the first element to 100
```

### List Methods:

Python provides various built-in methods for manipulating lists:

- `append()`: Adds an element to the end of the list.
  ```python
  my_list.append(4)
  ```

- `extend()`: Extends the list by appending elements from another iterable.
  ```python
  my_list.extend([5, 6, 7])
  ```

- `insert()`: Inserts an element at a specified position.
  ```python
  my_list.insert(2, 'new_element')
  ```

- `remove()`: Removes the first occurrence of a specified element.
  ```python
  my_list.remove('hello')
  ```

- `pop()`: Removes and returns an element at a specified position (or the last element if no position is specified).
  ```python
  popped_element = my_list.pop(1)
  ```

- `index()`: Returns the index of the first occurrence of a specified element.
  ```python
  index = my_list.index(True)
  ```

- `count()`: Returns the number of occurrences of a specified element.
  ```python
  count = my_list.count(3)
  ```

- `reverse()`: Reverses the order of the list.
  ```python
  my_list.reverse()
  ```

- `sort()`: Sorts the elements of the list.
  ```python
  my_list.sort()
  ```

### List Comprehensions:

List comprehensions provide a concise way to create lists:

```python
squared_numbers = [x**2 for x in range(5)]
# Result: [0, 1, 4, 9, 16]
```

### Nested Lists:

Lists can contain other lists, forming nested structures:

```python
nested_list = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

Lists are a fundamental and powerful data structure in Python, suitable for a wide range of tasks.

# Errors and Exceptions

In Python, errors and exceptions are part of the language's error-handling mechanism. Here's a brief overview:

### Errors:

Errors in Python can be broadly categorized into two types:

1. **Syntax Errors:**
   - These occur when you make a mistake in the syntax of your code.
   - The interpreter raises a `SyntaxError` if it encounters incorrect syntax.

   ```python
   # SyntaxError: invalid syntax
   print "Hello, World!"
   ```

2. **Runtime Errors (Exceptions):**
   - These occur during the execution of the program.
   - Examples include `ZeroDivisionError`, `TypeError`, `NameError`, etc.

   ```python
   # ZeroDivisionError: division by zero
   result = 10 / 0
   ```

### Exception Handling:

To handle exceptions and prevent them from crashing your program, you can use the `try`, `except`, `else`, and `finally` blocks.

- **try-except:**
  - Used to catch and handle exceptions.

  ```python
  try:
      result = 10 / 0
  except ZeroDivisionError:
      print("Error: Division by zero!")
  ```

- **else:**
  - Optional block that is executed if no exceptions are raised in the `try` block.

  ```python
  try:
      result = 10 / 2
  except ZeroDivisionError:
      print("Error: Division by zero!")
  else:
      print("Result:", result)
  ```

- **finally:**
  - Optional block that is executed regardless of whether an exception occurs.

  ```python
  try:
      result = 10 / 0
  except ZeroDivisionError:
      print("Error: Division by zero!")
  finally:
      print("This will always be executed.")
  ```

### Raising Exceptions:

You can manually raise exceptions using the `raise` statement:

```python
age = -1

if age < 0:
    raise ValueError("Age cannot be negative.")
```

### Custom Exceptions:

You can define your own exception classes by inheriting from the `Exception` class:

```python
class CustomError(Exception):
    pass

raise CustomError("This is a custom error.")
```

Classes

In Python, classes are a fundamental part of object-oriented programming (OOP). They allow you to structure your code in a more organized and modular way. Here's an overview of Python classes:

### Defining a Class:

You can define a class using the `class` keyword:

```python
class MyClass:
    # Class attributes and methods go here
    pass
```

### Class Attributes and Methods:

- **Attributes:**
  - Variables defined within a class are called attributes.
  - They represent the characteristics or properties of an object.

  ```python
  class Dog:
      species = 'Canis familiaris'
  ```

- **Methods:**
  - Functions defined within a class are called methods.
  - They define the behavior of the class.

  ```python
  class Dog:
      def bark(self):
          return "Woof!"
  ```

### Instantiating Objects:

- **Creating Instances:**
  - Instances are objects created from a class.

  ```python
  my_dog = Dog()  # Creating an instance of the Dog class
  ```

### Constructors and Destructors:

- **Constructor (`__init__`):**
  - The `__init__` method is called when an object is created. It initializes attributes.

  ```python
  class Dog:
      def __init__(self, name, age):
          self.name = name
          self.age = age
  ```

- **Destructor (`__del__`):**
  - The `__del__` method is called when an object is about to be destroyed.

  ```python
  class Dog:
      def __del__(self):
          print(f"{self.name} has been destroyed!")
  ```

### Instance Methods vs. Class Methods:

- **Instance Methods:**
  - Methods that operate on an instance of the class.
  - The `self` parameter represents the instance.

  ```python
  class Dog:
      def bark(self):
          return "Woof!"
  ```

- **Class Methods:**
  - Methods that operate on the class itself.
  - Decorate the method with `@classmethod` and use `cls` as the first parameter.

  ```python
  class Dog:
      count = 0  # Class attribute

      @classmethod
      def increment_count(cls):
          cls.count += 1
  ```


