📦 Count Square Submatrices with Given Sum
📌 Problem Statement

Given a 2D matrix mat[][] and an integer x, count the number of square submatrices whose sum of elements is exactly equal to x.

🧠 Approach Used
✅ 2D Prefix Sum Technique

To efficiently calculate the sum of any square submatrix in O(1) time, we:

Build a 2D prefix sum matrix

Use it to compute the sum of every possible square submatrix

Compare each square’s sum with the given value x

🔎 Algorithm Explanation
Step 1: Build Prefix Sum Matrix

Each cell stores the sum of elements from (0,0) to (i,j).

Formula:

prefix[i][j] = mat[i][j] 
             + prefix[i-1][j] 
             + prefix[i][j-1] 
             - prefix[i-1][j-1]
Step 2: Check All Possible Squares

Try every possible square size from 1 to min(n, m)

For each top-left position (i, j)

Calculate bottom-right (r2, c2)

Use prefix sum to compute total in O(1)

If total == x → increment count

⏱ Time Complexity

Building prefix sum → O(n × m)

Checking all squares → O(min(n,m) × n × m)

Overall Time Complexity:

O(n × m × min(n,m))
📦 Space Complexity
O(n × m)   // for prefix array
