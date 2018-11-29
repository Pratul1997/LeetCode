# Solution
```
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def addTwoNumbers(self, l1, l2):
        num1 = 0
        c1 = c2 = 0
        num2 = 0
        while l1 is not None:
            num1 = num1 + l1.val * 10 ** c1
            c1 += 1
            l1 = l1.next
        while l2 is not None:
            num2 = num2 + l2.val * 10 ** c2
            c2 += 1
            l2 = l2.next

        num3 = num1 + num2

        l3 = ListNode(num3 % 10)
        num3 = num3 // 10

        while num3 > 0:
            value = num3 % 10
            temp = ListNode(value)
            insert = l3
            while insert.next is not None:
                insert = insert.next
            insert.next = temp
            num3 = num3 // 10
        return l3
```
