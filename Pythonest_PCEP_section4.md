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

A) 5

B) 6

C) None

D) Error

Answer: B

```

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

```

#### 3.The return Keyword

Q5: What will be the output of the following code?

```python
def test():
    return

result = test()
print(result)

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

```

#### 4.The None Keyword

Q7: What does the expression x is None check?

A) If x is equal to 0

B) If x is an empty string

C) If x is not defined

D) If x has no value assigned

Answer: D) If x has no value assigned

Q8: What will the following code output?

```python
def no_return():
    pass

result = no_return()
print(result)

A) None

B) 0

C) ""

D) Error

Answer: A

```

#### 5. Recursion

Q9: What will be the output of the following code?

```python
def recursive_function(n):
    if n == 0:
        return 1
    return n * recursive_function(n - 1)

print(recursive_function(4))

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
```
