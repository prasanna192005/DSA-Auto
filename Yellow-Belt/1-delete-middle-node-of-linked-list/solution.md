# Approach

The solution uses a two-pointer approach (slow and fast).  The fast pointer moves twice as fast as the slow pointer. When the fast pointer reaches the end, the slow pointer will be at the middle.  We then need to delete the node the slow pointer points to.  This can be done by copying the value of the next node into the current node and deleting the next node.

**Note:**  Error handling for edge cases (single node list) is crucial.  The specific implementation may differ slightly between languages depending on how linked lists are handled.

## C++
cpp
#include <iostream>

struct Node {
    int data;
    Node *next;
    Node(int x) : data(x), next(nullptr) {}
};

void deleteMiddle(Node* &head) {
    if (head == nullptr || head->next == nullptr) return; // Handle edge cases

    Node *slow = head;
    Node *fast = head;
    Node *prev = nullptr;

    while (fast != nullptr && fast->next != nullptr) {
        prev = slow;
        slow = slow->next;
        fast = fast->next->next;
    }

    if (prev != nullptr) {
        prev->next = slow->next;  // Delete node
        delete slow;
    } else {
        head = head->next; // Delete the only node
        delete slow;
    }
}

int main() {
    Node* head = new Node(1);
    head->next = new Node(2);
    head->next->next = new Node(3);
    head->next->next->next = new Node(4);
    head->next->next->next->next = new Node(5);

    deleteMiddle(head);

    Node* current = head;
    while(current != nullptr){
        std::cout << current->data << " ";
        current = current->next;
    }
    std::cout << std::endl;
    return 0;
}


## Java
java
class Node {
    int data;
    Node next;
    Node(int x) { data = x; next = null; }
}

class Solution {
    public void deleteMiddle(Node head) {
        if (head == null || head.next == null) return;

        Node slow = head;
        Node fast = head;
        Node prev = null;

        while (fast != null && fast.next != null) {
            prev = slow;
            slow = slow.next;
            fast = fast.next.next;
        }

        if (prev != null) {
            prev.next = slow.next; // Delete node
        } else {
            head = head.next; // Delete the only node
        }
    }
}


## Python
python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

def delete_middle(head):
    if not head or not head.next:
        return

    slow = head
    fast = head
    prev = None

    while fast and fast.next:
        prev = slow
        slow = slow.next
        fast = fast.next.next

    if prev:
        prev.next = slow.next
    else:
        head = head.next

#Example Usage
head = Node(1)
head.next = Node(2)
head.next.next = Node(3)
head.next.next.next = Node(4)
head.next.next.next.next = Node(5)

delete_middle(head)

current = head
while current:
    print(current.data, end=" ")
    current = current.next
print()


## JavaScript
javascript
class Node {
    constructor(data) {
        this.data = data;
        this.next = null;
    }
}

function deleteMiddle(head) {
    if (!head || !head.next) return;

    let slow = head;
    let fast = head;
    let prev = null;

    while (fast && fast.next) {
        prev = slow;
        slow = slow.next;
        fast = fast.next.next;
    }

    if (prev) {
        prev.next = slow.next;
    } else {
        head = head.next;
    }
}

// Example Usage
let head = new Node(1);
head.next = new Node(2);
head.next.next = new Node(3);
head.next.next.next = new Node(4);
head.next.next.next.next = new Node(5);

deleteMiddle(head);

let current = head;
while (current) {
    console.log(current.data);
    current = current.next;
}
