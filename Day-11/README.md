🟢 Equal Sum Span in Two Binary Arrays
📌 Problem Description

Given two binary arrays a1[] and a2[] of equal length, find the length of the longest span (i, j) such that:

Sum of elements in a1[i…j] == Sum of elements in a2[i…j]

If no such span exists, return 0.

💡 Example
Example 1
Input:
a1 = [0,1,0,0,0,0]
a2 = [1,0,1,0,0,1]

Output:
4
Example 2
Input:
a1 = [0,1,0,1,1,1,1]
a2 = [1,1,1,1,1,0,1]

Output:
6
🚀 Optimized Approach (Prefix Sum + HashMap)
🔹 Key Idea

Instead of comparing subarray sums directly:

Compute difference:

diff[i] = a1[i] - a2[i]

Now find the longest subarray with sum = 0 in the diff array.

Use:

Prefix Sum

HashMap to store first occurrence of prefix sum

🧠 Algorithm Steps

Initialize:

prefixSum = 0

maxLen = 0

HashMap<Integer, Integer>

Traverse arrays:

Update prefixSum using (a1[i] - a2[i])

If prefixSum == 0 → update maxLen = i + 1

If prefixSum seen before → update maxLen

Else store prefixSum index
⏱ Complexity Analysis
Complexity	Value
Time	O(n)
Space	O(n)
