# LeetCode #26 — Remove Duplicates from Sorted Array

## Problem
Given a sorted array, remove duplicates in place and return the number of unique elements.

The first `k` elements of the modified array should contain the unique values, where `k` is the returned length.

## Example
Input: `[1, 1, 2]`

Expected unique length: `2`

First two elements after modification: `[1, 2]`

## Technique
**Two Pointers — Write Pointer**

- One pointer scans through the array.
- Another pointer tracks where the next unique value should be written.
- Since the array is sorted, duplicate values appear next to each other.
- Modify the existing array instead of creating another array.

## Complexity
- Time: `O(n)`
- Extra space: `O(1)`

## Key Learning
- Sorted arrays make duplicate detection easier.
- Two pointers can help modify arrays in place.
- The returned length tells us how many elements in the array's prefix are valid unique values.

## Status
Solved and practiced.

## Revision Questions
1. Why does sorting help us identify duplicates?
ans. sorting sorts the data in ascending order or descending order where we can detect the duplicates easily.
2. What does the write pointer track?
ans. the write pointer tracker the next unique number in the list
3. Why is the extra space `O(1)`?
ans. Because we are not using any extra list set or hashmap just a single variale storing the index value
4. Why do we return the unique count instead of a new list?
ans. a new list is a increase in a extra space which then will be of O(n) space complexity.
