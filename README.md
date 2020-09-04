# Coding-Interview-Prep

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

## LeetCode Patterns and Strategies


Comparing Two Strings:
- use a frequency map
