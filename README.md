#include <stdio.h>

int sumOfDigits(int num) {
    // Base case: if the number is 0, return 0
    if (num == 0) {
        return 0;
    } else {
        // Recursive case: add the last digit to the sum of the remaining digits
        return (num % 10) + sumOfDigits(num / 10);
    }
}

int main() {
    int number;

    // Prompt user for input
    printf("Enter a five-digit number: ");
    scanf("%d", &number);

    // Check if the number is a five-digit number
    if (number < 10000 || number > 99999) {
        printf("Please enter a valid five-digit number.\n");
        return 1;
    }

    // Calculate the sum of digits
    int sum = sumOfDigits(number);
// Display the result
    printf("The sum of the digits is: %d\n", sum);

    return 0;
}

