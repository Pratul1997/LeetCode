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

## Java
```
class Solution {
    public int[] twoSum(int[] nums, int target) {

        int n = nums.length;
        int[] arr = new int[2];
        HashMap < Integer, Integer > hm = new HashMap < Integer, Integer > ();

        for (int i = 0; i < n; i++) {
            hm.put(nums[i], i);
        }

        for (int i = 0; i < n; i++) {
            if (hm.containsKey(target - nums[i]) && i != hm.get(target - nums[i])) {
                arr[0] = i;
                arr[1] = hm.get(target - nums[i]);
                break;
            }

        }
        
        return arr;
    }
}
```
