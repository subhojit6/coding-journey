# DSA Problem: Second-Largest Distinct Element

## Problem

Given a list of integers, find the second-largest distinct value.

Examples:

```python
nums = [12, 35, 1, 10, 34, 1]
# Expected: 34
```

```python
nums = [35, 35, 35, 34, 12, 10]
# Expected: 34
```

```python
nums = [-8, -3, -10, -5]
# Expected: -5
```

## Approaches I Explored

- Finding the largest value first and then looking for another value.
- Considering removing the maximum value.
- Tracking the largest and second-largest values in variables.
- Using `None` to represent a second-largest value that has not been found yet.

## Lessons to Understand

### 1. Distinct Values

The second-largest value must be smaller than the largest value.

If the maximum is `35`, another occurrence of `35` is not the second-largest distinct value.

### 2. Initial Values

Initializing the largest values to `0` can fail when every number is negative.

A safer approach is to initialize the largest value from the first list element, then handle the second-largest value separately.

### 3. Edge Cases

Test:
- Duplicate maximum values.
- Negative numbers.
- A list containing only one distinct value.
- A list with just one element.
- An empty list, if the program is expected to handle it.

Decide how the program should behave when no second-largest distinct value exists.

## Technique

Array traversal and maintaining the largest two distinct values.

## Complexity Goal

Aim for:
- Time: O(n), using one traversal.
- Extra space: O(1).

## Current Status

Still practicing. The goal is to implement the solution independently and explain why it handles duplicates and negative numbers correctly.

## Questions to Answer

- Why is initializing the largest value to zero unsafe?
- Why must the second-largest value be distinct?
- What should happen if no second-largest distinct value exists?
- How can both values be maintained without sorting the list?

## Next Step

Solve the problem independently, test every example above, and update this file with the final approach and any mistakes I learned from.