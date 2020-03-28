# Solution

## Python
```
class Solution:
    def twoSum(self, nums, target):
        new_dic = dict()
        for x in range(len(nums)):
            sec = new_dic.get(target - nums[x], -1)
            if sec >= 0:
                return [sec, x]
            else:
                new_dic[nums[x]] = x
 ```

## Golang
```
func twoSum(nums []int, target int) []int {
	di := map[int]int{}

	for i := 0; i <= len(nums); i++ {
		if idx, ok := di[target-nums[i]]; ok {
			return []int{idx, i}
		} else {
			di[nums[i]] = i
		}
	}
	return []int{}
}
```
