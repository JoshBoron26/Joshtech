#include <stdio.h>
# include <stdlib.h>

int main() {
    int choice;
    float balance = 10000, amount;

    printf("=== SIMPLE ATM ===\n");
    printf("1. Check Balance\n");
    printf("2. Deposit\n");
    printf("3. Withdraw\n");
    printf("Choose option: ");
    scanf("%d", &choice);

    if (choice == 1) {
        printf("Balance: %.2f\n", balance);
    } 
    else if (choice == 2) {
        printf("Enter amount to deposit: ");
        scanf("%f", &amount);
        balance += amount;
        printf("New Balance: %.2f\n", balance);
    } 
    else if (choice == 3) {
        printf("Enter amount to withdraw: ");
        scanf("%f", &amount);
        if (amount <= balance) {
            balance -= amount;
            printf("New Balance: %.2f\n", balance);
        } else {
            printf("Insufficient balance!\n");
        }
    } 
    else {
        printf("Invalid choice!\n");
    }

    return 0;
}
