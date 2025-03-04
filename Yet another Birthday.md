# Yet Another Birthday! - Problem Statement

## Contest Link
[CUSS Presents IT Fiesta 2024 Inter University Programming Contest
](https://toph.co/contests/training/rxbqtb6)

## Tags
- **Randomized Hashing**
- **Implementation**

---

## Description

Today is Archita’s birthday! A total of `M` people (including her) attended the birthday party. After blowing out the candles, she’s ready to cut the cake, but she’s unsure if it’s perfect.

A cake is **perfect** if it can be split into **at least `M` pieces**, each with the **same flavor**.

The birthday cake can be considered as an array of ingredients! Two pieces `a` and `b` have the same flavor if and only if the **multiset of the ingredients** of them are equal. For example:
- Pieces `a = {1, 2, 1, 3, 3}` and `b = {3, 1, 2, 3, 1}` have the same flavor.
- Pieces `p = {1, 1, 2, 5}` and `q = {3, 5, 1, 1}` differ.
- Pieces `x = {1, 2, 2}` and `y = {1, 1, 2}` differ.

Archita won’t cut the cake unless she’s sure that it’s perfect. Her elder brother, Arnab, is unable to come up with a solution as he’s out of practice! Can you help her? What is the **minimum length of prefix or suffix** (not both) to cut from the cake so that the remaining portion will be perfect?

---

## Input

- The input starts with a single integer `T` (1 ≤ T ≤ 10^5), denoting the number of test cases.
- Each test case consists of two lines:
  - The first line contains three space-separated integers:
    - `N` (1 ≤ N ≤ 10^6): The length of the array.
    - `M` (1 ≤ M ≤ 10^6): The number of people.
  - The second line contains `N` integers `a_1, a_2, ..., a_N` (1 ≤ a[i] ≤ 10^6): The elements of the array.

It is guaranteed that the sum of `N` and the sum of `M` over all test cases does not exceed 10^6.

---

## Output

For each test case, print `"Case t: answer"`, where `t` is the test case number, followed by the answer of that test case. If it’s impossible to find a solution, print `-1`.

---

## Sample Input

```
3
9 2
1 5 5 1 5 1 5 1 1
5 3
1 2 3 3 2
11 3
3 9 6 3 2 3 2 6 6 2 3
```

## Sample Output

```
Case 1: 1
Case 2: -1
Case 3: 2
```

---

## Explanation

### First Test Case
- **Option 1**: Removing the first three elements `[1, 5, 5]` leaves the array `[1, 5, 1, 5, 1, 1]`, which can be divided into two pieces of equal flavor: `[1, 5, 1]` and `[5, 1, 1]`.
- **Option 2**: Removing one element from the suffix `[1]` leaves the array `[1, 5, 5, 1, 5, 1, 5, 1]`, which can be divided into four equal-flavored parts: `[1, 5]`, `[5, 1]`, `[5, 1]`, and `[5, 1]` or into two equal-flavored parts: `[1, 5, 5, 1]` and `[5, 1, 5, 1]`.

Since removing one element from the suffix results in the minimum cut, the answer is `1`.

---

## Constraints

- Time Limit: 3 seconds per test case.
- Memory Limit: 512 MB.

---

This README provides a clear and structured explanation of the problem, including input/output formats, sample cases, constraints, and relevant tags. It ensures that the reader understands the problem and the requirements for solving it.
