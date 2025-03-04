# Strive for Excellence

## Contest Link
[Problem Link](https://toph.co/contests/training/kldhdrk)

## Tags
- **Combinatorics**
- **Dynamic Programming (DP)**

---

## Description

"Strive for Excellence" is the motto of Remians. Mr. Arnab, who seeks excellence in everything, attended his crush's marriage ceremony. While observing the beautiful lighting decorations, he noticed an interesting pattern in the lighting sequence.

A lighting sequence can be represented as an array of size `N`, where `a_i` represents the color of the `i-th` light bulb. An array is called **excellent** if for each color `x`, the indices having color `x` are written in increasing order, and the maximum difference between adjacent indices is at most `D`.

For example, the array `[4, 3, 1, 3, 4, 3]` is excellent for `D = 4`. The indices for color `4` are `[1, 5]`, for color `3` are `[2, 4, 6]`, and for color `1` is `[3]`. The highest adjacent difference of indices for each color is `4`, which satisfies the condition.

Given `K` different colored bulbs and `N` bulbs available for each color, the task is to determine how many different excellent arrays of size `N` are possible. Two arrays are considered different if there exists at least one index `i` where the colors differ. Since the answer can be very large, it should be printed modulo `10^9 + 7`.

## Input

- The input starts with a single integer `T` (1 ≤ T ≤ 100), denoting the number of test cases.
- Each test case consists of three space-separated integers:
  - `N` (1 ≤ N ≤ 100): The size of the array.
  - `D` (1 ≤ D ≤ 10): The maximum allowed difference between adjacent indices for the same color.
  - `K` (1 ≤ K ≤ 100): The number of different colors.

It is guaranteed that the sum of `N` and the sum of `K` over all test cases does not exceed `100`.

## Output

For each test case, print the case number in the format `"Case #t:"`, where `t` is the test case number, followed by the answer for that test case.

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

## Explanation

### Third Test Case
Some examples of excellent sequences are:

1. `[4, 3, 4, 2, 1, 1, 1]`:
   - For color `4`, the indices are `[1, 3]`.
   - For color `1`, the indices are `[5, 6, 7]`.
   - The highest adjacent distance is `2`.

2. `[4, 3, 4, 2, 1, 1, 2]`:
   - For color `4`, the indices are `[1, 3]`.
   - For color `2`, the indices are `[4, 7]`.
   - For color `1`, the indices are `[5, 6]`.
   - The highest adjacent distance is `3`.

## Constraints

- Time Limit: 1 second per test case.
- Memory Limit: 512 MB.
