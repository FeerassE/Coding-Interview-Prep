# DynamicProgramming

Dynamic Programming is a difficult topic. This repository will document my understanding of this topic. 
Hopefully it will be of some use to you.

## Dynamic Programming Overview
An overview of Dynamic Programming

### What is Dynamic Programming?

"Dynamic programming is a technique for solving problems with overlapping subproblems."[<sup>3</sup>][3]

1. Problem has overlapping subproblems. Smaller problems are reused multiple times.
2. Problem has an optimal substrucutre. Optimal solution to smaller problems is optimal solution to entire the problem.

### How to idenfity a Dynamic Programming Problem
"The normal form of dynamic programming problem is to calculate the maximum or minimum"[<sup>1</sup>][1]

"The core of the problem is enumeration. Because we are asked to calculate the max or min, we must enumerate all the feasible answers and find max or min among those."[<sup>1</sup>][1]

### First Characteristic:
Problem may ask you to find:
1. Find the min/max
2. Find the number of ways
3. Find the longest

### Second Characteristic:
Earlier choices affect later choices.

## Ways to Implement dp

Top-down (Memoization and Recursion):
 - Starts from the end case
 - Save the result of each case (in a hashmap or array)
 - If we see a case again, retrieve the case from the hashmap, thus no need to recalculate
 - slower runtime but easier to understand

Bottom-up (Tabulation and Iteration):
 - Start from the base case
 - runtime is usually faster, because no recursion overhead

## Solving a dp problem

1. Find a recurrence relation
2. Create a recursive solution
3. Save underlying subproblems
4. Turn recursion into iterative loop

## Problem Sets
https://leetcode.com/discuss/general-discussion/662866/Dynamic-Programming-for-Practice-Problems-Patterns-and-Sample-Solutions

### FootNotes:
1. https://labuladong.gitbook.io/algo-en/i.-dynamic-programming/analysisofdynamicprogramming
2.  https://leetcode.com/problems/house-robber/discuss/156523/From-good-to-great.-How-to-approach-most-of-DP-problems
3. https://www.pearson.com/us/higher-education/program/Levitin-Introduction-to-the-Design-and-Analysis-of-Algorithms-3rd-Edition/PGM223052.html

[1]: https://labuladong.gitbook.io/algo-en/i.-dynamic-programming/analysisofdynamicprogramming
[2]:  https://leetcode.com/problems/house-robber/discuss/156523/From-good-to-great.-How-to-approach-most-of-DP-problems
[3]: https://www.pearson.com/us/higher-education/program/Levitin-Introduction-to-the-Design-and-Analysis-of-Algorithms-3rd-Edition/PGM223052.html

