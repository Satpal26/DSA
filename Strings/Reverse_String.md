# Reverse String

**Problem Link:** [LeetCode 344](https://leetcode.com/problems/reverse-string/)

first we will reverse the entire string .. for ex the string is "the pen" then after reversing it will look something like this "nep eht"

now we will take each reverse word and reverse it again to form the revrerse string like first we will take "nep" then reverse it to form "pen"

to do this we will first iterate the loop then what will do is that we will first take a temp string temp = "" this will be an empty string
then we will go till we find a space like for"nep eht" we will start from n and go till p coz after it theres a space ..
when we were iterating through each char we will check if [ s[i] != " " ] (condtn for space) then temp += s[i] and i++ ;
what happen in this that we will iterate each word till space and add it to temp so that after one iteration in temp there will be "nep" and we will reverese this
to form "pen" and add it to our ans ... 

the code will look something like this :-

class Solution {
public:
    string reverseWords(string s) {
        int n = s.length() ;
        string ans = "";

        reverse(s.begin() , s.end());

        for(int i = 0 ; i < n ; i++){
            string temp = "";

            while( i < n && s[i] != ' '){
                temp += s[i];
                i++;
            }

            reverse(temp.begin() , temp.end());

            if(temp.length() > 0 ){
                ans += " " + temp ;  // to add spaces between the string also 
            }
        }

        return ans.substr(1); //  here as in ans we have " " + temp so at the 0 index there will be space therefore we use this substr(1) to show that it should 
    }                             from the  second index 
};
