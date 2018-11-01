# Solution
```
class Solution:
    def plusOne(self, digits):
        digits[len(digits)-1]=digits[len(digits)-1]+1
        
        if(len(digits)==1 and digits[0]==10):
            digits=[1,0]
            
        if(len(digits)>1):
            a=1
            while(digits[len(digits)-a]>=10):
                if(a==len(digits)):
                    if(digits[0]==9):
                        break          
                    digits[len(digits)-a]=0
                    digits=[1]+digits
                    break
                digits[len(digits)-a]=0
                a=a+1
                digits[len(digits)-a] = digits[len(digits)-a]+1
        return digits
```
