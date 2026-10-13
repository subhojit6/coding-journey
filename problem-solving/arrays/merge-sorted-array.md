# LeetCode #88 — Merge Sorted Array

## Problem
Merge two sorted arrays into the first array in sorted order.

The first array has enough extra space at the end to hold all elements from the second array.

- `m` represents the number of valid elements in the first array.
- `n` represents the number of elements in the second array.

## Technique
**Two Pointers — Merge Backward**

Start from the ends of the valid portions of both arrays and place the larger value at the end of the first array.

### Pointer meanings
- `i = m - 1`: last valid element of the first array.
- `j = n - 1`: last element of the second array.
- `k = m + n - 1`: last available position in the destination array.

### Current Understanding
- The destination pointer starts at the end.
- Compare the values at `i` and `j`.
- Place the larger value at `k`.
- Move the pointer for the value that was used.
- Move `k` backward after each placement.
- Continue while `j >= 0`.

### Remaining Challenge
Finish the logic for when the first array's valid elements are exhausted while elements from the second array remain.

**Hint:** The remaining elements of the second array must still be copied into the first array.

## Complexity
Expected for the completed in-place solution:
- Time: `O(m + n)`
- Extra space: `O(1)`

## Edge Cases to Test
1. The second array is empty.
2. The first array has no valid elements.
3. Every element in the first array is smaller than the elements in the second.
4. Every element in the second array is smaller than the elements in the first.
5. Both arrays contain repeated values.

## Status
In progress — pointer logic and edge cases still need to be completed and tested.

## Revision Questions
1. Why do we merge from the end instead of the beginning?
ans. merging from the beginning may cause overwriting in some cases
2. What does each pointer (`i`, `j`, and `k`) represent?
ans. i pointer represents the last index value of the number which is a valuable number from the end of the first list. 
j pointer is to represent the last index value of the number from the end of the second list 
and k pointer is to place the larger value in that index position of nums1
3. Why is the loop condition `j >= 0` important?
ans. Because it should get all the values from the nums2 list to be added in nums1 list 
4. What happens when `i < 0` but `j >= 0`?
ans. when i gets less than zero we simply add all the remaining values from the nums2 list in to nums1.
