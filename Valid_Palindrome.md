**Problem Link:** [LeetCode 344](https://leetcode.com/problems/valid-palindrome/submissions/1781207664/)

we will use two pointer approach appraoch here [ start and end ] .

first of all we will check if the charc is valid or  not like valid character are only ( [a to z] & [A to Z ] or [0-9] ) other than this all are not valid so we have to skip that for that we will create a function which will check if its valid or not ..

then we first lowercase every char ( by using tolower() func of STL )  to lower case to check if it is a valid palindrome or not..
