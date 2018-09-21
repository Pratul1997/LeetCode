# Solution
```
class Solution:
    def reverseVowels(self, s):
        vowel=['a','e','i','o','u','A','E','I','O','U']
        st=''
        ans=''
        for x in range(len(s)):
            if(s[x] in vowel):
                st=st+s[x]
        st=st[::-1]

        count=0
        for y in range(len(s)):
            if(s[y] in vowel):
                ans=ans+st[count]
                count=count+1
            else:
                ans=ans+s[y]
        return ans
```
