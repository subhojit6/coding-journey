# DSA Learning Progress — Python

## Goal

Learn to solve problems independently, recognize common patterns, and analyze time and space complexity.

My approach:
1. Understand the problem.
2. Try a brute-force solution.
3. Check edge cases.
4. Improve the solution when possible.
5. Explain the technique and complexity in my own words.

## 1. Complexity Analysis

**Status:** Practiced; continue strengthening

Topics:
- O(1): constant time.
- O(n): linear time.
- O(n²): quadratic time.
- Nested loops and their impact on runtime.
- Fixed-size loops inside another loop.
- Basic extra-space analysis.
- Difference between creating a new collection and modifying a list in place.

## 2. Arrays and Searching

### Largest Element

- Scan through the list while tracking the largest value.
- Initialize the largest value from an element in the list rather than assuming all numbers are positive.

### Linear Search

- Check elements one by one.
- Use a Boolean flag such as `found` when needed.
- Technique: linear search.
- Typical time: O(n).
- Extra space: O(1).

### Binary Search

- Practiced searching for a target in a sorted list.
- Used `left`, `right`, and `middle`.
- Learned to update the search boundaries and stop when the target is found.
- Technique: binary search.
- Time: O(log n).
- Extra space: O(1) for the iterative approach.
- Important condition: the input must be sorted.

## 3. Two Sum

Approaches explored:
- Brute force using nested loops.
- Dictionary-based lookup.

What I learned:
- For each number, calculate the complement: `target - current_number`.
- Check whether that complement has already been seen.
- Store values and their indices in a dictionary.

Brute force:
- Time: O(n²).
- Auxiliary space: O(1), excluding the returned result.

Dictionary approach:
- Average time: O(n).
- Extra space: O(n).

Technique: hashing with a dictionary.

## 4. Contains Duplicate

What I learned:
- Use a set to track values already encountered.
- If a value is already in the set, a duplicate exists.

Typical complexity:
- Time: O(n) average.
- Extra space: O(n).

Technique: hashing with a set.

## 5. Single Number

Approaches explored:
- Brute-force comparisons.
- A dictionary to count occurrences.
- A second pass to find the value whose count is one.

What I learned:
- Frequency counting records how often each value appears.
- A dictionary can store each value and its count.

Typical dictionary approach:
- Time: O(n).
- Extra space: O(n).

Technique: frequency counting and hashing.

## 6. Move Zeroes

Approaches explored:
- Create a separate list containing non-zero values.
- Modify the original list in place using a write index, then fill the remaining positions with zeros.

What I learned:
- A new list requires extra memory.
- An in-place solution can reduce auxiliary space.
- A write index tracks where the next non-zero value should go.

In-place approach:
- Time: O(n).
- Extra space: O(1).

Technique: array traversal and in-place modification.

## 7. Missing Number

Approaches explored:
- Compare array values with expected values.
- Use a set to check which number is missing.
- Use a mathematical sum formula.

Formula:

`expected_sum = n * (n + 1) // 2`

Then subtract the actual sum of the array.

What I learned:
- Different approaches can solve the same problem.
- A set uses additional memory.
- The sum formula avoids creating a separate collection.

Typical sum approach:
- Time: O(n).
- Extra space: O(1).

Assumption: the array contains distinct numbers from 0 through n, with exactly one number missing.

## 8. Minimum and Maximum

What I learned:
- Initialize both values from the first element.
- Traverse the list and update the minimum and maximum.
- Both values can be found in one traversal.

Time: O(n).
Extra space: O(1).

## 9. Second-Largest Distinct Element

**Status: Currently learning**

Cases to test:
- `[12, 35, 1, 10, 34, 1]` → `34`
- `[35, 35, 35, 34, 12, 10]` → `34`
- `[-8, -3, -10, -5]` → `-5`

Lessons to understand:
- The second-largest value must be distinct from the largest.
- Initializing values to zero fails for some negative-number inputs.
- Removing one occurrence of the maximum does not reliably handle duplicates.
- Track whether a second-largest value has been found.
- Decide what to return if no second-largest distinct value exists.

Next: complete the solution independently and explain why it works.

## Techniques Practiced

- Array traversal.
- Linear search.
- Binary search.
- Brute force.
- Hashing with sets.
- Hashing with dictionaries.
- Frequency counting.
- In-place array modification.
- Mathematical shortcuts.
- Time and space complexity analysis.

## Upcoming Topics

- More hashing and frequency-counting problems.
- Two pointers.
- Sliding window.
- Prefix sums.
- Stack and queue.
- Recursion.
- Linked lists.
- Trees.
- Heaps.
- Graphs.
- Dynamic programming.

## Learning Rule

Do not mark a problem as mastered just because a solution works once. Re-solve it without looking at the previous code and explain the technique, complexity, and edge cases.

## Progress Update — October 13, 2026

### LeetCode #283 — Move Zeroes

**Status:** Revisited and practiced

- Practiced moving non-zero values forward with a write pointer.
- Used a second pass to fill remaining positions with zeroes.
- Debugged a problem caused by modifying a list while iterating over it.
- Reinforced the difference between in-place modification and creating a new list.

Complexity:
- Time: O(n)
- Extra space: O(1)

### LeetCode #26 — Remove Duplicates from Sorted Array

**Status:** Solved and practiced

- Used two pointers to process a sorted array.
- Used a write pointer to place distinct values in the front portion of the array.
- Practiced modifying an array in place.

Complexity:
- Time: O(n)
- Extra space: O(1)

Key lesson: because the array is sorted, duplicate values appear next to one another.

### LeetCode #88 — Merge Sorted Array

**Status:** In progress

- Practiced merging sorted arrays from the end.
- Worked with the destination pointer `k = m + n - 1`.
- Corrected the loop condition to continue while `j >= 0`.
- Still need to finish handling the case where the first array's valid elements are exhausted.

Key lesson: merging backward helps avoid overwriting unprocessed values in the destination array.

### Techniques Added to My Practice

- Two pointers.
- Write pointers.
- Backward traversal.
- In-place array modification.
- Debugging pointer boundaries and loop conditions.

### Next DSA Priority

1. Finish Merge Sorted Array.
2. Test edge cases and explain the pointer movements.
3. Continue practicing array problems using two pointers.
4. Record time and extra-space complexity for each solution.