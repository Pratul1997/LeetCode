# Solution
```
class Solution:
    def findWords(self, words):
        key=[['Q','W','E','R','T','Y','U','I','O','P'],
        ['A','S','D','F','G','H','J','K','L'],
        ['Z','X','C','V','B','N','M']]
        out = []
        for x in range(len(words)):
            flag = True
            if words[x][0].upper() in key[0]:
                val = 0
            elif words[x][0].upper() in key[1]:
                val = 1
            elif words[x][0].upper() in key[2]:
                val = 2
            for y in range(len(words[x])):
                if not words[x][y].upper() in key[val]:
                    flag = False
                    break
            if flag == True:
                out.append(words[x])
        return out
```
