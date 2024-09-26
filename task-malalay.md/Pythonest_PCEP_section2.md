# Section 2: Control Flow – Conditional Blocks and Loops

## PCEP-30-02 2.1 – Make Decisions and Branch the Flow with the `if` Instruction

### 1. Conditional Statements

Conditional statements allow you to execute different blocks of code based on certain conditions. The main types of conditional statements in Python are:

- **`if` Statement**: Executes a block of code if the condition is true.
  
  ```python
  if condition:
    # Code to execute if condition is true

- **`if-else` Statement**: Executes one block of code if the condition is true, and another block if it is false.

```python
if condition:
    # Code to execute if condition is true
    else:
        # Code to execute if condition is false
        

- **`if-elif` Statement**: Allows you to check multiple conditions. If the first condition is false, it checks the next condition.

```python
if condition1:
    # Code to execute if condition1 is true
    elif condition2:
        # Code to execute if condition2 is true

    
-**`if-elif-else` Statement**: Combines the previous concepts to handle multiple conditions with a final fallback.

```python
if condition1:
    # Code to execute if condition1 is true
    elif condition2:
        # Code to execute if condition2 is true
        else
        # Code to execute if neither condition is true

---

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

---

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

---

- **`Example`**
Here's a complete example demonstrating various conditional statements:

age = 20
if age < 18:
    print("You are a minor.")
    elif age >= 18 and age < 65:
        print("You are an adult.")
        else:
            print("You are a senior citizen.")

---

### Summary
Use if to execute code based on a condition.
Use if-else to provide an alternative when the condition is false.
Use if-elif to handle multiple conditions.
Nesting allows for more complex decision-making.
```

---
---

### Multi-Choice, True, False Questions

1. **What will be the output of the following code?**
   ```python
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

---

2. **Which of the following statements is true about the following code?**
```python
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

---

3. **What is the output of the following code?**
```python
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

---

4. **Consider the following code snippet:**
```python
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

---

5. **What will be the output of this code?**
```python
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

---

6. **What is the result of the following code?**
```
x = 5
if x > 0:
if x < 10:
print("x is positive and less than 10")
A. x is positive and less than 10
B. x is positive
C. No output
D. Error
**Answer**: A

---

7. **What will happen if you run the following code?**
```
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

---

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

---

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

---

10. **What will be the output of the following code?**
```
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

---
## PCEP-30-02 2.2 – Perform different types of iterations 

### 1. 