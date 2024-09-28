# Section 3: Data Collections – Tuples, Dictionaries, Lists, and Strings (25%)

## PCEP-30-02 3.1 – Collect and Process Data Using Lists

### 1. Constructing Vectors

In Python, a list can be used as a vector, which is a `one-dimensional array`. You can create a list using square brackets [].

#### Example

`vector` = [1, 2, 3, 4, 5] 2. Indexing and Slicing
Indexing allows you to access individual elements in a list, while slicing lets you access a range of elements.

#### Indexing

first_element = vector[0] # 1
last_element = vector[-1] # 5

#### Slicing

sub_vector = vector[1:4] # [2, 3, 4]

### 3. The len() Function

The len() function returns the number of elements in a list.

length = len(vector) # 5

### 4. List Methods

Python provides several built-in methods to manipulate lists:

append(): Adds an element to the end of the list.
insert(): Inserts an element at a specified index.
index(): Returns the index of the first occurrence of a value.

vector.append(6) # [1, 2, 3, 4, 5, 6]
vector.insert(0, 0) # [0, 1, 2, 3, 4, 5, 6]
index_of_3 = vector.index(3) # 3

### 5. Functions: len(), sorted()

len(): As mentioned, returns the length of the list.
sorted(): Returns a new sorted list from the elements of any iterable.

sorted_vector = sorted(vector) # [0, 1, 2, 3, 4, 5, 6]

### 6. The del Instruction

The del statement can be used to remove elements from a list.

del vector[0] # Removes the first element, vector is now [1, 2, 3, 4, 5, 6]

### 7. Iterating Through Lists with the for Loop

You can use a for loop to iterate over each element in a list.

for element in vector:
print(element) # Prints each element in the vector

### 8. Initializing Loops

You can initialize loops by using the range() function to create a sequence of numbers.

for i in range(len(vector)):
print(vector[i]) # Prints each element using its index

### 9. The in and not in Operators

These operators check for the presence of a value in a list.

if 3 in vector:
print("3 is in the vector") # True

if 10 not in vector:
print("10 is not in the vector") # True

### 10. List Comprehensions

A concise way to create lists using a single line of code.

squared_vector = [x**2 for x in vector] # [1, 4, 9, 16, 25, 36]

### 11. Copying and Cloning

You can create a copy of a list using slicing or the copy() method.

copied_vector = vector[:] # Copy using slicing
cloned_vector = vector.copy() # Copy using copy() method

### 12. Lists in Lists: Matrices and Cubes

You can create lists of lists to represent matrices or cubes.

#### Matrix (2D list)

```python
matrix = [
[1, 2, 3],

[4, 5, 6],

[7, 8, 9]
]

# Acessing elements in a matrix

element = matrix[1][2] # 6

```

#### Cube (3D list)

```python
cube = [

[

[1, 2],

[3, 4]

],

[

[5, 6],

[7, 8]

]
]
```

### Multi-Choice, True, False Questions

`1. Constructing Vectors`

1. What is the correct way to create a vector in Python?

- A) `vector = []`
- B) `vector = ()`
- C) `vector = {}`
- D) `vector = [1, 2, 3]`

- **Answer**: D

  2.Which of the following initializes a vector with three elements?

- A) `vector = [1, 2, 3]`
- B) `vector = [1; 2; 3]`
- C) `vector = (1, 2, 3)`
- D) `vector = {1, 2, 3}`
- **Answer**: A

  3.How can you create an empty vector?

- A) `vector = {}`
- B) `vector = []`
- C) `vector = ()`
- D) `vector = None`

- **Answer**: B

  4.Which of the following is not a valid way to create a vector?

- A) `vector = [1, 2, 3]`
- B) `vector = list()`
- C) `vector = [1; 2; 3]`
- D) `vector = [x for x in range(5)]`

- **Answer**: C

  5.What will `vector = [1, 2, 3]` return when printed?

- A) `None`
- B) `[1, 2, 3]`
- C) `1, 2, 3`
- D) `Error`

- **Answer**: B

  6.Which method can be used to create a vector from a string?

- A) `split()`
- B) `join()`
- C) `append()`
- D) `extend()`

- **Answer**: A

  7.How do you create a vector with repeated values?

- A) `vector = [0] * 5`
- B) `vector = repeat(0, 5)`
- C) `vector = [0, 0, 0, 0, 0]`
- D) `vector = [0:5]`

- **Answer**: A

  8.Which of the following creates a vector with the first 10 even numbers?

- A) `vector = [x for x in range(10)]`
- B) `vector = [x * 2 for x in range(10)]`
- C) `vector = [2, 4, 6, 8, 10]`
- D) `vector = list(range(0, 20, 2))`

- **Answer**: D

  9.What is the result of `vector = [1, 2, 3]; vector[0]`?

- A) `1`
- B) `2`
- C) `3`
- D) `Error`

- **Answer**: A

  10.How do you create a vector with mixed data types?

- A) `vector = [1, "two", 3.0]`
- B) `vector = (1, "two", 3.0)`
- C) `vector = {1, "two", 3.0}`
- D) `vector = [1; "two"; 3.0]`

- **Answer**: A

## 2. Indexing and Slicing

1.What will `my_list = [1, 2, 3, 4, 5]; my_list[1:4]` return?

- A) `[1, 2, 3]`

- B) `[2, 3, 4]`

- C) `[3, 4, 5]`

- D) `Error`

- **Answer**: B

  2.What does `my_list[-1]` return if `my_list = [1, 2, 3]`?

- A) `1`
- B) `2`
- C) `3`
- D) `Error`

- **Answer**: C

  3.How do you slice the last two elements of a list?

- A) `my_list[-2:]`
- B) `my_list[2:]`
- C) `my_list[:2]`
- D) `my_list[2:-1]`

- **Answer**: A

  4.What will `my_list[1:5:2]` return for `my_list = [0, 1, 2, 3, 4, 5]`?

- A) `[1, 3]`
- B) `[0, 2, 4]`
- C) `[1, 2, 3]`
- D) `[0, 1, 2, 3, 4]`

- **Answer**: A

  5.What will `my_list = [1, 2, 3]; my_list[:2]` return?

- A) `[1, 2]`
- B) `[2, 3]`
- C) `[1, 2, 3]`
- D) `Error`

- **Answer**: A

  6.How do you get the first three elements of a list?

- A) `my_list[0:3]`
- B) `my_list[:3]`
- C) Both A and B
- D) `my_list[3:]`

- **Answer**: C

  7.What does `my_list[::-1]` do?

- A) Returns the list in reverse order
- B) Returns the original list
- C) Returns an empty list
- D) Returns the first element

  - **Answer**: A

    8.What will `my_list[1:3]` return for `my_list = [5, 10, 15, 20]`?

- A) `[10, 15]`
- B) `[5, 10]`
- C) `[15, 20]`
- D) `Error`

- **Answer**: A

  9.If `my_list = [1, 2, 3, 4]`, what does `my_list[1:-1]` return?

- A) `[2, 3]`
- B) `[1, 2, 3]`
- C) `[2, 3, 4]`
- D) `Error`

- **Answer**: A

  10.What will `my_list[::2]` return for `my_list = [0, 1, 2, 3, 4]`?

- A) `[0, 2, 4]`
- B) `[1, 3]`
- C) `[0, 1, 2, 3, 4]`
- D) `Error`

- **Answer**: A

### 3.The len() Function

1.What does the `len()` function do?

- A) Returns the first element of a list
- B) Returns the length of a list
- C) Returns the last element of a list
- D) Returns an error

- **Answer**: B

  2.What will `len([1, 2, 3, 4])` return?

- A) `3`
- B) `4`
- C) `5`
- D) `Error`

- **Answer**: B

  3.If `my_list = []`, what does `len(my_list)` return?

- A) `0`
- B) `1`
- C) `Error`
- D) `None`

- **Answer**: A

  4.What does `len("Hello")` return?

- A) `5`
- B) `4`
- C) `Error`
- D) `None`

- **Answer**: A

  5.For a nested list `my_list = [[1, 2], [3, 4]]`, what does `len(my_list)` return?

- A) `2`
- B) `4`
- C) `Error`
- D) `None`

- **Answer**: A

  6.What will `len([None, None, None])` return?

- A) `0`
- B) `1`
- C) `3`
- D) `Error`
- **Answer**: C

  7.If `my_list = [1, 2, 3]`, what will `len(my_list) + 1` return?

- A) `3`
- B) `4`
- C) `5`
- D) `Error`

- **Answer**: B

  8.What does `len(range(5))` return?

- A) `4`
- B) `5`
- C) `0`
- D) `Error`

- **Answer**: B

  9.For a string `s = "Python"`, what does `len(s)` return?

- A) `6`
- B) `5`
- C) `Error`
- D) `None`

- **Answer**: A

  10.If `my_list = [1, 2, 3, 4, 5]`, what is the value of `len(my_list) * 2`?

- A) `5`
- B) `10`
- C) `15`
- D) `Error`

- **Answer**: B

`### 4.List Methods: append(), insert(), index(), etc`

1.What does `my_list.append(4)` do?

- A) Adds `4` at the beginning of `my_list`
- B) Adds `4` at the end of `my_list`
- C) Replaces the first element with `4`
- D) Returns an error

- **Answer**: B

  2.What will `my_list.insert(1, 5)` do if `my_list = [1, 2, 3]`?

- A) `[5, 1, 2, 3]`
- B) `[1, 5, 2, 3]`
- C) `[1, 2, 3, 5]`
- D) `Error`

- **Answer**: B

  3.What does `my_list.index(2)` return for `my_list = [1, 2, 3]`?

- A) `1`
- B) `2`
- C) `0`
- D) `Error`

- **Answer**: A

  4.What will happen if you call `my_list.index(5)` when `my_list = [1, 2, 3]`?

- A) `0`
- B) `Error`
- C) `-1`
- D) `None`

- **Answer**: B

  5.What does `my_list.remove(2)` do if `my_list = [1, 2, 3]`?

- A) Removes the first occurrence of `2`
- B) Removes the last occurrence of `2`
- C) Returns an error
- D) Does nothing

- **Answer**: A

  6.What will `my_list.pop()` return for `my_list = [1, 2, 3]`?

- A) `1`
- B) `2`
- C) `3`
- D) `Error`

- **Answer**: C

  7.What does `my_list.clear()` do?

- A) Removes all elements from the list
- B) Clears the first element
- C) Returns an empty list
- D) Does nothing

- **Answer**: A

  8.Which method adds multiple elements to a list?

- A) `append()`
- B) `insert()`
- C) `extend()`
- D) `remove()`

- **Answer**: C

  9.What does `my_list.sort()` do?

- A) Sorts the list in ascending order
- B) Sorts the list in descending order
- C) Returns an error
- D) Does nothing

- **Answer**: A

  10.If `my_list = [3, 1, 2]`, what will `my_list.sort()` return?

- A) `[1, 2, 3]`
- B) `[3, 2, 1]`
- C) `Error`
- D) `[3, 1, 2]`

- **Answer**: A

### 5.Functions: len(), sorted()

1.What does the `sorted()` function do?

- A) Sorts a list in place
- B) Returns a new sorted list
- C) Returns an error
- D) Does nothing

- **Answer**: B

  2.What is the result of `sorted([3, 1, 2])`?

- A) `[3, 1, 2]`
- B) `[1, 2, 3]`
- C) `Error`
- D) `[2, 3, 1]`

- **Answer**: B

  3.How can you sort a list in descending order?

- A) `sorted(my_list, reverse=True)`
- B) `my_list.sort(reverse=True)`
- C) Both A and B
- D) `Error`

- **Answer**: C

  4.If `my_list = [3, 1, 2]`, what does `len(my_list)` return?

- A) `2`
- B) `3`
- C) `1`
- D) `Error`

- **Answer**: B

  5.What will `sorted("hello")` return?

- A) `['e', 'h', 'l', 'l', 'o']`
- B) `'ehllo'`
- C) `Error`
- D) `['h', 'e', 'l', 'o']`

- **Answer**: A

  6.What will `len([1, 2, 3, 4, 5])` return?

- A) `4`
- B) `5`
- C) `6`
- D) `Error`

- **Answer**: B

  7.If `my_list = []`, what does `sorted(my_list)` return?

- A) `[]`
- B) `None`
- C) `Error`
- D) `0`

- **Answer**: A

  8.What does `len("Python3")` return?

- A) `7`
- B) `6`
- C) `5`
- D) `Error`

- **Answer**: A

  9.What will `sorted([5, 3, 1, 4, 2])` return?

- A) `[1, 2, 3, 4, 5]`
- B) `[5, 4, 3, 2, 1]`
- C) `Error`
- D) `[3, 2, 1, 5, 4]`

- **Answer**: A

  10.If `my_list = [3, 1, 2]`, what will `my_list.sort()` return?

- A) `[1, 2, 3]`
- B) `None`
- C) `Error`
- D) `[3, 1, 2]`

- **Answer**: B

### 6.The del Instruction

1. What does `del my_list[0]` do?

- A) Deletes the first element of `my_list`
- B) Deletes the last element of `my_list`
- C) Returns an error
- D) Does nothing

- **Answer**: A

  2.What will happen if you use `del my_list`?

- A) Deletes the list entirely
- B) Deletes the first element
- C) Returns an error
- D) Does nothing

- **Answer**: A

  3.If `my_list = [1, 2, 3]`, what does `del my_list[1]` return?

- A) `2`
- B) `1`
- C) `3`
- D) `Error`

- **Answer**: D

  4.What does `del my_list[1:3]` do?

- A) Deletes the first two elements
- B) Deletes elements at index 1 and 2
- C) Deletes the last two elements
- D) Returns an error

- **Answer**: B

  5.If `my_list = [1, 2, 3]`, what will `del my_list[3]` do?

- A) Deletes `3`
- B) Returns an error
- C) Deletes `2`
- D) Does nothing

- **Answer**: B

  6.What is the effect of `del my_list[:]`?

- A) Deletes all elements from `my_list`
- B) Clears the first element
- C) Returns an error
- D) Does nothing

- **Answer**:

---

## PCEP-30-02: Collect and Process Data Using Tuples

### 1. Tuples: Indexing, Slicing, Building, Immutability

`What is a Tuple?`
A tuple is a collection data type in Python that is ordered and immutable. Tuples can hold a variety of data types, including integers, strings, lists, and even other tuples.

`Indexing`
Accessing Elements: You can access elements in a tuple using indexing, similar to lists. Indexing starts at 0.

my_tuple = (1, 2, 3, 4)
print(my_tuple[0]) # Output: 1

`Negative Indexing:` You can also use negative indexing to access elements from the end of the tuple.

print(my_tuple[-1]) # Output: 4

`Slicing`
Slicing Tuples: You can slice tuples to get a subset of elements, similar to lists.

sliced_tuple = my_tuple[1:3] # Output: (2, 3)

`Slicing with Steps:` You can also specify a step in slicing.

my_tuple = (0, 1, 2, 3, 4, 5)
print(my_tuple[::2]) # Output: (0, 2, 4)

#### Building Tuples

`Creating Tuples:` You can create tuples by placing comma-separated values inside parentheses.

my_tuple = (1, 2, 3)
another_tuple = 1, 2, 3 # Parentheses are optional

`Single Element Tuple:` To create a single-element tuple, you need to add a comma.

single_element_tuple = (1,) # Output: (1,)

`Immutability`
Immutability: Tuples are immutable, meaning once they are created, their elements cannot be changed, added, or removed.

my_tuple[0] = 10 # This will raise a TypeError

`Creating a New Tuple:` If you need to modify a tuple, you can create a new one.

my_tuple = (1, 2, 3)
new_tuple = my_tuple + (4,) # Output: (1, 2, 3, 4)

### 2. Tuples vs. Lists: Similarities and Differences

`Similarities`

- Ordered: Both tuples and lists maintain the order of elements.
- Indexing and Slicing: Both support indexing and slicing.
- Heterogeneous: Both can store elements of different data types.

`Differences`

- Mutability:
- Tuples are immutable; once created, their elements cannot be changed.
- Lists are mutable; you can modify, add, or remove elements.

`Syntax:`

- Tuples are defined using parentheses ().
- Lists are defined using square brackets [].

`Performance:`

- Tuples are generally faster than lists for iteration, due to their immutability.
- Lists have more built-in methods for manipulation (e.g., append(), remove()).

`Use Cases:`

- Use tuples for fixed collections of items (e.g., coordinates).
- Use lists for collections that need to be modified.

### 3. Lists Inside Tuples and Tuples Inside Lists

- Lists Inside Tuples
  You can store lists as elements within a tuple. This allows you to create complex data structures.

```python
my_tuple = ([1, 2], [3, 4])
print(my_tuple[0]) # Output: [1, 2]
print(my_tuple[0][1]) # Output: 2

- Modifying Lists Inside Tuples: While the tuple itself is immutable, you can modify the contents of the list inside it.

my_tuple[0].append(3) # Now my_tuple is ([1, 2, 3], [3, 4])

- Tuples Inside Lists
  You can also store tuples within lists. This can be useful for grouping related data.

my_list = [(1, 2), (3, 4)]
print(my_list[0]) # Output: (1, 2)
print(my_list[1][0]) # Output: 3

-Accessing Tuples: You can access tuples within a list just like any other list element.

```

### Multi-Choice, Questions

1. Tuples: Indexing, Slicing, Building, Immutability

1. What will be the output of the following code?

   ```python
   my_tuple = (1, 2, 3, 4)
   print(my_tuple[1:3])
   ```

A) (2, 3)
B) (1, 2, 3)
C) [2, 3]
D) (2, 3, 4)

Answer: A

2.Which of the following statements is true about tuples?

A) Tuples are mutable.
B) Tuples can contain lists.
C) Tuples are defined using square brackets.
D) Tuples cannot be empty.

Answer: B

3.What will the following code return?

my_tuple = (1, 2, 3)
my_tuple[0] = 10
A) (10, 2, 3)
B) TypeError
C) None
D) (1, 2, 3, 10)

Answer: B

4.How do you create a single-element tuple?

A) single_tuple = (1)
B) single_tuple = [1]
C) single_tuple = (1,)
D) single_tuple = 1,

Answer: C

5.What is the result of the following operation?

```python
my_tuple = (1, 2, 3)
new_tuple = my_tuple + (4,)
print(new_tuple)
A) (1, 2, 3, 4)
B) (1, 2, 3)
C) TypeError
D) (4, 1, 2, 3)

Answer: A

6. Which of the following correctly slices the tuple my_tuple = (0, 1, 2, 3, 4) to get (1, 2, 3)?

A) my_tuple[1:4]
B) my_tuple[1:3]
C) my_tuple[1:5]
D) my_tuple[0:3]

Answer: A

7. What will be the output of the following code?

my_tuple = (1, 2, 3)
print(my_tuple[-2])
A) 1
B) 2
C) 3
D) TypeError

Answer: B

8. Which method can you use to convert a list to a tuple?

A) list()
B) tuple()
C) convert()
D) set()

Answer: B

9. Given the tuple my_tuple = (1, (2, 3), 4), what will my_tuple[1][0] return?

A) 1
B) 2
C) 3
D) 4

Answer: B

10. What is the result of the following code?

my_tuple = (1, 2, 3)
my_list = list(my_tuple)
my_list[0] = 10
print(my_tuple)
A) (10, 2, 3)
B) (1, 2, 3)
C) TypeError
D) (1, 10, 3)

Answer: B
```

#### 2.Tuples vs. Lists: Similarities and Differences

1. Which of the following is a key difference between tuples and lists?

```python
A) Both can store heterogeneous data.
B) Tuples are mutable, while lists are immutable.
C) Tuples are defined with parentheses, while lists use brackets.
D) Both support the same methods.

Answer: C

2.What is the primary reason to use a tuple instead of a list?

A) Tuples can contain only numbers.
B) Tuples are faster and consume less memory.
C) Tuples can be modified after creation.
D) Tuples support more methods than lists.

Answer: B

3.Which of the following methods is not available for tuples?

A) count()
B) append()
C) index()
D) len()

Answer: B

4.If my_list = [1, 2, 3] and my_tuple = (1, 2, 3), what is the output of the following code?

print(my_list == my_tuple)
A) True
B) False
C) TypeError
D) None

Answer: B

5.Which of the following statements is true?

A) Lists can be used as keys in dictionaries, but tuples cannot.
B) Tuples can be used as keys in dictionaries, but lists cannot.
C) Both lists and tuples can be used as keys in dictionaries.
D) Neither lists nor tuples can be used as keys in dictionaries.

Answer: B

6.Which operation can be performed on a tuple but not on a list?

A) Indexing
B) Slicing
C) Concatenation
D) None; both support all operations.

Answer: D

7.What will be the output of the following code?

my_list = [1, 2, 3]
my_tuple = (1, 2, 3)
print(type(my_list) == type(my_tuple))
A) True
B) False
C) TypeError
D) None

Answer: B

8.Which of the following can lead to a TypeError?

A) Trying to modify a list.
B) Trying to modify a tuple.
C) Accessing an index out of range in a tuple.
D) Accessing an index out of range in a list.

Answer: B

9. Which of the following is a valid way to create a tuple from a list?

A) tuple = (my_list)
B) my_tuple = my_list()
C) my_tuple = tuple(my_list)
D) my_tuple = list(my_tuple)

Answer: C

10. What will be the output of the following code?

my_tuple = (1, 2, 3)
my_list = [my_tuple] * 2
print(my_list)
A) [(1, 2, 3), (1, 2, 3)]
B) [(1, 2, 3, 1, 2, 3)]
C) TypeError
D) [(1, 2), (3)]

Answer: A

```

#### 3.Lists Inside Tuples and Tuples Inside Lists

1. What will the following code output?

```python
my_tuple = ([1, 2], [3, 4])
my_tuple[0].append(3)
print(my_tuple)
A) ([1, 2], [3, 4])
B) ([1, 2, 3], [3, 4])
C) TypeError
D) ([1, 2], [3, 4, 3])

Answer: A
2. Which of the following is a valid operation?

A) my_list = [(1, 2), (3, 4)]
B) my_list = (1, [2, 3])
C) my_tuple = [1, 2, (3, 4)]
D) All of the above.

Answer: D

3. Given the following code, what will be the output?

my_list = [(1, 2), (3, 4)]
print(my_list[1][0])
A) 1
B) 2
C) 3
D) 4

Answer: C

4. What will happen if you try to append a tuple to a list inside a tuple?

my_tuple = ([1, 2], [3, 4])
my_tuple[0].append((5, 6))
print(my_tuple)
A) ([1, 2], [3, 4])
B) ([1, 2, (5, 6)], [3, 4])
C) TypeError
D) ([1, 2], [3, 4, (5, 6)])

Answer: B

5. What will be the output of the following code?

my_tuple = (1, 2, [3, 4])
my_tuple[2][0] = 5
print(my_tuple)
A) (1, 2, [5, 4])
B) TypeError
C) (1, 2, 3)
D) (1, 2, [3, 4])

Answer: A

6. Which of the following is true about nesting tuples and lists?

A) You can only nest tuples inside lists.
B) You can only nest lists inside tuples.
C) Both nesting is allowed.
D) Nesting is not allowed in Python.

Answer: C

7. What will the following code output?

my_list = [(1, 2), (3, 4)]
my_tuple = (my_list, (5, 6))
print(my_tuple[0][1][0])
A) 1
B) 2
C) 3
D) 5

Answer: C

8. What is the output of the following code?

my_list = [1, 2, 3]
my_tuple = (my_list,)
my_tuple[0][0] = 10
print(my_tuple)
A) (10, 2, 3)
B) (1, 2, 3)
C) TypeError
D) None

Answer: A

9. Given the tuple my_tuple = (1, [2, 3], 4), what will my_tuple[1].append(5) do?

A) (1, [2, 3, 5], 4)
B) TypeError
C) (1, 2, 3, 5, 4)
D) (1, [5], 4)

Answer: A

10. What will the following code return?

my_tuple = ([1, 2], (3, 4))
my_tuple[0].extend([5, 6])
print(my_tuple)
A) ([1, 2, 5, 6], (3, 4))
B) TypeError
C) ([1, 2], [5, 6])
D) ([5, 6], (3, 4))

Answer: A
```

## PCEP-30-02: Collect and Process Data Using Dictionaries

### 1. Dictionaries: Building, Indexing, Adding, and Removing Keys

`What is a Dictionary?`
A dictionary is an unordered collection of items in Python that stores data in key-value pairs. Each key must be unique, and it is used to access the corresponding value.

`Building Dictionaries`
Creating a Dictionary: You can create a dictionary using curly braces {} or the dict() constructor.

```python
my_dict = {'name': 'Alice', 'age': 25}
another_dict = dict(name='Bob', age=30)
```

`Empty Dictionary:` To create an empty dictionary, use:

```python
empty_dict = {}
```

`Indexing`

- Accessing Values: You can access values in a dictionary using their keys.

```python
print(my_dict['name']) # Output: Alice
```

- KeyError: If you try to access a key that does not exist, a KeyError will be raised.

```python
print(my_dict['gender']) # Raises KeyError
```

`Adding Keys`

- Adding New Key-Value Pairs: You can add new key-value pairs by assigning a value to a new key.

```python
my_dict['gender'] = 'Female'
```

- Updating Existing Keys: You can update the value of an existing key in the same way.

```python
my_dict['age'] = 26
```

`Removing Keys`

- Using del: You can remove a key-value pair using the del statement.

```python
del my_dict['age']
```

- Using `pop()`: You can also use the `pop()` method to remove a key and return its value.

age = my_dict.pop('age', None) # Returns None if 'age' doesn't exist

### 2. Iterating Through Dictionaries and Their Keys and Values

`Iterating Through Keys`

- You can iterate through the keys of a dictionary using a for loop.

```python
for key in my_dict:
print(key)

- Alternatively, you can use the keys() method:

for key in my_dict.keys():
print(key)
```

`Iterating Through Values`

- To iterate through the values, use the values() method.

```python
for value in my_dict.values():
print(value)
```

`Iterating Through Key-Value Pairs`

- To iterate through both keys and values, use the items() method.

```python
for key, value in my_dict.items():
print(f"{key}: {value}")

```

### 3. Checking the Existence of Keys

- You can check if a key exists in a dictionary using the in keyword.

```python
if 'name' in my_dict:
print("Key 'name' exists.")
```

- Alternatively, you can use the `get()` method, which returns `None` if the key does not exist (or a specified default value).

```python
age = my_dict.get('age', 'Not Found') # Returns 'Not Found' if 'age' doesn't exist
```

### 4. Methods: keys(), items(), and values()

-`keys()`: Returns a view object that displays a list of all the keys in the dictionary.

```python
keys = my_dict.keys()
print(keys) # Output: dict_keys(['name', 'gender'])
```

`values():` Returns a view object that displays a list of all the values in the dictionary.

```python
values = my_dict.values()
print(values) # Output: dict_values(['Alice', 'Female'])
```

- `items():` Returns a view object that displays a list of tuples, each containing a key-value pair.

```python
items = my_dict.items()
print(items) # Output: dict_items([('name', 'Alice'), ('gender', 'Female')])
```

### multi choice, Question with Answers

```python
1. What method would you use to retrieve all keys from a dictionary?

A) get_keys()
B) keys()
C) all_keys()
D) retrieve_keys()

Answer: B

2.If you try to access a key that does not exist in a dictionary, what will happen?

A) It will return None.
B) It will raise a KeyError.
C) It will create a new entry with a default value.
D) It will return an empty string.

Answer: B

3.Which of the following methods would you use to check if a key exists in a dictionary?

A) exists()
B) has_key()
C) in
D) contains()

Answer: C

4.What will be the output of the following code?

d = {'a': 1, 'b': 2}
print(d.get('c', 3))

A) None
B) 3
C) KeyError
D) 0

Answer: B

5. How can you remove a key from a dictionary?

A) delete key
B) remove(key)
C) del key
D) discard(key)

Answer: C

6. What does the items() method return?

A) A list of keys only.
B) A list of values only.
C) A list of tuples containing key-value pairs.
D) A dictionary.

Answer: C

7. Which of the following statements correctly adds a new key-value pair to a dictionary?

A) d.add('c', 3)
B) d['c'] = 3
C) d.insert('c', 3)
D) d.append('c', 3)

Answer: B

8. Consider the following code. What will be the output?

d = {'x': 1, 'y': 2}
for key, value in d.items():
    print(key, value)

A) x 1
y 2
B) 1 x
2 y
C) x y
1 2
D) y x
2 1

Answer: A

9. What will happen if you call the values() method on a dictionary?

A) It will return a list of keys.
B) It will return a list of values.
C) It will return a set of keys and values.
D) It will return a dictionary.

Answer: B

10. Which of the following is true about dictionary keys in Python?

A) They can be mutable types.
B) They must be unique.
C) They can be of any data type.
D) They cannot be strings.

Answer: B.
```

## PCEP-30-02 3.4 Operate with strings

### 1. Constructing Strings

- Strings in Python can be created using single quotes `(')`, double quotes `(")`, triple single quotes `(''')`, or triple double quotes `(""")`. Here are some examples:

```python
single_quote_string = 'Hello, World!'
double_quote_string = "Hello, World!"
triple_single_quote_string = '''This is a
multi-line string.'''
triple_double_quote_string = """This is also a
multi-line string."""

```

### 2. Indexing

- Strings in Python are indexed, meaning each character in a string has a position (index) starting from 0. You can access individual characters using their index:

```python
my_string = "Python"
print(my_string[0]) # Output: P
print(my_string[5]) # Output: n

```

- Negative indexing allows you to access characters from the end of the string:

```python
print(my_string[-1]) # Output: n
print(my_string[-2]) # Output: o

```

### 3. Slicing

- Slicing allows you to extract a portion of a string by specifying a start index and an end index. The syntax is `string[start:end]`.

```python
my_string = "Hello, World!"
print(my_string[0:5]) # Output: Hello
print(my_string[7:]) # Output: World!
print(my_string[:5]) # Output: Hello
print(my_string[-6:]) # Output: World!

```

### 4. Immutability

- Strings in Python are immutable, meaning once a string is created, it cannot be changed. Any operation that modifies a string will create a new string instead of altering the original. For example:

```python
original_string = "Hello"
new_string = original_string.replace("H", "J") # Creates a new string
print(original_string) # Output: Hello
print(new_string) # Output: Jello
```

### 5. Escaping Using the \ Character

- To include special characters (like quotes) within a string, you can use the backslash `(\)` to escape them:

```python
escaped_single_quote = 'It\'s a sunny day.'
escaped_double_quote = "She said, \"Hello!\""
```

### 6. Quotes and Apostrophes Inside Strings

- You can use different types of quotes to include quotes or apostrophes without escaping:

```python
quote_string = "He said, 'Python is great!'"
apostrophe_string = 'It\'s a beautiful day.'
```

### 7. Multi-line Strings

- Multi-line strings can be created using triple quotes. This is useful for long texts or documentation:

```python
multi_line_string = """This is a string that spans multiple lines.
It can contain both single ' and double " quotes."""

```

### 8. Basic String Functions and Methods

Python provides several built-in functions and methods to operate on strings:

- len(): Returns the length of the string.

```python
my_string = "Hello"
print(len(my_string)) # Output: 5

```

- str.lower(): Converts the string to lowercase.

```python
print(my_string.lower()) # Output: hello

```

- str.upper(): Converts the string to uppercase.

```python
print(my_string.upper()) # Output: HELLO

```

- str.strip(): Removes leading and trailing whitespace.

```python
whitespace_string = " Hello "
print(whitespace_string.strip()) # Output: Hello

```

- str.replace(old, new): Replaces occurrences of a substring.

```python
print(my_string.replace("H", "J")) # Output: Jello

```

- str.split(separator): Splits the string into a list based on the separator.

```python
sentence = "Python is fun"
print(sentence.split()) # Output: ['Python', 'is', 'fun']

```

- str.join(iterable): Joins elements of an iterable into a single string.

```python
words = ['Python', 'is', 'awesome']
print(" ".join(words)) # Output: Python is awesome
```

### Questions with Answers

#### 1.Constructing Strings

Q1: Which of the following is a valid way to create a string in Python?

`A) str = "Hello"`
`B) str = 'Hello'`
`C) str = '''Hello'''`
D) All of the above

Answer: D

Q2: What will be the output of the following code?

```python
s = "Hello" + " World"
print(s)
A) HelloWorld
B) Hello World
C) Hello + World
D) Hello, World

Answer: B

```

#### 2. Indexing, Slicing, Immutability

Q3: What will s[1] return if s = "Python"?

A) P
B) y
C) o
D) n

Answer: B

Q4: What will be the result of the following code?

```python
s = "Immutable"
s[0] = 'i'
A) iImmutable
B) Immutable
C) Error
D) Immutabl

Answer: C
```

#### 3. Escaping Using the \ Character

Q5: Which of the following strings contains an escape character?

A) "Hello"
B) "Hello\nWorld
C) "Hello World"
D) "'Hello'"

Answer: B

Q6: What will be the output of the following code?

```python
print("She said, \"Hello!\"")
A) She said, "Hello!"
B) She said, Hello!
C) She said, \"Hello!\"
D) Error

Answer: A

```

#### 4. Quotes and Apostrophes Inside Strings

Q7: How can you include a single quote in a string that is defined with single quotes?

A) s = 'It\'s a nice day'
B) s = 'It’s a nice day'
C) s = "It's a nice day"
D) Both A and C

Answer: D

Q8: What will be the output of the following code?

```python
s = 'He said, "It\'s fine."'
print(s)
A) He said, "It's fine."
B) He said, "It\'s fine."
C) He said, "Its fine."
D) Error

Answer: A

```

#### 5. Multi-line Strings

Q9: Which of the following is a valid multi-line string?

```python
A) s = "Hello\nWorld"
B) s = '''Hello\nWorld'''
C) s = "Hello World"
D) s = """Hello World"""

Answer: D

Q10: What will the output of the following code be?

s = """Line 1
Line 2"""
print(s)
A) Line 1 Line 2
B) Line 1\nLine 2
C) Line 1\nLine 2\n
D) Line 1\nLine 2

Answer: C
```

#### 6. Basic String Functions and Methods

Q11: What does the method s.lower() do?

A) Converts all characters in string s to uppercase
B) Converts all characters in string s to lowercase
C) Returns the original string
D) None of the above

Answer: B

Q12: What will be the result of the following code?

```python
s = "Python"
print(s.replace("P", "J"))
A) Jython
B) Python
C) Pjthon
D) JytHon

Answer: A
```
