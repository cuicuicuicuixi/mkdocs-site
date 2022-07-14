# String

## Table of Contents : Brush leetcode

* [Valid Palindrome](#valid-palindrome)
* [Prefix and Suffix Search](#prefix-an-suffix-search)

## Content

#### Valid Palindrome

##### Problem Description

A phrase is a Palindrome if, after converting all uppercase letters into lowercase letters and removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric characters include letters and numbers.

Given a string 's', return 'true' if it is a Palindrome, or 'false' otherwise.

##### Answer

```cpp
    bool isPalindrome(string s) {
        for(int i = 0; i < s.length(); i++)
        {
            if((s[i]-'A' >= 0 && s[i] - 'A' < 26)) s[i] = 'a' + s[i] - 'A'; 
        }
        int l = 0, r = s.length()-1;
        while(l < r)
        {
            if(!(s[l]-'a' >= 0 && s[l] - 'a' < 26) && !(s[l] - '0' >= 0 && s[l] - '0' <= 9)) {
                l++;
                continue;
            }
            if(!(s[r]-'a' >= 0 && s[r] - 'a' < 26) && !(s[r] - '0' >= 0 && s[r] - '0' <= 9)) {
                r--;
                continue;
            }
            if(l < r && s[l] != s[r]) return false;
            else if(l < r && s[l] == s[r]) {
                l++;
                r--;
            }
        }
        return true;
    }

```

#### Prefix and Suffix Search

##### Problem Description

Design a special dictionary that searches the words in it by a prefix and a suffix.

ImPlement the 'WordFilter' Class:

* 'WordFilter(string[] words)' initializes the object with the 'words' in the dictionary.
* 'f(string pref, string suff) return the index of the word in the dictionary, which has the prefix 'pref' and the suffix 'suff'. If there is more than one valid index, return the largest of then. If there is no such word in the dictionary, return '-1'.

##### Answer


