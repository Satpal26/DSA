**PROBLEM LINK** [Leetcode 1903](https://leetcode.com/problems/largest-odd-number-in-string/description/)

In this ques we have to find Largest Odd Number in String basically its an easy prooblem where we will start the iteration from the rightmost end 
and check if the the digit is odd or even if its odd we will return the string from 0 position to that index simple..

here's the code :-

        string largestOddNumber(string num) {
        int end = num.length() - 1 ;
        string ans = "";

        for(int i = num.length()-1 ; i >= 0 ; i-- ){
            if((num[i] - '0')% 2 != 0 ){
                ans = num.substr(0, i+1) ; 
                break;
            }
        }

        return ans ; 
    }

(num[i] - '0') here this means we are forming that number only because in strings every char have some ascii values 
for example:

'0' → 48
'1' → 49
'2' → 50

for ex if char '5' comes its ascii is 53 therefore '5' - '0' = 53 - 48 = 5 ...
