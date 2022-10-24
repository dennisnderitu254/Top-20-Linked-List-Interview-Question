Find the middle of a given linked list
======================================

Given a singly linked list, find the middle of the linked list. For example, if the given linked list is 1->2->3->4->5 then the output should be 3.

If there are even nodes, then there would be two middle nodes, we need to print the second middle element. For example, if the given linked list is 1->2->3->4->5->6 then the output should be 4.

`Method 1:` Traverse the whole linked list and count the no. of nodes. Now traverse the list again till count/2 and return the node at count/2

Output

`5->NULL`
`The middle element is [5]`
`4->5->NULL`
`The middle element is [5]`
`3->4->5->NULL`
`The middle element is [4]`
`2->3->4->5->NULL`
`The middle element is [4]`
`1->2->3->4->5->NULL`
`The middle element is [3]`


Time Complexity: O(n) where n is no of nodes in linked list
Auxiliary Space: O(1)

`Method 2:` Traverse linked list using two-pointers. Move one pointer by one and the other pointers by two. When the fast pointer reaches the end, the slow pointer will reach the middle of the linked list.

![method2middle](/Top-20-Linked-List-Interview-Question/middlevalueofalinkedlist/method2middle.png)

Output

`5->NULL`
`The middle element is [5]`
`4->5->NULL`
`The middle element is [5]`
`3->4->5->NULL`
`The middle element is [4]`
`2->3->4->5->NULL`
`The middle element is [4]`
`1->2->3->4->5->NULL`
`The middle element is [3]`

Time Complexity: O(N), As we are traversing the list only once.
Auxiliary Space: O(1), As constant extra space is used.

`Method 3:` Initialize the mid element as head and initialize a counter as 0. Traverse the list from the head, while traversing increment the counter and change mid to mid->next whenever the counter is odd. So the mid will move only half of the total length of the list.

Output

`5->NULL`
`The middle element is [5]`

`4->5->NULL`
`The middle element is [5]`

`3->4->5->NULL`
`The middle element is [4]`

`2->3->4->5->NULL`
`The middle element is [4]`

`1->2->3->4->5->NULL`
`The middle element is [3]`

Time Complexity: O(N), As we are traversing the list once.
Auxiliary Space: O(1), As constant extra space is used.
