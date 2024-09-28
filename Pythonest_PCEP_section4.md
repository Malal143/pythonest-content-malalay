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

### Question with Answers

#### 1.Defining and Invoking User-Defined Functions

Q1: What will be the output of the following code?

```python
def func(x):
    return x + 1

print(func(5))
```

A) 5

B) 6

C) None

D) Error

Answer: B

Q2: Which of the following is a valid way to define a function in Python?

A) function myFunc() {}

B) def myFunc():

C) myFunc() => {}

D) myFunc := function()

Answer: B

#### 2.Generators

Q3: What will the following code output?

```python
def my_gen():
    yield 1
    yield 2

gen = my_gen()
print(next(gen))
print(next(gen))
```

A) 1 2

B) 1 then 2

C) 2 then 1

D) Error

Answer: B

Q4: How can you convert a generator to a list?

A) list(gen)

B) gen.to_list()

C) gen.list()

D) convert(gen)

Answer: A

#### 3.The return Keyword

Q5: What will be the output of the following code?

```python
def test():
    return

result = test()
print(result)
```

A) None

B) 0

C) Error

D) ""

Answer: A

Q6: Which of the following statements is true about the return statement in Python?

A) A function can have multiple return statements, but only one will execute.

B) A function can return multiple values, but they must be of the same type.

C) The return statement can only return integers.

D) None of the above.

Answer: A

#### 4.The None Keyword

Q7: What does the expression x is None check?

A) If x is equal to 0

B) If x is an empty string

C) If x is not defined

D) If x has no value assigned

Answer: D

Q8: What will the following code output?

```python
def no_return():
    pass

result = no_return()
print(result)
```

A) None

B) 0

C) ""

D) Error

Answer: A

#### 5.Recursion

Q9: What will be the output of the following code?

```python
def recursive_function(n):
    if n == 0:
        return 1
    return n * recursive_function(n - 1)

print(recursive_function(4))
```

A) 4

B) 24

C) 16

D) Error

Answer: B) 24

Q10: Which of the following statements about recursion is false?

A) Recursion can lead to infinite loops without a base case.

B) Recursive functions can always be replaced with iterative solutions.

C) Recursion can consume more memory than iterative solutions.

D) Recursion is always more efficient than iteration.

Answer: D

## PCEP-30-02 4.2 – Organize interaction between the function and its environment

### 1. Parameters vs. Arguments

**Parameters** are variables defined in a function's declaration that accept values when the function is called. They act as placeholders for the values that will be passed into the function.

**Arguments**, on the other hand, are the actual values or data you pass into the function when you call it.

**Example:**

```python
def greet(name): # 'name' is a parameter
print(f"Hello, {name}!")

greet("Alice") # "Alice" is an argument

```

### 2. Positional, Keyword, and Mixed Argument Passing

**Positional Arguments:**
are passed to a function in the order that the parameters are defined. The first argument corresponds to the first parameter, the second to the second, and so on.

**Example:**

```python
def add(a, b):
return a + b

result = add(2, 3) # 2 is assigned to 'a', 3 to 'b'

```

**Keyword Arguments:**
Are passed to a function by explicitly stating the parameter name and its value. This allows you to skip arguments or pass them in a different order.

**Example:**

````python
def display_info(name, age):
print(f"{name} is {age} years old.")

display_info(age=30, name="Bob") # Order doesn't matter

```
**Mixed Argument Passing**
You can combine positional and keyword arguments, but positional arguments must come first.

**Example:**

def info(name, age, country="USA"):
print(f"{name} is {age} years old and lives in {country}.")

info("Alice", 25) # Uses default for country
info("Bob", 30, country="Canada") # Overrides default
````

### 3. Default Parameter Values

Default parameter values allow you to define a parameter with a default value that will be used if no argument is provided for that parameter.

Example:

```python
def power(base, exponent=2):
return base \*\* exponent

print(power(3)) # Output: 9 (3^2)
print(power(3, 3)) # Output: 27 (3^3)
```

### 4. Name Scopes

N**ame Scope** refers to the region of a program where a name (variable, function, etc.) is accessible. Python has several scopes:

- Local Scope: Names defined within a function are local to that function.
- Enclosing Scope: Names in the local scope of enclosing functions (if any).
- Global Scope: Names defined at the top level of a module or script.
- Built-in Scope: Names pre-defined in Python (like len()).

**Example:**

```python
x = 10 # Global variable

def my_function():
x = 5 # Local variable
print(x)

my_function() # Output: 5
print(x) # Output: 10

```

### 5. Name Hiding (Shadowing)

Name hiding occurs when a local variable has the same name as a global variable. In this case, the local variable "shadows" the global variable within its scope.

Example:

```python
x = 10 # Global variable

def my_function():
x = 5 # Local variable (shadows global)
print(x)

my_function() # Output: 5
print(x) # Output: 10

```

### 6. The Global Keyword

The global keyword allows you to modify a global variable inside a function. Without using global, Python treats any variable assignment inside a function as local to that function.

**Example**:

```python
x = 10

def modify_global():
global x # Declare x as global
x = 5 # Modify global variable

modify_global()
print(x) # Output: 5
```

### Questions

Q1: Which of the following statements about parameters and arguments is true?

A) Parameters are the values passed to functions, while arguments are the placeholders in the function definition.

B) Parameters are defined in the function, while arguments are the values supplied during a function call.

C) Parameters can only be integers, while arguments can be of any type.

D) There is no difference between parameters and arguments.

Answer: B

Q2: What will be the output of the following code?

```python
def func(a, b):
    return a + b

print(func(1, 2))

A) 3

B) 12

C) None

D) Error

Answer: A
```

Q3: What will the following code output?

```python
def multiply(x, y=2):
    return x * y

print(multiply(5))

A) 5

B) 10

C) 7

D) Error

Answer: B
```

Q4: Which of the following function calls is valid?

```python
def func(a, b, c=5):
    return a + b + c

A) func(1, 2)

B) func(1, b=2)

C) func(a=1, 2)

D) func(1, 2, 3, 4)

Answer: A
```

Q5: What happens if you call the following function without providing the second argument?

```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

print(greet("Alice"))

A) Hello, Alice!

B) None

C) Error

D) Alice!

Answer: A
```

Q6: Which of the following statements is true regarding default parameter values?

A) Default values must be immutable types.

B) Default values are evaluated at function definition time, not at call time.

C) You can only have one default parameter in a function.

D) Default values can only be numbers.

Answer: B

Q7: What will the following code output?

```python
x = 10

def func():
    x = 5
    def inner_func():
        return x
    return inner_func()

print(func())

A) 10

B) 5

C) None

D) Error

Answer: B
```

Q8: Which of the following scopes has the highest precedence in Python?

A) Local Scope

B) Enclosing Scope

C) Global Scope

D) Built-in Scope

Answer: A

Q9: In the following code, what will be printed?

```python
x = 20

def func():
    x = 10
    print(x)

func()
print(x)

A) 10 then 20

B) 20 then 10

C) 10

D) Error

Answer: A

```

Q10: Which statement about name hiding (shadowing) is false?

A) A local variable can shadow a global variable.

B) Shadowing can lead to confusion in code.

C) Shadowed global variables can be accessed without the global keyword.

D) Shadowing is a common practice in programming.

Answer: C

## PCEP-30-02 4.3 – Python Built-In Exceptions Hierarchy
