📌 Push Zeros To End (Java)
📖 Problem Statement

Given an integer array, move all 0s to the end of the array while maintaining the relative order of non-zero elements.

You must do this:

✅ In-place (no extra array)

✅ O(n) time complexity

✅ O(1) space complexity

💡 Approach (Two Pointer Technique)

We use two pointers:

low → Points to the position where the next non-zero element should be placed.

high → Traverses the array.

🔹 Logic

Traverse the array using high.

If arr[high] is not zero:

Swap arr[low] and arr[high]

Increment low

Continue until end of array.

This ensures:

All non-zero elements shift left.

Zeros automatically move to the end.

Order is preserved.

🧠 Algorithm
Initialize low = 0
For high from 0 to n-1:
    If arr[high] != 0:
        Swap arr[low] and arr[high]
        Increment low

🔍 Example
Input:
[1, 0, 2, 0, 3]
Output:
[1, 2, 3, 0, 0]
⏱ Complexity Analysis
Complexity Type	Value
Time Complexity	O(n)
Space Complexity	O(1)
Stable Order	✅ Yes
