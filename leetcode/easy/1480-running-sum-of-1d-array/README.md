# Running Sum of 1d Array

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

Given an array `nums`. We define a running sum of an array as `runningSum[i] = sum(nums[0]…nums[i])`.

Return the running sum of `nums`.

 

Original
C++
 **Example 1:** 

```
Input: nums = [1,2,3,4]
Output: [1,3,6,10]
Explanation: Running sum is obtained as follows: [1, 1+2, 1+2+3, 1+2+3+4].
```

 **Example 2:** 

```
Input: nums = [1,1,1,1,1]
Output: [1,2,3,4,5]
Explanation: Running sum is obtained as follows: [1, 1+1, 1+1+1, 1+1+1+1, 1+1+1+1+1].
```

 **Example 3:** 

```
Input: nums = [3,1,2,10,1]
Output: [3,4,6,16,17]

```

 

 **Constraints:** 

- 1 <= nums.length <= 1000
- -10^6 <= nums[i] <= 10^6

## Solution

**Language:** C++  
**Runtime:** 1 ms (beats 14.66%)  
**Memory:** 12.6 MB (beats 10.17%)  
**Submitted:** 2026-11-26T08:04:00.261Z  

```cpp
class Solution {
public:
    std::vector<int> runningSum(std::vector<int>& nums) {
        // Start from the second element (index 1)
        for (int i = 1; i < nums.size(); ++i) {
            // Add the previous running sum to the current element
            nums[i] += nums[i - 1];
        }
        
        return nums;
    }
};
```

---

[View on LeetCode](https://leetcode.com/problems/running-sum-of-1d-array/)