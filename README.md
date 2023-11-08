#include <stdio.h>
#include <math.h>

int main() {
    double num1, num2, result;
    char operator;

    printf("Enter the first number: ");
    scanf("%lf", &num1);

    printf("Enter the operator (+, -, *, /, ^): ");
    scanf(" %c", &operator);

    printf("Enter the second number: ");
    scanf("%lf", &num2);

    switch(operator) {
        case '+':
            result = num1 + num2;
            printf("The sum is: %.2lf\n", result);
            break;
        case '-':
            result = num1 - num2;
            printf("The difference is: %.2lf\n", result);
            break;
        case '*':
            result = num1 * num2;
            printf("The product is: %.2lf\n", result);
            break;
        case '/':
            if(num2 != 0) {
                result = num1 / num2;
                printf("The quotient is: %.2lf\n", result);
            } else {
                printf("Error: Division by zero is not allowed.\n");
            }
            break;
        case '^':
            result = pow(num1, num2);
            printf("The result of %.2lf raised to the power of %.2lf is: %.
