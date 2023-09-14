#include <stdio.h>

#define MAX_SIZE 100

void displayArray(int arr[], int size) {
    printf("Array elements: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int insertElement(int arr[], int size, int position, int element) {
    if (size >= MAX_SIZE || position < 0 || position > size) {
        return size; 
    }

    for (int i = size; i > position; i--) {
        arr[i] = arr[i - 1]; 
    }

    arr[position] = element;
    return size + 1; 
}

int deleteElement(int arr[], int size, int position) {
    if (size <= 0 || position < 0 || position >= size) {
        return size; 
    }

    for (int i = position; i < size - 1; i++) {
        arr[i] = arr[i + 1]; 
    }

    return size - 1; 
}

int main() {
    int arr[MAX_SIZE];
    int size = 0;


    size = insertElement(arr, size, 0, 10);
    size = insertElement(arr, size, 1, 20);
    size = insertElement(arr, size, 1, 15);

    printf("After inserting elements:\n");
    displayArray(arr, size);


    size = deleteElement(arr, size, 1);

    printf("After deleting element at position 1:\n");
    displayArray(arr, size);

    return 0;
}
