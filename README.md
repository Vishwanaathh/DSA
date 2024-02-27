# DSA
// Online C++ compiler to run C++ program online
#include <iostream>
using namespace std;
class node{
public:
    int data;
    node* next;
    
    node(int data){
        this->data=data;
        next=NULL;
    }
    
};
void insertAtHead(node* &head, int data){
    if(head == NULL){
        head = new node(data);
    } else {
        node *n = new node(data);
        n->next = head;
        head = n;
    }
}

void printll(node * head){
    while(head!=NULL){
        cout<<head->data<<"-->";
        head=head->next;
    }
}

int main() {
    // Write C++ code here
    node* head=NULL;
    insertAtHead(head,4);
    insertAtHead(head,3);
    insertAtHead(head,2);
    printll(head);
    

    return 0;
}
