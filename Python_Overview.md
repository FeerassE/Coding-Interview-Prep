
# Python Overview

### Max and Min Numbers

```
# These are for initializing maximum and minimum values
Max Number:
float('inf')

Min:
float('-inf')
```

### Strings:
Essential information:

Python strings are immutable. They cannot be modified.

You must turn them into lists.

```
myString = "hello world"
myString = list(myString)
# >>> myString is ['w', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd']
# let's turn it back into a string
myString = "".join(myString)
print(myString)
# >>> myString is "hello world"
```

Declaration:<br>
myString = "hello world"

Find a substring:<br>
```
# find() returns the lowest index of a substring
myString.find(substringToFind, indexWhereToStartSearch, indexWhereToEndSearch)
```

Iterating over a string: <br>
```
for char in myString:
   print(char)
```

String concatenation:
```
myString = "hello "
newString = myString + "world"
print(myString)
# hello 
print(newString)
# hello world
```

### Data Type Conversion:
```
# convert a char to an int
myNum = ord('a')

# convert an int to a char
myChar = chr(97)

# convert an int to a string
myChar = str(97)
```

### Control Flow:
```
if x < 0:
   print('Negative')
elif x == 0:
   print('Zero')
elif x == 1:
   print('One')
else:
   print('More')
```

### Operators:
```
and

or

==

!=

<

>

<=

>=

```

### Arrays:

Lists are functionally arrays in Python. The List class
implements an array thus has slow inserts/fast appends.

Declaration:<br>
```myList = []```

Append:<br>
``` myList.append(3) ```

Insert:<br>
``` myList.insert(index, elem) ```

Remove at index:<br>
``` myList.pop(index) ```

Length of a list:<br>
```len(myList)```

Initialize:<br>
```
myList = [None for x in range(6)]
myList2D = [[None for x in range(6)] for y in range(6)]
```

Slicing:<br>
```
a = [0,1,2,3,4,5]
a = [includeFrom:excludeFrom]
a[1:]==[1,2,3,4,5]
a[:5]==[0,1,2,3,4]
a[1:2]==[1]
```

Loops:
```
for x in myList:
   print(x)
   
for i in range(len(x)):
   print(i)
  
while x > 5:
   x -= 1

# for loop with indexes
for i, x in enumerate(list):
   print(i)
   
# for loop starting at index 2
for item in myList[2:]:
    print(item)
    
# reverse for loop:
for i in range(len(myArray) - 1, -1, -1):
   print(i)
   
for i in myList[::-1]:
   print(i)

# range function arguments
for i in range(startIncluding, endExcluding, stepAdded):
   print(i)
```

2D Arrays:<br>
```
a = [[1, 2, 3], [4, 5, 6]]
a[0][1] == 2
a[0][0] == 1
a[1][0] == 4

for row in a:
   for elem in row:
      print(elem)
```

Sort:<br>
```
Ascending: myList.sort()
Descending: myList.sort(reverse = True)
```

List Comprehension: <br>
A great way to generate lists in a compact way.
```
# newList = [expression for item in list]
myList = [item * 2 for item in otherList]
```


### Dictionaries
Dictionaries are associative arrays implemented as hashtables in python

Declaration:<br>
``` myDictionary = {} ```

Existence check:<br>
``` 
if "myKey" in myDictionary:
   return True
```

Loops:<br>
```
#loop over a python dictionary
for key, value in d.items():
   print(key)
   print(value)

# key is a letter, the value is the furthest index of the letter in the string.
# loops over each letter in the string and saves the letter and the last position it was found in 
# the string, into the dictionary.

myDictionary = {letter:i for i, letter in enumerate(S)}
```

### Math

```
import Math

Math.sqrt(7) == 2.6457513110645907

Math.floor(2.6) == 2
Math.ceil(2.6) == 3
# Division
# Floor Division operator is //
5 / 2 >> 2
5.0 / 2 >> 2.5
5.0 // 2 >> 2
```

### Data Structres

#### Queue (FIFO):

Think of a queue to see a movie. 

First person to get In to the ine, is the First to go Out of the line to see the movie. (Thanks to a first year TA for that analogy)

First In First Out (FIFO)

List implementation (slow removal):

```
# Using a List is slow
myList = [10, 11, 12, 13, 14]

myList.pop(0) 
print(myList)
# >>> [11, 12, 13, 14]
# This is an O(N) operation because all elements must now be shifted to the left.

myList.append(15)
print(myList)
# >>> [11,12,13,14,15]
```
Queue implementation:

```
# This is Python's built in Queue module (library).

import queue

myQueue = queue.Queue()
# We call the queue constructor to build a Queue for us

myQueue.put("firstElement")
myQueue.put("secondElement)
print(myQueue.qsize())
# >>> 2
myQueue.get()
myQueue.get()
print(myQueue.qsize())
# >>> 0
print(myQueue.empty())
# >>> True
```

#### Stack (LIFO):
Last in first out.
Think of a stack of pancakes. The last pancake you put on the stack is the first one you can grab and eat. (Thanks to a first year TA for that analogy)
```
# Simply use .pop() and .append() on a list.
```

#### Heap/Priority Queue:
A heap is a binary tree where each node has the smallest value in it's subtree (aka among all it's children).
A heap and priority queue are the same I believe.

```
# You can use an empty list as a heap or call the heapify function on a list to turn it into a heap in place.

h = []
heapify(h)

# heappush to push item onto heap
heapq.heappush(h, item)

# heappop to return smallest item in heap
heapq.heappop(h)

```

### Python Tips and Tricks

### Destructure

[Helpful guide](https://blog.teclado.com/destructuring-in-python/)

Destructuring in python means breaking composite strucutres into their individual parts. <br>

```
# Tuples are represented by a comma, and we are breaking the tuple below into separate parts:
x, y = 5, 2
# or
x, y = (5, 2)

# Using enumerate returns an enumerate objects which contains a tuple for each item in the collection.
# Each tuple contains a counter and the value from the original collection.

myList = ["A", "B", "C"]

for counter, letter in enumerate(myList):
   print(str(counter) + " " + letter)

# >>> 0 A
# >>> 1 B
# >>> 2 C
```


### Use Asterick to Unpack Iterable
```
>>> fruits = ['apple ', 'orange ', 'banana ', 'pear ']
>>> print(*fruits)
apple orange banana pear
```
