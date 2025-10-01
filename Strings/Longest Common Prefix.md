**PROBLEM LINK** [LeetCode 14](https://leetcode.com/problems/longest-common-prefix/description/)

brute force for this is we will start checking by taking first char of the first string and check on other string one by one but this will take alot of time

so we will sot the string then we will check only first and last char like how many of them are common... 

the code will look like this:- 

     string longestCommonPrefix(vector<string>& strs) {

        if(strs.empty()) return "" ;


        sort(strs.begin() , strs.end());

        string first = strs[0];
        string last = strs.back();
        
        int i = 0 ;
        while( i  < first.size() && i < last.size() && first[i] == last[i] ){
            i++;
        }

        return first.substr(0,i);
    }
