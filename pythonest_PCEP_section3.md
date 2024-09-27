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

matrix = [
[1, 2, 3],
[4, 5, 6],
[7, 8, 9]
]

#### Accessing elements in a matrix

element = matrix[1][2] # 6

#### Cube (3D list)

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
