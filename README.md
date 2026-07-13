# Move Zeroes

## Problem

Given an integer array `nums`, move all `0`s to the end while maintaining the relative order of the non-zero elements. The operation must be performed in-place without using an extra array.

### Example

**Input**

```
nums = [1,0,2,3,0,4,0,1]
```

**Output**

```
[1,2,3,4,1,0,0,0]
```

## Approach

This solution uses the **Two Pointer** technique.

* `i` traverses the array from left to right.
* `j` keeps track of the position where the next non-zero element should be placed.
* Whenever a non-zero element is found, it is swapped with the element at index `j`.
* After every swap, `j` is incremented.
* By the end of the traversal, all non-zero elements are at the beginning in their original order, and all zeros are moved to the end.

## Algorithm

1. Initialize `j = 0`.
2. Traverse the array using `i`.
3. If `nums[i]` is non-zero:

   * Swap `nums[i]` and `nums[j]`.
   * Increment `j`.
4. Continue until the end of the array.
5. The array is modified in-place.

## Complexity Analysis

**Time Complexity:** `O(n)`

* The array is traversed only once.

**Space Complexity:** `O(1)`

* No extra data structure is used; only a temporary variable is required for swapping.

## Key Concept

The pointer `j` always indicates the position where the next non-zero element should be placed. Swapping ensures that the relative order of non-zero elements is preserved while all zeros naturally move to the end.
