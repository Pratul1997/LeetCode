# Solution 
```
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution(object):
    def addTwoNumbers(self, l1, l2):
        num1 = 0
        while l1 is not None:
            num1 = num1 * 10 + l1.val
            l1 = l1.next
        num2 = 0
        while l2 is not None:
            num2 = num2 * 10 + l2.val
            l2 = l2.next

        num3 = str(num1 + num2)
        out = re = ListNode(0)
        for x in range(len(num3)):
            vt = int(num3[x])
            re.val = vt
            if x == len(num3) - 1:
                continue
            temp = ListNode(0)
            re.next = temp
            re = re.next
        return out
```
