# odd-even
This problem rearranges a linked list by placing nodes at odd positions first, followed by nodes at even positions, while keeping their original order. It is solved in O(n) time and O(1) extra space.

APPROACH
The goal is to arrange the nodes based on their positions, not their values.

For example:

Original:  1 → 2 → 3 → 4 → 5

Odd positions:   1 → 3 → 5
Even positions:  2 → 4

Final:           1 → 3 → 5 → 2 → 4

We maintain two parts:

Odd list → nodes at positions 1, 3, 5...
Even list → nodes at positions 2, 4, 6...

Finally, we connect the end of the odd list to the beginning of the even list.

ALGORITHM
If the list has 0 or 1 node, return head.
Set odd = head.
Set even = head->next.
Store the first even node in evenHead.
Move the odd pointer to the next odd node.
Move the even pointer to the next even node.
Continue until there are no more nodes.
Connect the last odd node to evenHead.
Return head.
COMPLEXITY
Time Complexity

O(n)

We traverse the linked list once.

Space Complexity

O(1)
