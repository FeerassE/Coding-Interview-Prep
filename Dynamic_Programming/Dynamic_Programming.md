# Dynamic Programming

Dynamic Programming is a difficult topic. This repository will document my understanding of this topic. 
Hopefully it will be of some use to you.

## What is Dynamic Programming?

"Dynamic programming is a technique for solving problems with overlapping subproblems."[<sup>3</sup>][3]

1. Problem has overlapping subproblems. Smaller problems are reused multiple times.
2. Problem has an optimal substrucutre. Optimal solution to smaller problems is optimal solution to entire the problem.

## How to idenfity a Dynamic Programming Problem
"The normal form of dynamic programming problem is to calculate the maximum or minimum"[<sup>1</sup>][1]

"The core of the problem is enumeration. Because we are asked to calculate the max or min, we must enumerate all the feasible answers and find max or min among those."[<sup>1</sup>][1]

#### First Characteristic:
Problem may ask you to find:
1. Find the min/max
2. Find the number of ways
3. Find the longest

#### Second Characteristic:
Earlier choices affect later choices. Such as using one element now prevents the use of another element later.

### *These two characteristics are not sufficient. There are more dp problems.

## Ways to Implement dp

Top-down (Memoization and Recursion):
 - Starts from the end case
 - Save the result of each case (in a hashmap or array)
 - If we see a case again, retrieve the case from the hashmap, thus no need to recalculate
 - slower runtime but easier to understand

Bottom-up (Tabulation and Iteration):
 - Start from the base case
 - runtime is usually faster, because no recursion overhead

## Elements of dp problem

1. State variable - contains data describing a relevant scenario to your problem
2. Function to solution given state
3. A recurrence relation to transition between states
4. Base cases to prevent infinite recursion

## Solving a dp problem

1. Find a recurrence relation
2. Create a recursive solution
3. Save underlying subproblems
4. Turn recursion into iterative loop

Core DP problems:

1. Climbing Stairs
2. House Robber  
   1. State: max amount possible at this house
   2. Recurrence: We take the amount from this house plus max amount two houses before or we take the max amount from the house before.<\br>
      ```dp[i] = max(house[i] + dp[i - 2], dp[i - 1])```
3. Min Cost Climbing Stairs
4. N-th Tribonacci Number
5. Longest Common Subsequence


## Problem Sets
https://leetcode.com/discuss/general-discussion/662866/Dynamic-Programming-for-Practice-Problems-Patterns-and-Sample-Solutions

### FootNotes:
1. https://labuladong.gitbook.io/algo-en/i.-dynamic-programming/analysisofdynamicprogramming
2.  https://leetcode.com/problems/house-robber/discuss/156523/From-good-to-great.-How-to-approach-most-of-DP-problems
3. https://www.pearson.com/us/higher-education/program/Levitin-Introduction-to-the-Design-and-Analysis-of-Algorithms-3rd-Edition/PGM223052.html

[1]: https://labuladong.gitbook.io/algo-en/i.-dynamic-programming/analysisofdynamicprogramming
[2]:  https://leetcode.com/problems/house-robber/discuss/156523/From-good-to-great.-How-to-approach-most-of-DP-problems
[3]: https://www.pearson.com/us/higher-education/program/Levitin-Introduction-to-the-Design-and-Analysis-of-Algorithms-3rd-Edition/PGM223052.html

