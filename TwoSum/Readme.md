## 1. Two SUM

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
You can return the answer in any order.

# Example 1:
Input: nums = [2, 7, 11, 15], target = 9

Output: [0, 1]

Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

# Example 2:
Input: nums = [3, 2, 5], target = 7

Output: [1, 2]

# Example 3:
Input: nums = [3, 3], target = 6

Output: [0, 1]

## Explanation

![image](https://github.com/IshanKarki/LeetCodes/assets/44771554/daf6f63f-bc5d-49e6-9993-bf87687daff2)

_Big-O Complexity Chart: http://bigocheatsheet.com/_

As we can see the **Brute Force Approach** is a bit slow on time complexity with a **O(n^2)** as every element will have to check for every other element in the list without repetition, 

# For Example,

if nums = [ 2, 7, 11, 15] then here the first element nums[0] = 2 will have to iterate through every other element 7, 11 & 15 to check if their addition matches to the specified target, here its target = 9, thus we get output of [0, 1] as the number 2 and 7 in the list add up to target 9, and they are in index 0 and 1 respectively. Thus, there's almost always more than one way to solve a problem. The algorithm with the least time complexity is optimal than the other.

Hence, here in Brute Force, the time complexity is **(n * n)** as every element checks its way to every other element. 
Thus, in LeetCode it took about _**1687 ms**_ of time complexity and around _**17.3 MB**_ space complexity to solve this problem. 

This problem is better optimized using a hash table.

The Hash Table method of solving the two sum problem is optimal than brute force approach as the time complexity it takes is just **O(n)**.
Here, in hash table we map the elements in the nums list and their respective index as key-value pair in the numMap dictionary. We then, find the complement by subtracting the first element in the nums list from the target and then check if that complement value is a key in the numMap hash table, that way we eliminate our execution of the program but just checking the right numbers. 

# For Example,

    if nums = [2, 7, 11 15] then the first element nums[0] = 2 will be taken and subtracted from the target and the value obtained is stored as complement.

    complement =  9 - 2 = 7, now we then check if that complement = 7 is in numMap.
    for understanding numMap hash table, it's like this:

    numMap = {

    2 : 0,

    7 : 1,

    11 : 2,

    15 : 3

    }
 
Now, we check if complement = 7 is in numMap i.e key in numMap and yes we have it, so we get the index of it as 1 and return [0, 1]

# Now for repetition we do 
    
		'_**numMap[complement] != i**_'  
		for cases like nums = [3, 3] and target = 6

    numMap = {

    3 : 0,

    3 : 1

    }

Here, complement = target - first element

    complement = 6 - 3 = 3

Now, this complement = 3 will be checked in numMap we have two 3, thus to avoid repetition, we don't want the complement to be same as the current index i, thus now we get the answer,
[0, 1]

Thus, in LeetCode it took about _**62 ms**_ of time complexity and around _**17.8 MB**_ space complexity to solve this problem.

This is about _****27 times**** faster_ than that with brute force approach, although it took about _**0.5 MB** more space_.


