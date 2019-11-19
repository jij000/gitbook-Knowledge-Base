# Linked List Cycle

## [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/description/)

| Category | Difficulty | Likes | Dislikes |
| :--- | :--- | :--- | :--- |
| algorithms | Easy \(38.69%\) | 1939 | 279 |

**TagsCompanies**

Given a linked list, determine if it has a cycle in it.

To represent a cycle in the given linked list, we use an integer `pos` which represents the position \(0-indexed\) in the linked list where tail connects to. If `pos` is `-1`, then there is no cycle in the linked list.

**Example 1:**

```text
Input: head = [3,2,0,-4], pos = 1
Output: true
Explanation: There is a cycle in the linked list, where tail connects to the second node.
```

![](https://assets.leetcode.com/uploads/2018/12/07/circularlinkedlist.png)

**Example 2:**

```text
Input: head = [1,2], pos = 0
Output: true
Explanation: There is a cycle in the linked list, where tail connects to the first node.
```

![](https://assets.leetcode.com/uploads/2018/12/07/circularlinkedlist_test2.png)

**Example 3:**

```text
Input: head = [1], pos = -1
Output: false
Explanation: There is no cycle in the linked list.
```

![](https://assets.leetcode.com/uploads/2018/12/07/circularlinkedlist_test3.png)

**Follow up:**

Can you solve it using _O\(1\)_ \(i.e. constant\) memory?

[Discussion](https://leetcode.com/problems/linked-list-cycle/discuss/?currentPage=1&orderBy=most_votes&query=) \| [Solution](https://leetcode.com/problems/linked-list-cycle/solution/)

## Solution

```java
/**
 * Definition for singly-linked list. class ListNode { int val; ListNode next;
 * ListNode(int x) { val = x; next = null; } }
 */
public class Solution {
    public boolean hasCycle(ListNode head) {
        ListNode fastPoint = head;
        ListNode slowPoint = head;
        while (slowPoint != null && slowPoint.next != null) {
            if (fastPoint == null || fastPoint.next == null) {
                return false;
            } else {
                fastPoint = fastPoint.next.next;
            }
            slowPoint = slowPoint.next;
            if (fastPoint == slowPoint) {
                return true;
            }
        }
        return false;
    }
}
```

## Note

1. 原理是快慢指针, 如果有环则终究会相遇
2. 注意快指针的null的判断

