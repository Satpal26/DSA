**PROBLEM LINK** [LeetCode 1910](https://leetcode.com/problems/remove-all-occurrences-of-a-substring/description/)

here a string is given s and theres a part of string given and we have to erase that part from left and return that ..
here we have use find func from which we will find the position of that part like the first position 
then after this we will use erase funcn where first we add the initial position from where we have to erase the string 
and we will add the length of string upto which the string will be erase like if erase(2,3) is given this means
we will erase a string of length 3 which starts from position 2 .. 


the code for this will look something like this :-

      string removeOccurrences(string s, string part) {
        while (s.length() > 0 && s.find(part) < s.length()){
            s.erase(s.find(part) , part.length());
        }

        return s ; 
    }
