# Coding Interview Prep

This repo will help me track my progress as well as serve as a place to summarize my notes as I prepare for coding interviews. 

This repo will be most helpful to you if you have already taken a data structure and algorithms course or are familiar with those concepts.

If you haven't, try one of these:

- [ ] [Abdul Bari's Algorithms course is excellent](https://www.youtube.com/playlist?list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O)

- [ ] [MIT 2011 algorithms course](https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=2&t=0s)


"When I consider everything that grows<br>
Holds in perfection but a little moment;"

LeetCode Problems solved: **76**

AlgoExpert Problems solved: **43**

## Tasks:
- [ ] Review any data structures with weak understanding
   - [ ] [Hash Table](https://www.youtube.com/watch?v=mFY0J5W8Udk)

- [x] [Review coding patterns article](https://hackernoon.com/14-patterns-to-ace-any-coding-interview-question-c5bb3357f6ed) (**briefly** read through)
  - [x] sliding window (ex: Maximum sum subarray of size 'K')
  - [x] Two Pointers or Iterators (ex: Square a sorted array) (usually sorted array or datastructure)
  - [x] Fast and Slow pointers (ex: Palindrome Linked List, Determine if cycle)
  - [x] Merge Intervals (ex: Intervals Intersection)
  - [x] Cyclic sort
  - [x] In-place reversal of linked list
  - [x] Tree BFS
  - [x] Tree DFS
  - [x] Find the Median of a Number Stream
  - [x] Subsets
  - [x] Modified binary search
  - [x] Top K elements (ex: Top ‘K’ Numbers)
  - [x] K-way Merge (Merge K Sorted Lists)
  - [x] Topological sort (Task scheduling)

- [ ] [Review Binary Search](https://www.youtube.com/watch?v=C2apEw9pgtw) (only check off when you can recreate from memory)
   - https://leetcode.com/problems/binary-search/discuss/423162/Binary-Search-101-The-Ultimate-Binary-Search-Handbook
   - https://leetcode.com/problems/koko-eating-bananas/discuss/769702/Python-Clear-explanation-Powerful-Ultimate-Binary-Search-Template.-Solved-many-problems.

- [ ] [Review Breadth First and Depth First Search](https://www.youtube.com/watch?v=pcKY4hjDrxk) (only check off when you can recreate from memory)

- [ ] Review sorting algorithms by recreating (only check off when you can recreate from memory)
  - [ ] [MergeSort](https://www.youtube.com/watch?v=mB5HXBb_HY8)
  - [ ] [QuickSort](https://www.youtube.com/watch?v=7h1s2SojIRw)
  
  
## Big O notation
provides an upperbound (worst case)


## Miscellaneous Info
ASCII values:
- lowercase 'a': decimal 97
- uppercase 'A': decimal 65

BitWise Operations:
XOR(^):<br>
1 ^ 1 = 0<br>
0 ^ 0 = 0<br>
1 ^ 0 = 1<br>
0 ^ 1 = 1<br>

a ^ b = c<br>
c ^ a = b<br>
c ^ b = a<br>

## Python3 Specific Info

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



### Graphs

#### Depth First Search

```
# Recursive
def dfs(node, visited)
   if visited is None:
      visited = set()
      
   visited.add(node)
   
   for child in node.children:
      dfs(child, visited)

# Iterative (use a stack)
# pop node from stack
# add the last unvisited child to stack
# once all children visited, say node is visited

# this needs TESTING
def dfs(tree, visited)
   if visited is None:
      visited = set()
   
   stack = [tree]
   
   while(len(stack)):
      node = stack.pop()
      for child in node.children:
         if child not in visited:
            stack.append(node)
            stack.append(child)
            continue
      visited.add(node)
```
#### Breadth First Search


```
# Recursive (need to check if this is correct)
import queue
def bfs(node, queue):
   for child in node.children:
      queue.put(child)
   
   if len(queue):
      bfs(queue.get(),queue)

# Iterative
import queue
def bfs(tree):

   queue = queue.Queue()
   queue.put(tree)
   
   while(len(queue)):
      node = queue.get()
      
      for child in node.children:
         queue.put(child)
```

#### PreOrder, InOrder, PostOrder Traversal
Look at where the print statements are.
```
# Preorder Traversal

def traverse(tree):
   if tree:
      print(tree)
      traverse(tree.left)
      traverse(tree.right)
      
# Inorder Traversal

def traverse(tree)
   if tree:
      traverse(tree.left)
      
      print(tree)
      traverse(tree.right)
      
# Postorder Traversal

def traverse(tree)
   if tree:
      traverse(tree.left)
      traverse(tree.right)
      print(tree)
```


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

## Java Specific Info
Math Functions:<br>
``` Math.pow(a,b); // returns a double, so make sure to type cast to int (int) ```<br>
Sort an array<br>
```Arrays.sort(nameOfArray);```

Arrays<br>
int array<br>
``` int a[] = new int[5] ```

List is an interface in Java. You need to instantiate the actual implementation, be it ArrayList or LinkedList, to use a List.<br>
``` List<String> myList = new ArrayList<String>(); ```<br>
``` myList.get(0); // Access first element ```<br>
``` myList.add(5); // Add five as an element ```<br>
``` myList.remove(0); // Remove first element ```<br>
``` myList.size(); // Gets the Length ```<br>

2D Arrays<br>
``` List<List<Integer>> list = new ArrayList<List<Integer>>(); ```<br>
Then add rows when necessary<br>
``` list.add(new ArrayList<Integer>()); ```<br>


Sets:<br>
``` Set<Integer> set = new HashSet<Integer>(); ``` <br>
associated functions: contains(value);

Maps<br>
``` Map<String, Integer> myHashMap = new HashMap<String, Integer>(); // key value pairs```

## Sorting Algorithms
- Abdul Bari QuickSort https://www.youtube.com/watch?v=7h1s2SojIRw


## Patterns and Strategies

### List of problems
- Leetcode Patterns https://seanprashad.com/leetcode-patterns/
- TeamBlind curated list https://www.teamblind.com/post/New-Year-Gift---Curated-List-of-Top-75-LeetCode-Questions-to-Save-Your-Time-OaM1orEU

### Comparing Two Strings:
- use a frequency map

### Dynamic Programming:
Excellent beginner video https://www.youtube.com/watch?v=oBt53YbR9Kk
```
    Types of Problems
    0/1 Knapsack
    Unbounded Knapsack
    Shortest Path (eg: Unique Paths I/II)
    Fibonacci Sequence (eg: House Thief, Jump Game)
    Longest Common Substring/Subsequeunce
```
- Kadane's Algorithm: https://medium.com/@rsinghal757/kadanes-algorithm-dynamic-programming-how-and-why-does-it-work-3fd8849ed73d
- list of beginner DP problems: https://leetcode.com/discuss/general-discussion/662866/DP-for-Beginners-Problems-or-Patterns-or-Sample-Solutions
- list of DP problems: https://leetcode.com/discuss/general-discussion/1000929/solved-all-dynamic-programming-dp-problems-in-7-months
- Abdul Bari's dynamic programming video https://www.youtube.com/watch?v=5dRGRueKU3M
- Break down of how to attempt a DP question: https://leetcode.com/problems/target-sum/discuss/455024/DP-IS-EASY!-5-Steps-to-Think-Through-DP-Questions
- Dynamic Programming Pattern article: https://leetcode.com/discuss/general-discussion/458695/Dynamic-Programming-Patterns
- Guide on how to solve DP problems: https://leetcode.com/discuss/study-guide/1490172/Dynamic-programming-is-simple

## Behavioural Questions:
- What are you looking for in your next role? Why this company?
- Tell me about a time when you had to work with a cross-functional team to solve a problem.
- Tell me about a time when you demonstrated a bias for action.
- Tell me about a time when you took ownership of a project or process and improved it.
- Tell me about a time when you had to deal with ambiguity.
- Tell me about a time when you disagreed with someone or had to resolve a disagreement.
- Tell me about a time when you led a project that failed. Why did it fail and what did you learn?
- What is your management style?
- How do you know that your team is working optimally?
- How do you handle low-performers?
- How do you approach solving complex problems?
- How do you evaluate buying vs. building technology?
- What is your approach to recruiting talent?

