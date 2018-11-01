# Solution
```
class Solution:
    def myPow(self, x, n):
        flag=True
        k=0
        if(n<0):
            k=-n
            flag=False
        elif(n>0):
            k=n
        else:
            return 1

        val=Solution.pw(x,k)
        if(flag==False):
            val=1/val
        
        return val
           
    def pw(x,n):
        if(n==1):
            return x
        temp=Solution.pw(x,n//2)
        if(n%2==0):
            return temp*temp
        else:
            return temp*temp*x  
```
