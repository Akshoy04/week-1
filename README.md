1) Program to input elements of array and print all the elements


#include <stdio.h>

int main() {

    int n;
    printf("Enter the number of elements in the array: ");
    scanf("%d", &n);
    int arr[n];  
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++) {
        printf("Element %d: ", i + 1);
        scanf("%d", &arr[i]);
    }
    printf("\nThe elements in the array are:\n");
    for(int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    return 0;
}


2) count the numbers of positive and negative

#include <stdio.h>

int main() {

    int n, i, num, positive = 0, negative = 0;
    printf("Enter the number of elements: ");
    scanf("%d", &n);
    printf("Enter %d numbers:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &num);
        if(num > 0)
            positive++;
        else if(num < 0)
            negative++;
    }
    printf("Number of positive numbers: %d\n", positive);
    printf("Number of negative numbers: %d\n", negative);
    return 0;
}


3) convert decimal to binary

#include <stdio.h>

int main() {

    int num, binary[32], i = 0;
    printf("Enter a decimal number: ");
    scanf("%d", &num);
    if(num == 0) {
        printf("Binary: 0");
        return 0;
    } 
    while(num > 0) {
        binary[i] = num % 2;
        num = num / 2;
        i++;
    }
    printf("Binary: ");
    for(i = i - 1; i >= 0; i--) {
        printf("%d", binary[i]);
    }
    return 0;
}


4) generate n number of terms in FIBONACCI METHOD

#include <stdio.h>

int main() {

    int n, first = 0, second = 1, next, i;
    printf("Enter the number of terms: ");
    scanf("%d", &n);
    printf("Fibonacci series: ");
    for(i = 0; i < n; i++) {
        if(i == 0)
            next = 0;
        else if(i == 1)
            next = 1;
        else
            next = first + second;
        printf("%d ", next);
        first = second;
        second = next;
    }
    return 0;
}
