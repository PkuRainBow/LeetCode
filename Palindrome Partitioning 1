class Solution {
public:
	  //store the final results.
    vector<vector<string>> ans;
    
    bool IsPalindrome(string s, int start, int end){
        if(start==end)
            return true;
        int i=start, j=end;
        while(i<j){
            if(s[i]!=s[j])
                return false;
            i++;
            j--;
        }
        return true;
    }
    //递归
    void recursivePar(string s, int start, vector<string> par){
        if(start==s.length()){
            ans.push_back(par);//store all the palind... and we have pushed the par into the answer set...
            return;
        }
        //*********how to design the recursive procedure***********//
        for(int i=start; i<s.length(); i++){//the sring "ss" of different length [1,2,3...]
            if(IsPalindrome(s, start, i)){  //the "ss" is palindrome
                par.push_back(s.substr(start, i-start+1));//store the palind.. part and go on to find ... ----> par is the sub answer
                recursivePar(s, i+1, par);//go on to find the next palind...
                par.pop_back();
            }
        }
    }
    
    vector<vector<string>> partition(string s) {
        // Start typing your C/C++ solution below
        // DO NOT write int main() function
        vector<string> par;
        par.clear();
        ans.clear();
        recursivePar(s, 0, par);
        return ans;
    }
};


