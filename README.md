# Leetcode-2965.-Find-Missing-and-Repeated-Values
# Description
You are given a 0-indexed 2D integer matrix grid of size n * n with values in the range [1, n2]. Each integer appears exactly once except a which appears twice and b which is missing. The task is to find the repeating and missing numbers a and b.

Return a 0-indexed integer array ans of size 2 where ans[0] equals to a and ans[1] equals to b.

# Solution
The problem states that we are given a 2D matrix whose length is that of the number of elements present.

In the array there are elements ranging from [1,n] , where n is the length of the grid . We have to find a repeated value and a missing value .


Example:

Input: grid = [[9,1,7],[8,9,2],[3,4,6]]

Output: [9,5]

Explanation: Number 9 is repeated and number 5 is missing so the answer is [9,5].

# Algorithm
1. Let n be the size of the grid.
2. Create a hash map freq to store how many times each number appears.
3. Initialize two variables: repeated = 0 and missing = 0.
4. Loop through each row in the grid.
5. For each number in the row, increment its count in the freq map.
6. After filling the frequency map, loop from 1 to n * n.
7. If a number appears twice (freq[i] == 2), assign it to repeated.
8. If a number is missing (freq[i] == 0), assign it to missing.
9. Return the result as a vector: {repeated, missing}.
# Time Complexity
Traversing the entire n x n grid takes O(n²) time.

Counting frequencies using a hash map is done in a single pass — O(n²) operations.

Looping from 1 to n² to find the repeated and missing numbers also takes O(n²) time.

Total Time = O(n²) + O(n²) = O(n²)
