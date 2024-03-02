# Equal Row and Column Pairs
Given a 0-indexed n x n integer matrix grid, return the number of pairs (ri, cj) such that row ri and column cj are equal.

A row and column pair is considered equal if they contain the same elements in the same order (i.e., an equal array).

 

    Example 1:
![image](https://github.com/IshanKarki/LeetCodes/assets/44771554/31ecd19e-c780-49ca-a651-47d10b3d5b0b)

    Input: grid = [[3,2,1],[1,7,6],[2,7,7]]
    Output: 1
    Explanation: There is 1 equal row and column pair:
    - (Row 2, Column 1): [2,7,7]



    Example 2:
![image](https://github.com/IshanKarki/LeetCodes/assets/44771554/10dd92ec-ee0c-4bfd-b442-375af18d6a10)

    Input: grid = [[3,1,2,2],[1,4,4,5],[2,4,2,2],[2,4,2,2]]
    Output: 3
    Explanation: There are 3 equal row and column pairs:
    - (Row 0, Column 0): [3,1,2,2]
    - (Row 2, Column 2): [2,4,2,2]
    - (Row 3, Column 2): [2,4,2,2]
