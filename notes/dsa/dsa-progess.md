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
**Status:** Completed

- Practiced merging two sorted arrays from the end.
- Used three pointers: `i`, `j`, and `k`.
- Used backward traversal to avoid overwriting unprocessed values.
- Completed the merge logic, including handling remaining elements.

**Complexity:**
- Time: O(m + n)
- Extra space: O(1)

**Key lesson:** When merging backward, continue copying any remaining elements from the second array if the first array's valid elements are exhausted.

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

# DSA Progress Update — October 22, 2026

## 1. Time and Space Complexity

### Concepts Studied
- O(1): constant time or auxiliary space.
- O(log n): logarithmic time, including binary search.
- O(n): linear time and auxiliary space.
- O(n log n): encountered when analysing sorting approaches.
- O(n²): quadratic time, commonly associated with nested loops.
- Time complexity versus auxiliary space complexity.
- In-place modification versus creating an additional collection.
- Best-case and worst-case time complexity.

### Important Lessons
- Sequential O(n) loops generally combine to O(n), not O(n²).
- A fixed number of variables requires O(1) auxiliary space.
- An additional list that grows with the input requires O(n) auxiliary space.
- Complexity analysis should account for the actual operations and additional memory used.

## 2. Arrays and Array Traversal

### Concepts Practised
- Iterating through arrays and Python lists.
- Tracking minimum and maximum values.
- Tracking the second-largest distinct value.
- Using read and write pointers.
- Modifying arrays in place.
- Traversing arrays from either direction.
- Recognising mathematical shortcuts that avoid unnecessary comparisons.

### Problems Practised
- Find the largest element.
- Find the second-largest distinct element.
- Find the largest difference between two numbers.
- Move Zeroes (#283).
- Remove Duplicates from Sorted Array (#26).
- Merge Sorted Array (#88).
- Squares of a Sorted Array (#977).
- Remove Element (#27).

### Key Lessons
- A single traversal can maintain useful information such as a minimum, maximum, or candidate.
- Sorted arrays provide useful properties for detecting duplicates and comparing values.
- A write pointer identifies where the next valid value should be stored.
- Backward traversal can prevent overwriting values that have not yet been processed.

## 3. Hashing, Sets, and Dictionaries

### Concepts Studied
- Set membership and duplicate detection.
- Dictionary key-value pairs.
- Hashing and the role of hash values in lookup.
- Frequency counting with dictionaries.
- Storing previously seen values.
- Using dictionaries to associate values with indices.
- Set intersection and deduplication.
- XOR cancellation for finding a unique element.
- Recognising when hashing can eliminate repeated searching.

### Problems Practised
- Contains Duplicate (#217).
- Two Sum (#1).
- Single Number (#136).
- Intersection of Two Arrays (#349).
- Majority Element (#169).
- Ransom Note (#383).

### Key Lessons
- Use a set when the main question is whether a value has been seen.
- Use a dictionary when a value needs associated information, such as an index or frequency.
- Frequency counting can replace repeated scans of an array.
- Set operations can simplify intersection problems.
- XOR has the property that equal values cancel when XORed together.
- A candidate produced by an algorithm is not automatically a valid answer unless the problem's assumptions guarantee it.

### Status Notes
- Intersection of Two Arrays (#349): completed using sets.
- Majority Element (#169): practised candidate tracking and reasoning about the majority guarantee.
- Ransom Note (#383): introduced; completion still needs to be confirmed.

## 4. Two Pointers and In-Place Techniques

### Concepts Studied
- Left and right pointers.
- Read and write pointers.
- Moving pointers based on comparisons.
- Filling an output array from right to left.
- Using sorted-array properties to reduce unnecessary comparisons.
- Understanding the role of each pointer rather than memorising pointer movements.

### Problems Practised
- Remove Duplicates from Sorted Array (#26).
- Merge Sorted Array (#88).
- Squares of a Sorted Array (#977).
- Two Sum II — Input Array Is Sorted (#167).
- Valid Palindrome (#125).

### Status Notes
- Merge Sorted Array (#88): completed.
- Squares of a Sorted Array (#977): completed using two pointers and a separate result array.
- Two Sum II (#167): practice started; completion needs confirmation.
- Valid Palindrome (#125): working toward a two-pointer solution that skips non-alphanumeric characters without constructing a cleaned string.

## 5. Searching and Sorting

### Concepts Studied
- Linear search.
- Binary search on sorted data.
- How binary search repeatedly reduces the search space.
- Comparing sorting-based approaches with set-based approaches.
- Recognising the time cost of sorting before scanning.

### Key Lesson
The appropriate approach depends on the input properties and the required output. Sorting, hashing, and pointer-based techniques have different time and space trade-offs.

## 6. Prefix Sums and Sliding Windows

### Concepts Studied
- Prefix sums as a way to store cumulative totals.
- Fixed-size sliding windows as a way to process consecutive groups of elements.
- The importance of understanding a technique before using it in a solution.

### Practice Candidates
- Range Sum Query — Immutable (#303).
- Maximum Average Subarray I (#643).

**Status:** Concepts introduced for practice. Individual problem completion should be recorded only after verifying the work.

## 7. Other Problem-Solving Techniques

### Mathematical Reasoning
For the largest-difference problem, recognised that the largest possible difference is the maximum value minus the minimum value. This avoids comparing every possible pair.

### Majority Candidate Tracking
Practised reasoning about a candidate for the majority element and why a candidate must be verified when the problem does not guarantee that a majority exists.

### General Problem-Solving Process
1. Understand what the problem asks.
2. Work through a small example manually.
3. Consider a straightforward solution.
4. Analyse its time and auxiliary space.
5. Identify repeated work or unnecessary operations.
6. Consider an appropriate optimisation.
7. Implement, test, and explain the solution.

## 8. Current Revision Priorities

- Strengthen auxiliary-space analysis.
- Practise dictionary frequency counting.
- Revisit two-pointer boundary conditions.
- Finish and verify unfinished problem attempts.
- Practise explaining the reasoning behind pointer movements.
- Revisit older problems periodically instead of restarting the entire DSA roadmap.

## 9. Documentation Rule

A problem should be marked **Completed** only when its solution has been implemented and tested sufficiently to support that status.

A topic being introduced or assigned for practice does not mean it has been mastered.

The objective is to build independent problem-solving ability, not simply to accumulate solved-problem counts.