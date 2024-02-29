# DSA-Missing-Number
Given an array nums containing n distinct numbers in the range [0, n], return the only number in the range that is missing from the array.

```
Input: nums = [9,6,4,2,3,5,7,0,1]
Output: 8
Explanation: n = 9 since there are 9 numbers, so all numbers are in the range [0,9]. 8 is the missing number in the range since it does not appear in nums.
```
```
class Solution:
    def missingNumber(self, nums: List[int]) -> int:
        #converstion from list to set casue only unique numbers are avaialable, it will reduce time complexity from O(n2) to O(n) while iterating thru !!!!
        nums=set(nums)
        # iteration thru range of max len of input nums
        for i in range(len(nums)+1):
            # if iterated number not in range then it`s an answer
            if i not in nums:
                return i
```
Space complexity: O(1)
Time complexity: O(n)
