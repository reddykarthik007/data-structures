#include <stdio.h>
#include <stdlib.h>
struct Node {
    int data;
    struct Node* next;
};
struct Node* insertFront(struct Node* head, int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    newNode->next = head;
    return newNode;
}
struct Node* deleteNode(struct Node* head, int key) {
    if (head == NULL)
        return head;

    if (head->data == key) {
        struct Node* temp = head;
        head = head->next;
        free(temp);
        return head;
    }

    struct Node* curr = head;
    struct Node* prev = NULL;
    while (curr != NULL && curr->data != key) {
        prev = curr;
        curr = curr->next;
    }

    if (curr == NULL)
        return head;

    prev->next = curr->next;
    free(curr);
    return head;
}

void displayList(struct Node* head) {
    struct Node* current = head;
    while (current != NULL) {
        printf("%d -> ", current->data);
        current = current->next;
    }
    printf("NULL\n");
}

int main() {
    struct Node* head = NULL;

    head = insertFront(head, 10);
    head = insertFront(head, 20);
    head = insertFront(head, 30);

    printf("Linked list after insertions:\n");
    displayList(head);

    head = deleteNode(head, 20);

    printf("Linked list after deletion:\n");
    displayList(head);

    while (head != NULL) {
        struct Node* temp = head;
        head = head->next;
        free(temp);
    }

    return 0;
}
