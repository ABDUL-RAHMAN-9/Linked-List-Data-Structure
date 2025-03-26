# Linked-List-Data-Structure
## Given a Singly Linked List, the task is to print all the elements in the list.
# Examples : 
```  
    Input: 1->2->3->4->5->null
    Output: 1 2 3 4 5
    Explanation: Every element of each node from head node to last node is printed.

    Input: 10->20->30->40->50->null
    Output: 10 20 30 40 50
    Explanation: Every element of each node from head node to last node is printed.
```

## Step-by-Step Algorithm
- We will initialize a temporary pointer to the head node of the singly linked list.
- After that, we will check if that pointer is null or not null, if it is null, then return.
- While the pointer is not null, we will access and print the data of the current node, then we move the pointer to next node.
        
# Code :

```
#include <iostream>
using namespace std;

// A linked list node
class Node {
public:
    int data;
    Node* next;

    // Constructor to initialize a new node with data
    Node(int new_data) {
        this->data = new_data;
        this->next = nullptr;
    }
};

// Function to print the singly linked list
void printList(Node* head) {

    // A loop that runs till head is nullptr
    while (head != nullptr) {

        // Printing data of current node
        cout << head->data << " ";

        // Moving to the next node
        head = head->next;
    }
}

int main() {
  
    // Create a linked list: 10 -> 20 -> 30 -> 40
    Node* head = new Node(10);
    head->next = new Node(20);
    head->next->next = new Node(30);
    head->next->next->next = new Node(40);

    printList(head);

    return 0;
}


```

# Output 
```
10 20 30 40 
```
# Complexity
Time Complexity : O(n)
<br>
Auxiliary Space : O(1)
