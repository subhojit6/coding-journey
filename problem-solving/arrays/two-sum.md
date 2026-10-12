# DSA Problem: Two Sum

## Problem

Given a list of integers and a target value, return the indices of two different elements whose sum equals the target.

Example:

```python
nums = [2, 7, 11, 15]
target = 9
```

Expected result:

```python
[0, 1]
```

Because `nums[0] + nums[1] == 9`.

## Approach 1: Brute Force

### Idea

Check every possible pair of elements using nested loops.

### What I Learned

- List indices identify element positions.
- The inner loop can start at `i + 1` to avoid pairing an element with itself or checking the same pair twice.
- A straightforward solution helps establish the logic before optimizing.

### Complexity

- Time: O(n²)
- Auxiliary space: O(1), excluding the returned result.

## Approach 2: Dictionary / Hashing

### Idea

For each number, calculate the value needed to reach the target.

```python
complement = target - nums[i]
```

Check whether that complement has already been stored in a dictionary. If it has, the two indices have been found. Otherwise, store the current number and its index.

### Example

For `nums = [2, 7, 11, 15]` and `target = 9`:

1. Visit `2`; its complement is `7`. It has not been seen, so store `2`.
2. Visit `7`; its complement is `2`. The dictionary already contains `2`.
3. Return the indices of `2` and `7`: `[0, 1]`.

### Complexity

- Average time: O(n)
- Extra space: O(n)

## Technique

Hashing with a dictionary.

## Main Lesson

Instead of repeatedly searching the list for the complement, store previously seen values so they can be looked up efficiently.

## What I Need to Practice

- Write the dictionary solution without looking at previous code.
- Explain why the complement is `target - current_number`.
- Understand why checking before storing the current number prevents using the same element twice.
- Test negative numbers, repeated values, and cases where no valid pair exists.
- Follow the problem's required behavior when no solution exists.

## Status

Practiced both brute force and dictionary-based approaches. Continue practicing until I can independently implement and explain the optimized solution.