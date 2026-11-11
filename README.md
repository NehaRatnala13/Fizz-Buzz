# Fizz-Buzz
Given an integer `n`, return a string array `answer` (1-indexed) where: * `answer[i] == "FizzBuzz"` if `i` is divisible by 3 and 5. * `answer[i] == "Fizz"` if `i` is divisible by 3. * `answer[i] == "Buzz"` if `i` is divisible by 5. * `answer[i] == i` (as a string) if none of the above conditions are true.
# LeetCode 412: Fizz Buzz 🔢✨

## Problem Description
Given an integer `n`, return a string array `answer` (**1-indexed**) where:
* `answer[i] == "FizzBuzz"` if `i` is divisible by `3` and `5`.
* `answer[i] == "Fizz"` if `i` is divisible by `3`.
* `answer[i] == "Buzz"` if `i` is divisible by `5`.
* `answer[i] == str(i)` (as a string) if none of the above conditions are true.

### Examples
**Example 1:**
* **Input:** n = 3
* **Output:** `["1","2","Fizz"]`

**Example 2:**
* **Input:** n = 5
* **Output:** `["1","2","Fizz","4","Buzz"]`

**Example 3:**
* **Input:** n = 15
* **Output:** `["1","2","Fizz","4","Buzz","Fizz","7","8","Fizz","Buzz","11","Fizz","13","14","FizzBuzz"]`

---

## Method Explanation
The solution loops sequentially from `1` to `n`. For each number, it checks divisibility using the modulo operator (`%`):
1. First, we evaluate if the number is divisible by both `3` and `5` (or `15`). This condition must come first to prevent a partial match by the standalone `3` or `5` checks.
2. Next, we check individual divisibility for `3` (`Fizz`) and `5` (`Buzz`).
3. If no conditions match, the loop falls back to converting the integer directly to a string.

---

## Complexity Analysis

| Metric | Complexity | Description |
| :--- | :--- | :--- |
| **Time Complexity** | **O(N)** | We iterate exactly once from 1 to N. |
| **Space Complexity** | **O(1)** | Excluding the output array, we only use a few boolean flags. |
