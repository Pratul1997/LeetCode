# Solution
```
class Solution:
    def longestCommonPrefix(self, strs):
        if(len(strs)>1):
            rt=""
            minlen=1000000
            index=-1
            for st in range(len(strs)):
                if(len(strs[st])<minlen):
                    minlen=len(strs[st])
                    index=st
            bindex=-1
            for x in range(len(strs[index])):
                ch=strs[index][x]
                for y in strs:
                    if(y[x]!=ch and bindex==-1):
                        bindex=x
            if(bindex==-1):
                return(strs[index])
            return (strs[index][:bindex])
        elif(len(strs)==1):
            return strs[0]
        else:
            return ""
```
