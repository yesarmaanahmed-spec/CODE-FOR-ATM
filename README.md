# CODE-FOR-ATM
#include <stdio.h>

int main()
{
    int pin = 1234, p, choice;
    float balance = 5000, amount;

    printf("Enter PIN: ");
    scanf("%d", &p);

    if(p == pin)
    {
        printf("\n1. Check Balance");
        printf("\n2. Deposit");
        printf("\n3. Withdraw");
        printf("\nEnter choice: ");
        scanf("%d", &choice);

        switch(choice)
        {
            case 1:
                printf("Balance = %.2f", balance);
                break;

            case 2:
                printf("Enter amount: ");
                scanf("%f", &amount);
                balance += amount;
                printf("Balance = %.2f", balance);
                break;

            case 3:
                printf("Enter amount: ");
                scanf("%f", &amount);

                if(amount <= balance)
                {
                    balance -= amount;
                    printf("Balance = %.2f", balance);
                }
                else
                    printf("Insufficient Balance");
                break;

            default:
                printf("Invalid Choice");
        }
    }
    else
        printf("Invalid PIN");

    return 0;
}
