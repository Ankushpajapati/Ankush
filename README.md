#include <stdio.h>

// Function to calculate the nth Fibonacci number
unsigned long long fibonacci(int n) {
    if (n <= 0)
        return 0;
    else if (n == 1)
        return 1;
    else
        return fibonacci(n - 1) + fibonacci(n - 2);
}

int main() {
    int num;
    printf("Enter the number of Fibonacci terms to generate: ");
    scanf("%d", &num);

    if (num < 1) {
        printf("Please enter a positive integer greater than zero.\n");
        return 1;
    }

    printf("Fibonacci Sequence:\n");
    for (int i = 0; i < num; i++) {
        printf("%llu ", fibonacci(i));
    }

    printf("\n");
    return 0;
}
