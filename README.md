# Coding Interview Prep

This repo will help me track my progress as well as serve as a place to summarize my notes as I prepare for coding interviews. 

This repo will be most helpful to you if you have already taken a data structure and algorithms course or are familiar with those concepts.

If you haven't, try one of these:

- [ ] [Abdul Bari's Algorithms course is excellent](https://www.youtube.com/playlist?list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O)

- [ ] [MIT 2011 algorithms course](https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=2&t=0s)


"When I consider everything that grows<br>
Holds in perfection but a little moment;"

LeetCode Problems solved **38**:

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

### Strings:

Declaration:<br>
myString = "hello world"

Find a substring:<br>
```
# find() returns the lowest index of a substring
myString.find(substringToFind, indexWhereToStartSearch, indexWhereToEndSearch)
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

## Patterns and Strategies

### List of problems
- https://seanprashad.com/leetcode-patterns/


### Comparing Two Strings:
- use a frequency map

### Dynamic Programming:

```
    Types of Problems
    0/1 Knapsack
    Unbounded Knapsack
    Shortest Path (eg: Unique Paths I/II)
    Fibonacci Sequence (eg: House Thief, Jump Game)
    Longest Common Substring/Subsequeunce
```

- Excellent beginner video https://www.youtube.com/watch?v=oBt53YbR9Kk <br>
- Break down of how to attempt a DP question: https://leetcode.com/problems/target-sum/discuss/455024/DP-IS-EASY!-5-Steps-to-Think-Through-DP-Questions.






