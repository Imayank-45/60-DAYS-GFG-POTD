🎨 Painter’s Partition Problem — Minimum Time (Java)
📌 Problem Statement

Given an array arr[] representing lengths of boards and an integer k representing number of painters.

Each painter can paint only continuous boards and all painters work at the same speed.

Your task is to find the minimum time required to paint all boards.

The time taken to paint a board is equal to its length.

🧠 Approach

This problem is solved using:

Binary Search on Answer + Greedy Checking

We do NOT search on array indices.
We search on time (answer space).

🔹 Key Observations

Minimum possible time = max board length
(because a painter must paint at least one full board)

Maximum possible time = sum of all board lengths
(one painter paints everything)

So answer lies between:

max(arr)  →  sum(arr)
⚙️ Algorithm
Step 1: Binary Search Range
start = max(arr)
end   = sum(arr)
Step 2: Check Feasibility (Greedy)

Try to assign boards to painters such that:
No painter paints more than mid time.

If painters required ≤ k → possible
Else → not possible
