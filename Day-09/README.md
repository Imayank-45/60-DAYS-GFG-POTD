📘 Subarray with Given XOR (Java)
🚀 Problem Statement

Given an integer array arr[] and an integer k,
find the total number of subarrays whose XOR is equal to k.

🧠 Approach

We use:

✅ Prefix XOR

✅ HashMap

✅ Optimized O(n) solution

🔹 Key Idea

If:

prefixXor ^ oldPrefixXor = k

Then:

oldPrefixXor = prefixXor ^ k

So while traversing the array:

Maintain prefixXor

Calculate required = prefixXor ^ k

If required exists in HashMap → increase count

Store current prefixXor in map

🔍 Example
Input
arr = [4, 2, 2, 6, 4]
k = 6
Output
4
Valid Subarrays
[4,2]
[2,2,6]
[6]
[2,2,6,4]
⏱ Time Complexity
O(n)

Single traversal

HashMap operations in O(1)

🗂 Space Complexity
O(n)

HashMap stores prefix XOR values

🎯 Why This Problem Is Important?

Frequently asked in interviews

Similar pattern to:

Subarray Sum Equals K

Prefix Sum problems

Strengthens understanding of:

Bitwise XOR

HashMap frequency technique

Pattern recognition in DSA


How to optimize brute force O(n²) to O(n)

How to use mathematical transformation in DSA
