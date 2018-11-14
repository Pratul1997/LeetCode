# Solution
```
class Solution:
    def twoSum(self, numbers, target):
        new_dic=dict()
        for x in range(len(numbers)):
            sec=new_dic.get((target-numbers[x]),-1)
            if(sec>=0):
                return [sec+1,x+1]
            else:
                new_dic[numbers[x]]=x
```
