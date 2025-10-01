**PROBLEM LINK** [LeetCode 242](https://leetcode.com/problems/valid-anagram/description/)

Anagram = An anagram is a word or phrase formed by rearranging the letters of a different word or phrase, using all the original letters exactly once.

first what comes in my mind is that i will sort both the strings s and t and check if s==t it will return true else false
and luckily the soln accepted also but its not optimal also ...

the code was something like this :-

    bool isAnagram(string s, string t) {
        if (s.length() != t.length()) return false;
        
        sort(s.begin() , s.end());
        sort(t.begin() , t.end());

        return s == t ;
    }

the optimal solution can be done by using Maps.. we will create an map mpp of <char,int>

where first we will run a loop in s and increment the frequency of that char in map ..
for ex if s = "anagram"..first loop will run from "a" it will increment the freq of a in the map
then there is "n" it will increment the freq of "n" in map and so on...

then we run a loop in t and decrement the freq of char in map..

if both s and t  are anagrams of each other at the end all the freq of char in the map will be zero..

so the code will look something like this :-

     bool isAnagram(string s, string t) {
        if (s.length() != t.length()) return false;
        
        unordered_map<char,int> mpp ;

        for(char c : s ) mpp[c]++;

        for(char c : t) mpp[c]-- ;

        for(auto it : mpp){
            if(it.second != 0 ) return false;
        }

        return true;
    }
