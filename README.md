//# ultra-basic-calculator
//Calculator using C program
//It is my first project after learning a basic C program.
//I will update it after learning new things.
// Here is the code:

#include <stdio.h>

int main() {
    char confirm;
    int choice;
    int a, b;
    float c, d;

    printf("========== Basic Calculator ==========\n");
    printf("Type 'y' or 'Y' if you want to calculate anything: ");
    scanf(" %c", &confirm);  // Added space before %c to consume any leftover newline

    if (confirm == 'y' || confirm == 'Y') {
        printf("\nChoose the operator by number:\n");
        printf("1. Addition (+)\n");
        printf("2. Subtraction (-)\n");
        printf("3. Multiplication (*)\n");
        printf("4. Division (/)\n");
        printf("5. Modulus (%%)\n");  // %% to escape percent sign
        printf("Enter your choice (1-5): ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("\nEnter two integers to add:\n");
                printf("First number: ");
                scanf("%d", &a);
                printf("Second number: ");
                scanf("%d", &b);
                printf("Result: %d + %d = %d\n", a, b, a + b);
                break;

            case 2:
                printf("\nEnter two integers to subtract:\n");
                printf("First number: ");
                scanf("%d", &a);
                printf("Second number: ");
                scanf("%d", &b);
                printf("Result: %d - %d = %d\n", a, b, a - b);
                break;

            case 3:
                printf("\nEnter two integers to multiply:\n");
                printf("First number: ");
                scanf("%d", &a);
                printf("Second number: ");
                scanf("%d", &b);
                printf("Result: %d * %d = %d\n", a, b, a * b);
                break;

            case 4:
                printf("\nEnter two numbers to divide:\n");
                printf("First number: ");
                scanf("%f", &c);
                printf("Second number: ");
                scanf("%f", &d);
                if (d != 0) {
                    printf("Result: %.2f / %.2f = %.2f\n", c, d, c / d);
                } else {
                    printf("Error: Division by zero is not allowed.\n");
                }
                break;

            case 5:
                printf("\nEnter two integers for modulus:\n");
                printf("First number: ");
                scanf("%d", &a);
                printf("Second number: ");
                scanf("%d", &b);
                if (b != 0) {
                    printf("Result: %d %% %d = %d\n", a, b, a % b);
                } else {
                    printf("Error: Modulus by zero is not allowed.\n");
                }
                break;

            default:
                printf("Invalid choice! Please select between 1 and 5.\n");
        }
    } else {
        printf("You did not enter 'y'. Exiting the program.\n");
    }

    return 0;
}
