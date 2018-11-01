# Solution
```
class Solution:
    def matrixReshape(self, nums, r, c):
        no_row=len(nums)
        no_col=len(nums[0])
        ls=[[]]
        if(no_row*no_col==r*c):
            new_arr=[]
            for l in range(len(nums)):
                new_arr=new_arr+nums[l]
            count=0
            di=0
            for x in range(len(new_arr)):
                if(count<c):
                    ls[di].append(new_arr[x])
                    count=count+1
                else:  
                    ls.append([])
                    di=di+1
                    ls[di].append(new_arr[x])
                    count=1
            return ls
        else:
            return nums
```
