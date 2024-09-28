# Section 4: Functions and Exceptions (28%)

## PCEP-30-02 4.1 – Decompose the code using functions

### 1. Defining and Invoking User-Defined Functions

**Defining Functions:**

In Python, you can define a function using the `def` keyword followed by the function name and parentheses. Inside the parentheses, you can specify parameters that the function can accept.

**Example:**

```python
def greet(name):
print(f"Hello, {name}!")

```

In this example, `greet` is a function that takes one parameter, `name`, and prints a greeting.

**Invoking Functions:**

To call (invoke) a function, you simply use its name followed by parentheses, passing any required arguments.

**Example:**

```python
greet("Alice") # Output: Hello, Alice!

```

### 2. Generators

**What are Generators?**

Generators are a special type of function that return an iterator. They allow you to iterate through a sequence of values without storing the entire sequence in memory. You define a generator using the `yield` keyword instead of `return`.

Example:

```python
def count_up_to(n):
count = 1
while count <= n:
yield count
count += 1

```

**Invoking Generators:**

You can use a generator in a loop or convert it to a list.

**Example:**

```python
for number in count_up_to(5):
print(number)

# Output: 1, 2, 3, 4, 5
```

### 3. The return Keyword

**Using `return`:**

The return keyword is used to exit a function and optionally pass back a value to the caller. A function can return multiple values as a tuple.

Example:

```python
def add_and_subtract(a, b):
    return a + b, a - b

result = add_and_subtract(5, 3)
print(result) # Output: (8, 2)

```

### 4. The None Keyword

**What is None?**

`None` is a special constant in Python that represents the absence of a value or a null value. If a function does not explicitly return a value, it returns `None` by default.

Example:

```python
def do_nothing():
    pass

    result = do_nothing()
    print(result) # Output: None

```

### 5. Recursion

**What is Recursion?**

Recursion is a programming technique where a function calls itself to solve a smaller instance of the same problem. Each recursive call should bring the problem closer to a base case, which stops the recursion.

Example:
Here’s a simple example of a recursive function that calculates the factorial of a number:

```python
def factorial(n):
    if n == 0: # Base case
    return 1
    else:
        return n \* factorial(n - 1) # Recursive case

print(factorial(5)) # Output: 120
```
