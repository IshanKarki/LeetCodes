# Roman to Integer 
Roman numerals are represented by seven different symbols: I, V, X, L, C, D and M.

    Symbol       Value
    I             1
    V             5
    X             10
    L             50
    C             100
    D             500
    M             1000
    
_For example_, **2** is written as **II** in Roman numeral, just two ones added together. **12** is written as **XII**, which is simply X + II. The number **27** is written as **XXVII**, which is XX + V + II.

Roman numerals are usually written _largest_ to _smallest_ from_**left to right**_. 
However, the numeral for _four is not IIII_. Instead, the number four is written as **IV**. 
Because the one is before the five we subtract it making four. 

The same principle applies to the number _nine_, which is written as _IX_. There are **six instances** where subtraction is used:

_I can be placed before V (5) and X (10) to make 4 and 9._

_X can be placed before L (50) and C (100) to make 40 and 90._ 

_C can be placed before D (500) and M (1000) to make 400 and 900._

# Given a roman numeral, convert it to an integer.

    Example 1:
    Input: s = "III"
    Output: 3
    Explanation: III = 3.

    Example 2:
    Input: s = "LVIII"
    Output: 58
    Explanation: L = 50, V= 5, III = 3.

    Example 3:
    Input: s = "MCMXCIV"
    Output: 1994
    Explanation: M = 1000, CM = 900, XC = 90 and IV = 4.
