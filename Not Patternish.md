# Not Patternish 

## Contest Link
[PSTU IT Carnival Programming Contest 2024 (South Zone)](https://toph.co/c/pstu-it-carnival-2024-south-zone)

## Tags
- **Stopper**
- **Matrix Exponentiation**

---

## Description

Given a **circular array** of `N` integers indexed from `0` to `N-1`, the array changes every second according to the following rule:

For each `i` (0 ≤ i ≤ N-1), the new value of `a_i` is given by:
```
a_i = a_{(i-1+N) % N} ⊕ a_{(i+1) % N}
```
where `⊕` denotes the **bitwise XOR operation**. All elements are updated **simultaneously** at each second based on the values from the previous second.

Your task is to determine the value of the array after `Z` seconds.

---

## Input

- The first line contains a single integer `T` (1 ≤ T ≤ 50), the number of test cases.
- For each test case:
  - The first line contains two integers `N` (1 ≤ N ≤ 200) and `Z` (1 ≤ Z ≤ 10^8), the size of the array and the number of seconds.
  - The second line contains `N` integers `a_1, a_2, ..., a_N` (0 ≤ a_i ≤ 10^18), the elements of the array.

It is guaranteed that the sum of `N` over all test cases does not exceed `200`.

---

## Output

For each test case, output `N` integers — the value of the array after `Z` seconds.

---

## Sample Input 1

```
1
5 3
3 1 2 3 2
```

## Sample Output 1

```
2 0 3 2 3
```

---

## Sample Input 2

```
1
6 5
5 5 7 1 7 9
```

## Sample Output 2

```
12 2 4 0 8 2 
```

---

## Constraints

- Time Limit: 1 second per test case.
- Memory Limit: 512 MB.
