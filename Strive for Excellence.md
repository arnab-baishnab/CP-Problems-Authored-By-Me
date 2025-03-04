# Strive for Excellence

## Problem Statement  

“Strive for Excellence” is the motto of Remians.  

Mr. Arnab wants excellence in everything. One day, he attended his crush’s marriage ceremony. He was broken. Bearing pain in his heart, he was observing beautiful lighting decorations. All of a sudden, he found something interesting about the lighting sequence.  

A lighting sequence can be represented as an array of size **N**, where **aᵢ** represents the color of the **iᵗʰ** light bulb.  

An array is called **excellent** if for each color **x**, we write the indices having color **x** in increasing order like **b₁ < b₂ < b₃ < ... < bₘ**, then:

\[
\max_{j<m} (b_{j+1} - b_j) \leq D
\]

In other words, for each **j** such that **j < m**, the difference between **bⱼ** and **bⱼ₊₁** is at most **D**.  

### Example  

Consider the array:  

```
[4,3,1,3,4,3]
```

For **D = 4**, this array is **excellent** because:  

- The indices of color **4** are **[1,5]**  
- The indices of color **3** are **[2,4,6]**  
- The index of color **1** is **[3]**  

For each color, the highest adjacent difference of indices is at most **4**.  

## Task  

You are given **K** different colored bulbs, and there are **N** bulbs available of each color. Your task is to find the number of different **excellent arrays** of size **N** that can be formed.  

Two arrays **A** and **B** are considered different if there exists at least one index **i** such that **Aᵢ ≠ Bᵢ**.  

Since the answer can be large, return the result modulo **10⁹ + 7**.  

---

## Input Format  

- The first line contains a single integer **T** (**1 ≤ T ≤ 100**) — the number of test cases.  
- Each test case consists of three space-separated integers:  

  - **N** (**1 ≤ N ≤ 100**) → Size of the array  
  - **D** (**1 ≤ D ≤ 10**) → Maximum allowed distance between adjacent indices of the same color  
  - **K** (**1 ≤ K ≤ 100**) → Number of different colors available  

It is guaranteed that the sum of **N** and **K** over all test cases does not exceed **100**.  

---

## Output Format  

For each test case, print:  

```
Case #t: result
```

where **t** is the test case number (1-based index), and **result** is the number of excellent arrays modulo **10⁹ + 7**.  

---

## Sample Input  

```
5
5 4 5
8 2 1
7 3 4
5 3 5
5 3 10
```

## Sample Output  

```
Case #1: 3125
Case #2: 1
Case #3: 8692
Case #4: 2805
Case #5: 92710
```

---

## Explanation  

For the **third test case (N = 7, D = 3, K = 4)**, some valid **excellent sequences** are:  

```
[4,3,4,2,1,1,1]  → For color 4, indices are [1,3]  
                  → For color 1, indices are [5,6,7]  
                  → The highest adjacent difference is 2
```

```
[4,3,4,2,1,1,2]  → For color 4, indices are [1,3]  
                  → For color 2, indices are [4,7]  
                  → For color 1, indices are [5,6]  
                  → The highest adjacent difference is 3
```

---

## Constraints  

- **1 ≤ T ≤ 100**  
- **1 ≤ N ≤ 100**  
- **1 ≤ D ≤ 10**  
- **1 ≤ K ≤ 100**  
- The sum of **N** and **K** over all test cases does not exceed **100**.  

---

## Notes  

- The problem involves combinatorics and constraint handling.  
- Use **modular arithmetic** to avoid overflow issues.  
- Dynamic programming or backtracking may help in efficient computation.  

---

This **README** is now ready to be added to your repository. Let me know if you need any modifications! 🚀
