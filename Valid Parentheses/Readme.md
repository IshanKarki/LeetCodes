# Valid Parentheses

Given a string s containing just the characters **'(', ')', '{', '}', '[' and ']'**, determine if the input string is valid.

An input string is valid if:
1. Open brackets must be closed by the same type of brackets.
2. Open brackets must be closed in the correct order.
3. Every close bracket has a corresponding open bracket of the same type.
 

        Example 1:
        Input: s = "()"
        Output: true

        Example 2:
        Input: s = "()[]{}"
        Output: true

        Example 3:
        Input: s = "(]"
        Output: false

The above problem can be approached from implementing a stack.
so we create an empty list stack,

	stack = []
 Then, to let the computer know which is the correct closing bracket of the respective opening bracket, we create a dictionary to map the opening brackets with their corresponding closing brackets as key-value pair,

		pairs = {
				'(':')',
				'{':'}',
				'[':']'
		}
then we loop through the input string to figure out the individual elements in the entered string
so we loop through the s,

		for bracket in s:
then inside the loop, we check if the individual string in s is in keys of the pairs dictionary, and if it is we append that string to stack list,

	if bracket in pairs:
	  stack.append(bracket)
else we know that the entered string is a closing bracket and for that we pop every last element from the stack, to check if the closing bracket in **s** is the same key value of the popped string in pairs dictionary.

_Example_, if **s = { [ ] }** then stack will be 

    stack = ['{','[']
and at third iteration bracket = ']' so we pop the last string from stack i.e stack.pop() = '['
Thus, 
we check if 

    pairs[stack.pop()] == bracket 
    pairs['['] == bracket
    pairs['['] == ']'
here,

    ']' == ']'
Thus, since this is equal so we just pop so in the stack we have

    stack = ['{']
Now, in the s, bracket = '}'
we do the same thing as above and pop the last element, thus if the string s is valid, it must be empty.

lets check for an invalid input

_Example_, say **s = { [ } ]** then stack will be 

    stack = ['{','[']
then bracket = '}', the last pop from stack is stack.pop() = '[',

    pairs['['] == '}'
    ']' == '}' # This statement is False
Thus, it returns False.

Say it started with an element not in pairs, i.e its a closing bracket then,

_Example_, say **s = ] } { ( ) ]**

then stack = [ ]
thus, we return False as

    len(stack) == 0 # here, this is True so if this is True we return False

    
