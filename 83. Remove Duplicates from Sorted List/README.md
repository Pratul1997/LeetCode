# Solution

```
class Solution:
    def deleteDuplicates(self, head):
        if head is None:
            return head
        elif head.next is None:
            return head
        elif head.next.next is None:
            if head.val == head.next.val:
                return head.next
            else:
                return head
        temp = head
        while head.next is not None:
            if head.next.val == head.val:
                head.next = head.next.next
                continue
            head = head.next
        return temp
```
