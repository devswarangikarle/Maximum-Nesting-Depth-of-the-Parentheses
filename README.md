# Maximum-Nesting-Depth-of-the-Parentheses

Given a valid parentheses string s, return the nesting depth of s. The nesting depth is the maximum number of nested parentheses.
Constraints:
1 <= s.length <= 100
s consists of digits 0-9 and characters '+', '-', '*', '/', '(', and ')'.
It is guaranteed that parentheses expression s is a VPS.

class Solution:
    def maxDepth(self, s: str) -> int:
        max_depth = 0 
        curr_depth = 0 

        for char in s :
            if char == "(" :
                curr_depth += 1
                max_depth = max(curr_depth , max_depth) 
            elif char == ")" :
                curr_depth -= 1

        return max_depth
        
