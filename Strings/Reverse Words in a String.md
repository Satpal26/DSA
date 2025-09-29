Reverse Words in a String

**Problem Link:** [LeetCode 151](https://leetcode.com/problems/reverse-words-in-a-string/description/)

in this ques we have to reverse each word in the string for ex if **the sky is blue** is given we have to make it **blue is sky the** ..

to make this happen first we will reverse the whole string by using **reverse(s.begin() , s.end())**  ... here after reversing it will look something like this *eulb si yks eht*

now we will again reverse but now word by word .. to make this we will iterate a loop where we will start from 0 till **s[i] != ' '** ( this means we will iterate from 0 till there is a space between two words ) 
and we will store this in a temp string called temp.. after this we will again that temp string by using the reverse func of STL and will add this to a ans string..

The code for this ques will look something like this :- 

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

            if(temp.length() > 0 ){          [ here to check if the temp is empty or not ] 
                ans += " " + temp ;
            }
        }

        return ans.substr(1);
    }
};

here we used substr at the end because as we can see we use ans += " " + temp to create space between the words so the first will start with space which we dont want thats why we use ans.substr(1) 
this means it will start from position 1 ....

