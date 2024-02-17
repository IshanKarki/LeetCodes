# Number of Good Pairs / Identical Pairs
Given an array of integers **_nums_**, return the **_number of good pairs_**.

**A pair ( i, j ) is called good if nums[ i ] == nums[ j ] and i < j.**


    Example 1:
    Input: nums = [1,2,3,1,1,3]
    Output: 4
    Explanation: There are 4 good pairs (0,3), (0,4), (3,4), (2,5) 0-indexed.

    Example 2:
    Input: nums = [1,1,1,1]
    Output: 6
    Explanation: Each pair in the array are good.

    Example 3:
    Input: nums = [1,2,3]
    Output: 0

I solved the solution with two approaches, for one being time complexity of **O( n )** and the other being **O( n ^ 2)**, only to find out that both solutions have the time complexity of **O( n ^ 2)**.
First one is the basic common nested loop solution, and the other is by using the **_count( )_** method. But later I learned as I got similar results for time complexity
of both programs in LeetCode, hence I checked it for myself. 

I checked it on https://www.bigocalc.com/
For the first program,


    class Solution1:
      def numIdenticalPairs(self, nums):
        pair = 0
        for i in range(x):
          for j in range(i+1, x):
            if nums[i] == nums[j]:
              pair += 1

      return pair 
It said,
![image](https://github.com/IshanKarki/LeetCodes/assets/44771554/679ad861-2a47-4484-b80a-334becd09623)

For the second program,

    class Solution2:
      def numIdenticalPairs(self, nums):
        pair = 0
        num = nums.copy() # we make a copy of the original to make no changes to the original list/array
        for i in range(x):
          pair += num.count(nums[i]) - 1 
          if num.count(nums[i]) > 1:
            num.remove(nums[i])
    
      return pair
This is what it said,


![image](https://github.com/IshanKarki/LeetCodes/assets/44771554/5b92e0c6-ef0f-4ed7-877e-fde9ba38fe46)

__Note_:_ Both codes are on the notebook file, first being the regular nested loop approach and the other being the **_count( )_** method.
