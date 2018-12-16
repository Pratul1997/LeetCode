# Solution
```
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution(object):
    def isPalindrome(self, head):
        arr = []
        if head is None:
            return True
        elif head.next is None:
            return True
        else:
            while head is not None:
                arr.append(head.val)
                head = head.next
            if arr == arr[::-1]:
                return True
            else:
                return False
```
