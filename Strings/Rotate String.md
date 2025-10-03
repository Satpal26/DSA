**PROBLEM LINK** [LeetCode 796](https://leetcode.com/problems/rotate-string/)

NOTE :- **IF YOU CONCATENATE (ADD STRING) TO ITSELF, IT WILL CONTAIN ALL ROTATIONS AS A SUBSTRING IN IT**

so basically its and easy ques the only thing we have to keep in  mind is that the **NOTE** things...

the code will look something like this:-
    
    bool rotateString(string s, string goal) {
        
        if(s.length()  != goal.length()) return false;

        string temp = s + s ; 

        if(temp.find(goal) != string::npos){

            return true;
        }else{
            return false;
        }
    }

string::npos is a constant in the C++ standard library.

Think of it as:
👉 npos = No Position Found

it is used to check if the goal thing is in temp or not...
