# 📌 Union of Arrays with Duplicates

## 🧩 Problem Statement
Given two arrays `a[]` and `b[]`, return the **Union** of both arrays.

The Union should contain **only distinct elements** present in either array.  
If an element appears multiple times, it should be included only once in the result.

---

## 💡 Approach Used: HashSet

To remove duplicates efficiently, we use a **HashSet**.

### Steps:
1. Create a `HashSet<Integer>` to store unique elements.
2. Traverse array `a[]` and add elements to the set.
3. Traverse array `b[]` and add elements to the same set.
4. Convert the set into an `ArrayList` and return it.

---

## 🧠 Why HashSet?

- Automatically removes duplicates.
- Average Time Complexity for insert: **O(1)**
- Clean and simple implementation.

⏱️ Time Complexity

O(n + m)
Where:

n = size of array a

m = size of array b

📦 Space Complexity

O(n + m) (for storing unique elements in HashSet)
