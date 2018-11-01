# Solution
```
class Solution:
    def reverse(self, x):
        while(x>0):
            if(x%10==0):
                x=int(x/10)
            else:
                break
        sum=0
        count=0
        if(x<0):
            count=1
            x=x*(-1)
            
        while(x>0):
            sum=sum*10+(x%10)
            x=int(x/10)
        
        if(count==1):
            sum=sum*(-1)
        if(sum>=2147483647 or sum<=-2147483648):
            sum=0
        return sum
```
