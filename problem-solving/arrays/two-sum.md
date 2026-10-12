# Two Sum

## 1. Problem Information

**Platform:** LeetCode  
**Topic:** Arrays and Hashing  
**Status:** Solved; needs revision

## 2. Understand the Problem

Given a list of integers and a target, find the indices of two different elements whose values add up to the target.

**Example:**

Input: `nums = [2, 7, 11, 15]`, `target = 9`

Output: `[0, 1]`

Because `nums[0] + nums[1] = 2 + 7 = 9`.

## 3. My First Thought

**Approach:** Brute force using nested loops.

Check pairs of elements until a pair adds up to the target.

**What I learned:** The straightforward solution is a useful starting point, even if it isn't the most efficient.

## 4. Brute-Force Solution

**Time complexity:** O(n²)  
**Extra space complexity:** O(1), excluding the returned answer.

**Why is it inefficient?**

The nested loops may check many pairs, resulting in quadratic time complexity.

## 5. Improved Solution

**Technique:** Hash map / dictionary.

For each number:
1. Calculate the complement: `target - current_number`.
2. Check whether that complement is already in the dictionary.
3. If found, return the two indices.
4. Otherwise, store the current number and its index.

**Time complexity:** O(n) average  
**Extra space complexity:** O(n)

**Why is it better?**

The dictionary lets me check whether the required complement has already appeared without scanning the entire list again.

## 6. Mistakes and Lessons

**Important distinction:** This solution uses hashing, not binary search.

**Key lesson:** When looking for a pair that adds up to a target, consider whether remembering previously seen values can avoid repeated searching.

## 7. Final Understanding

I first tried nested loops. Then I learned how a dictionary can store previously visited numbers and their indices.

I should be able to explain why the complement is calculated as `target - current_number` and why the dictionary improves the average time complexity.

## 8. Revision Tracker

- [ ] Solve Two Sum again without notes
- [ ] Explain the dictionary approach aloud
- [ ] Review after 3 days
- [ ] Review after 7 days
- [ ] Review after 14 days

## 9. Key Takeaway

Brute force helps me find a working approach. Hashing can help me avoid repeating work.