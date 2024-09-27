# Section 2: Control Flow – Conditional Blocks and Loops

## PCEP-30-02 2.1 – Make Decisions and Branch the Flow with the `if` Instruction

### 1. Conditional Statements

Conditional statements allow you to execute different blocks of code based on certain conditions. The main types of conditional statements in Python are:

- **`if` Statement**: Executes a block of code if the condition is true.

  ```python
  if condition:
    # Code to execute if condition is true

  ```

- **`if-else` Statement**: Executes one block of code if the condition is true, and another block if it is false.

````python
if condition:
    # Code to execute if condition is true
    else:
        # Code to execute if condition is false

```
- **`if-elif` Statement**: Allows you to check multiple conditions. If the first condition is false, it checks the next condition.

```python
if condition1:
    # Code to execute if condition1 is true
    elif condition2:
        # Code to execute if condition2 is true

```
-**`if-elif-else` Statement**: Combines the previous concepts to handle multiple conditions with a final fallback.

```python
if condition1:
    # Code to execute if condition1 is true
    elif condition2:
        # Code to execute if condition2 is true
        else
        # Code to execute if neither condition is true

```

### 2. Multiple Conditional Statements
You can have multiple if, elif, and else statements to handle complex decision-making.


if condition1:
    # Code for condition1
    elif condition2:
        # Code for condition2
        elif condition3:
            # Code for condition3
            else:
                # Code if none of the above conditions are true

```
### 3. Nesting Conditional Statements
You can nest conditional statements within each other to create more complex logic.


if condition1:
    # Code for condition1
    if condition2:
        # Code for condition2 within condition1
        else:
            # Code if condition2 is false
            else:
                # Code if condition1 is false

```
- **`Example`**
Here's a complete example demonstrating various conditional statements:

age = 20
if age < 18:
    print("You are a minor.")
    elif age >= 18 and age < 65:
        print("You are an adult.")
        else:
            print("You are a senior citizen.")

```
### Multi-Choice, True, False Questions

1. **What will be the output of the following code?**
x = 10
if x > 5:
    print("Greater than 5")
    elif x < 5:
        print("Less than 5")
        else:
            print("Equal to 5")
A. Greater than 5
B. Less than 5
C. Equal to 5
D. No output
**Answer**: A

```
2. **Which of the following statements is true about the following code?**
y = 15
if y < 10:
    print("Low")
    elif y < 20:
        print("Medium")
        else:
            print("High")
A. It will print "Low".
B. It will print "Medium".
C. It will print "High".
D. It will raise an error.
**Answer**: B

```
3. **What is the output of the following code?**
a = 5
b = 10
if a > b:
    print("A")
    elif a < b:
        print("B")

        else:
            print("C")
- A. A
- B. B
- C. C
- D. No output
- **Answer**: B

```
4. **Consider the following code snippet:**
x = 0
if x:
    print("True")
    else:
        print("False")
What will be printed?
A. True
B. False
C. 0
D. No output
**Answer**: B

```
5. **What will be the output of this code?**
num = 8
if num % 2 == 0:
    print("Even")
    elif num % 2 == 1:
        print("Odd")
        else:
            print("Not a number")
A. Even
B. Odd
C. Not a number
D. No output
**Answer**: A

```
6. **What is the result of the following code?**
x = 5
if x > 0:
    if x < 10:
        print("x is positive and less than 10")
A. x is positive and less than 10
B. x is positive
C. No output
D. Error
**Answer**: A

```
7. **What will happen if you run the following code?**
x = True
y = False
if x:
    if y:
        print("Both True")
        else:
            print("Only x is True")
            else:
                print("x is False")
A. Both True
B. Only x is True
C. x is False
D. No output
**Answer**: B

```
8. **What is the output of the following code?**
x = 20
if x > 10:
    print("A")
    elif x > 15:
        print("B")
        else:
            print("C")
A. A
B. B
C. C
D. No output
**Answer**: A

```
9. **Which of the following statements is correct regarding the following code?**
x = -1
if x > 0:
    print("Positive")
    elif x < 0:
        print("Negative")
        else:
            print("Zero")
A. It will print "Positive".
B. It will print "Negative".
C. It will print "Zero".
D. It will raise an error.
**Answer**: B

```
10. **What will be the output of the following code?**
x = 10
y = 20
if x == 10 and y == 20:
    print("Both are correct")
    elif x == 10 or y == 20:
        print("At least one is correct")
        else:
            print("None are correct")
A. Both are correct
B. At least one is correct
C. None are correct
D. Error
**Answer**: A

```
## PCEP-30-02 2.2 – Perform different types of iterations

### 1.The pass Instruction

The pass statement is a null operation; it does nothing when executed. It's often used as a placeholder in loops, functions, or classes where code will eventually go but is not yet implemented.

Example:
for i in range(5):
    if i == 2:
        pass # Placeholder for future code
        print(i)

### 2. Building Loops

Python supports several types of loops: while and for.

#### a. while Loop

A while loop continues executing as long as a condition is True.

Example:

count = 0
while count < 5:
    print(count)
    count += 1

#### b. for Loop

A for loop iterates over a sequence (like a list, tuple, or string).

Example:

for i in range(5):
    print(i)

### 3. Iterating Through Sequences

You can iterate through various data structures like lists, tuples, and strings.

Example:

fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)

### 4. Expanding Loops with while-else and for-else

Both while and for loops can have an else clause that runs if the loop completes normally (not terminated by break).

Example:
```python
for i in range(3):
    print(i)
    else:
        print("Loop completed without break.")

count = 0
while count < 3:
    print(count)
    count += 1
    else:
        print("While loop completed without break.")

### 5. Nesting Loops and Conditional Statements

You can nest loops and conditionals to create more complex logic.

Example:

for i in range(3):
    for j in range(2):
        if i == j:
            print(f"i: {i}, j: {j} - They are equal")
            else:
                print(f"i: {i}, j: {j} - They are not equal")

## 6. Controlling Loop Execution with break and continue

`break`: Terminates the loop.
`continue`: Skips the current iteration and continues with the next one.

Example:

for i in range(5):
    if i == 2:
        break # Exit the loop when i is 2
        print(i)
        print("-----")
        for i in range(5):
            if i == 2:
                continue # Skip the rest of the loop when i is 2
                print(i)
````

## Multi-Choice, True, False Questions

### 1. The `pass` Instruction

**1.** What is the purpose of the `pass` statement in Python?

- A. To terminate a loop
- B. To define an empty block of code
- C. To raise an exception
- D. To return a value

**Answer:** B

---

### 2. Building Loops with `while`, `for`, `range()`, and `in`

**2.** Which of the following correctly creates a loop that prints numbers from 1 to 5?

- A. `for i in range(5): print(i)`
- B. `for i in range(1, 6): print(i)`
- C. `while i < 5: print(i); i += 1`
- D. `while i < 6: print(i); i += 1`

**Answer:** B

## 3. Iterating Through Sequences

**3.** What will be the output of the following code?

fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
print(fruit[0])

- A. a b c
- B. apple banana cherry
- C. ['a', 'b', 'c']
- D. Error

**Answer:** A

## 4. Expanding Loops with while-else and for-else

**4.** What does the else block do in a for loop?

- A. It executes when the loop is terminated by a break statement.
- B. It executes when the loop completes normally without hitting a break.
- C. It executes for every iteration of the loop.
- D. It has no effect.

  **Answer:** B

## 5. Nesting Loops and Conditional Statements

**5.** What will be the output of the following code?

for i in range(3):
for j in range(2):
if i == j:
print(i, j)

- A. (0, 0) (1, 1) (2, 2)
- B. (0, 0) (1, 1)
- C. (0, 0) (1, 1) (2, 2) (2, 2)
- D. No output

**Answer:** B

## 6. Controlling Loop Execution with break

**6.** What will be the output of the following code?

for i in range(5):
if i == 3:
break
print(i)

- A. 0 1 2 3
- B. 0 1 2
- C. 1 2 3
- D. 0 1 2 3 4

**Answer:** B

## 7. Controlling Loop Execution with continue

**7.** What will be the output of the following code?

for i in range(5):
if i == 2:
continue
print(i)

- A. 0 1 2 3 4
- B. 0 1 3 4
- C. 0 1 2 3
- D. 1 2 3 4

**Answer:** B

## 8. Using range()

**8.** What will be the output of the following code?

for i in range(1, 10, 2):
print(i, end=' ')

- A. 1 2 3 4 5 6 7 8 9
- B. 1 3 5 7 9
- C. 1 2 3 4 5 6 7 8 9
- D. 1 2 3 4 5 6 7 8

**Answer:** B

### 9. Nested Loops

Question 9: How many times will "Hello" be printed in the following code?

for i in range(2):
for j in range(3):
print("Hello")

- A. 2
- B. 3
- C. 5
- D. 6

**Answer:** D

### 10. Using for with in

**10.** Which of the following statements is true about the for loop?

- A. It can iterate over any iterable object.
- B. It can only iterate over lists.
- C. It cannot be used with strings.
- D. It requires a counter variable.

**Answer:** A
