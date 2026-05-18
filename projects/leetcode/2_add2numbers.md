---
date: 11/08/25
---
``` C
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * }
 */
#include <stdio.h>
#include <stdio.h>

struct ListNode *createNode(int val){
    struct ListNode *node = malloc(sizeof(struct ListNode));
    node -> val = val;
    node -> next = NULL;
    return node;
}

struct ListNode* addTwoNumbers(struct ListNode* l1, struct ListNode* l2) {
    // take two linked list nodes as input, return linked list node as output
    struct ListNode *dummyhead = createNode(0);
    struct ListNode *temp = dummyhead;
    int carry = 0;

    while (l1 != NULL || l2 != NULL || carry != 0)
    {
        int sum = carry;
        
        if (l1 != NULL) // case where l1 is longer than l2
        {
            sum += l1->val;
            l1 = l1->next;
        }
        if (l2 != NULL) // case where l2 is longer than l1
        {
            sum += l2->val;
            l2 = l2->next;
        }

        carry = sum/10;
        temp->next = createNode(sum%10);
        temp = temp->next;
    }

    return dummyhead->next;
}
```