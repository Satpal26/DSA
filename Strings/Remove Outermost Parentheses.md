**PROBLEM LINK** [Leetcode 1021](https://leetcode.com/problems/remove-outermost-parentheses/description/)

valid Parentheses is something which have a start [ ( ] and an end [ ) ] so in this question we have to remove the outermost Parentheses 

for example : if s = "(()())(())" then after outermost parentheses it will look somehting like this "()()()"

so to solve this we will first initialize count = 0  and string ans = "" 

then we will run a loop where first we will check if " ) " comes then we will do count--;

and also check if count != 0  then only we will add the char in the ans;

then we will check if " ( " we wil do count++ ..

the code will look like this :-

    string removeOuterParentheses(string s) {
        int count = 0 ;
        string ans  = "" ; 

        for(int i = 0 ; i < s.length() ; i++){

            if(s[i] == ')') count--;

            if(count != 0 ) ans+= s[i];

            if(s[i] == '(') count++ ;
        }

        return ans;
    }
