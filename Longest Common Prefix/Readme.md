# Longest Common Prefix

Write a function to find the _**longest common prefix**_ **_string_** amongst an **array of strings**.

If there is no common prefix, return an empty string "".

 

    Example 1:
    Input: strs = ["flower","flow","flight"]
    Output: "fl"

    Example 2:
    Input: strs = ["dog","racecar","car"]
    Output: ""
    Explanation: There is no common prefix among the input strings.

    Example 3:
    Input: strs = ["account", "accompany", "a"]
    Output: "a"

    Example 4:
    Input: strs = ["go", "google", "goofie"]
    Output: "go"

We solve the solution with vertical scanning approach, as it has the least time complexity of **O(N)**, we can also approach the LCP problem with Divide and Conquer which have the time complexity of **O(k)**, where **k** is the sum of all the characters in the string, which is same as the **O(N)** and Binary Search with the time complexity of **O(k.logN)**. 
