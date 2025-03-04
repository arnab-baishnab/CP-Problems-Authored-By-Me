# Consistency Is the Key! [Easy, Math, Bruteforce]

## Contest Link
[7th DRMC International Tech Carnival 2024](https://toph.co/c/7th-drmc-international-tech-carnival-2024)

## Tags
- Math
- Bruteforce
- Simulation

## Problem Statement
A long, long time ago, there lived a hare in the forest who always boasted of his running speed. He would often tease the tortoise for
being the slowest animal around. One fine day, he dared the tortoise to a race in order to exhibit his skills in front of other animals in the forest.
Fed up with the hare’s bragging, the tortoise finally accepted the challenge and decided to compete with him in a race.

The hare has a serious procrastination factor. After each second, its speed decreases by half. That means if initially its speed is 1m/s,
then in the 1st second it will cross 1 meter, in the 2nd second it will cross 0.5 meters, and so on. On the other hand, the tortoise’s speed remains
constant.

You’re given the initial speed of the hare and the tortoise. You have to find the minimum integer number of seconds needed for the tortoise to beat
the hare.

## Input Format
- Input will start with a single integer **T** (1 ≤ T ≤ 10^6), denoting the number of test cases.
- Each test case will contain two space-separated integers **x** and **y**:
  - **x = 2^p** where **p** is an integer in the range **[0, 50]** (Initial speed of the hare in meters per second).
  - **y** (1 ≤ y ≤ 10^16) (Initial speed of the tortoise in meters per second).

## Output Format
For each test case, print the case number in the format:
```
Case #t: S
```
Where **t** is the test case number (starting from 1) and **S** is the minimum integer number of seconds needed for the tortoise to beat the hare.

## Sample Input
```
4
2 1
4 3
2 2
4 5   
```

## Sample Output
```
Case #1: 4
Case #2: 3
Case #3: 2
Case #4: 1
```

## Explanation
- **Test Case 1:** After 4 seconds, the hare’s position is (2 + 1 + 0.5 + 0.25) = **3.75 meters**, while the tortoise's position is (1 + 1 + 1 + 1) = **4 meters**. The tortoise cannot beat the hare in 3 or fewer seconds.
- **Test Case 3:** After 1 second, both have equal positions of **2 meters**. After 2 seconds, the hare reaches **3 meters**, and the tortoise reaches **4 meters**, overtaking the hare.
